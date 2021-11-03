#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>


void Add(int* p)

{

	(*p)++;
  
}


int main()

{

	int num = 0;
  
	while (num < 5000)
  
	{
  
		//调用一次num就增加1的函数
    
		Add(&num);
    
		printf("%d\n", num);
    
	}
  
	
	return 0;
  
}


//函数的嵌套调用和链式访问


#include<string.h>

int main()

{

	//int len = strlen("abc");
  
	//printf("len=%d\n", len);
  

	//链式访问
  
	//printf("%d\n", strlen("abc"));

	char arr1[20] = { 0 };
  
	char arr2[] = "bit";
  
	//strcpy(arr1, arr2);
  
	printf("arr1=%s\n", strcpy(arr1, arr2));
  

	printf("%d", printf("%d", printf("%d", 43)));//43 2 1,返回字符个数
  

	return 0;
  
}



int main()

{

	int a = 10;
  
	int b = 20;
  
	//声明函数-告知
  
	int Add(int, int);
  
	int c = Add(a, b);
  
	printf("%d\n", c);
  
	return 0;
  
}


//函数定义

int Add(int x, int y)

{

	return x + y;
  
}
