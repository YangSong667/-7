# -7
作业
#include <stdio.h>
#include <string.h>
struct Sutdent
{
	char sutdent_ID[17];
	int seat1;
	int seat2;
}student[1000];
int main()
{
	int Iint[1000];
	int i, j, n, a;
	printf("考生数：");
	scanf_s("%d", &a);
	for (i = 0; i < a; i++)
	{
		scanf_s("%s %d %d", &student[i].sutdent_ID, &student[i].seat1, &student[i].seat2);
	}                  
	scanf_s("%d", &n);
	for (j = 0; j < n; j++)
	{
		scanf_s("%d", &Iint[j]);
	}
	for (j = 0; j < n; j++)
	{
		int M;
		for (i = 0; i < a; i++)
		{
			if (Iint[j] == student[i].seat1)
			{
				M = i; break;
			}
		}
		printf("%s %d\n", student[M].sutdent_ID, student[M].seat2);
	}
	return 0;
}
