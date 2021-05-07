# 0507
## 進階題：字串中的數字個數 

```C
#include <stdio.h>
int main ()
{
	char a[80];
	int ans=0;
	scanf("%s",&a);
	int i=0;
	while(a[i]!='\0'){
		if(a[i]>='0'&&a[i]<='9')ans++;
			i++;
	}
	printf("%d",ans);
}
```
## 利用自訂函式最大值max與最小值min求出兩者之差
```C
#include<iostream>
using namespace std;
int max(int a,int b,int c, int d)
{
	int max;
	if(a>b && a>c && a>d)max=a;
	else if (b>a && b>c && b>d)max=b;
	else if (c>a && c>b && c>d)max=c;
	else max=d;
	return max;
}
int min(int a,int b,int c,int d)
{
	int min;
	if(a<b && a<c && a<d)min=a;
	else if (b<a && b<c && b<d)min=b;
	else if (c<a && c<b && c<d)min=c;
	else min=d;
	return min;
}
int main(){
  int a,b,c,d;cin>>a>>b>>c>>d;
  cout<<(max(a,b,c,d)-min(a,b,c,d));
  return 0;
}
/* 上方C++ main 函式 等同於 下方 C 的 main 函式
int main(void){
  int a, b, c, d;
  scanf("%d %d %d %d", &a, &b, &c, &d);
  printf("%d",  max(a,b,c,d) - min(a,b,c,d) );
  return 0;
}
```
## 進階題：奇數之和 
```C
  #include <stdio.h>
int main()
{
	int n,ans=0;
	scanf("%d",&n);
	for(int i=1;i<=n;i++){
	if(i%2!=0)ans+=i;
	}
	printf("%d",ans);
}
```
## 進階題：兩數間可被7整除的數 
```C
#include <stdio.h>
int main ()
{
	int a,b;
	scanf("%d%d",&a,&b);
	for(int i=a;i<=b;i++){
	if(i%7==0) printf("%d ",i);
	}
}
```
