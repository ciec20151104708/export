#include<stdio.h>
#include<stdlib.h>
int main()
{
	FILE *fp1;
	char text;
	fp1 = fopen("export.gpx","r");
	if(fp1==NULL)
	{
		printf("读取文件错误");
		return 0;
	}
	else
	{
		text = fgetc(fp1);
		while(text!= EOF)
		{
			printf("%c",text);	
			text = fgetc(fp1);	
		}
		fclose(fp1);		
	} 
	return 0;
}
