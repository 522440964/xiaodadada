# xiaodadada
#include<stdio.h>
#include<string.h>
int main()
{
	char s[1000];
	char w[100];
	int i,j,wl,sl,t=0,num;
	printf("请输入一串字符\n");
	gets(s);
	printf("请输入一个字符\n");
	gets(w);
	strlwr(s);
	strlwr(w);
	wl=strlen(w);
	sl=strlen(s);
	for(i=0;i<sl;i++)
	{
		num=0;
		if(s[i]==w[0])
		{
			for(j=0;j<wl;j++)
			{
				if(s[i+j]==w[j])
				{
					num++;
				}	
			}
			if(num==wl) t++;
		}
	}
	
	printf("相同的个数为%d\n",t);
			return 0;
}
