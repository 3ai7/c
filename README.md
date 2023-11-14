# c
初入计算机语言的学习
//写1~100的奇数
#include<stdio.h>
int main()
{
	
	for (int i = 1; i <= 100; i++) {
		while (i % 2 == 1) {
			printf("%d ", i);
			i++;
		}
	}
		return 0;
	
}

对于输入缓冲区，用while循环将里面的字符清空，以getchar()来取，
因为我们按回车键时会在输入缓冲区中留下字符'\n'，其ascll值为10。
同时，当输入多个字符时，在字符中间按了空格，那么就只会读取空格前面的字符，
会有剩余字符在输入缓冲区中，需要读取多次才能清空输入缓冲区，
才会在下一阶段停留，等待你输入字符。
#include<stdio.h>
int main()
{
	int ret = 0;
	char arr[20] = { 0 };
	printf("请输入密码:");
	scanf("%s", &arr);
	while (getchar() != '\n')
	{
		;
	}
	printf("请确认(y/n):");
	ret = getchar();
	if (ret == 'y')
	{
		printf("确认成功\n");
	}
	else
	{
		printf("放弃确认\n");
	}
	return 0;
}
