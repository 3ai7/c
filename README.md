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
