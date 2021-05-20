---
layout: single
title: "조건문"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
---

### 01. 사주보기
![saju](/assets/images/if1.PNG)
~~~c
#include <studio.h>
 int main(void)
{ int year, month, day, result;

printf("당신의 사주를 봐드립니다.\n");
printf("연도 월 일을 차례대로 입력하세요 : ");
scanf("%d, %d, %d", &year, &month, &day);

result=(year-month+day)%10;
if(result==0)
