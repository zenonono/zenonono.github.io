---
layout: single
title: "C언어" 
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
---

### 1.사주보기(교과서 96쪽 문제01)
#include <stdio.h>
main()
{
 int year, month, day, res;
 printf("당신의 사주를 봐드립니다\n연도, 월, 일을 차례대로 입력하세요 : ");
 scanf("%d %d %d", &year, &month, &day);
 res = (year-month+day) % 10;
 if(year-month+day == 0)
 printf("당신의 사주는 대박입니다\n");
 else
 printf("당신의 사주는 그럭저럭입니다.\n");
}
~~~

### 2. 3개의 터널 (교과서 98쪽 문제02)
#include <stdio.h>
int main()
{
 int a, b, c;
 printf("세 터널의 높이를 차례대로 입력하세요 : ");
 scanf("%d %d %d", &a, &b, &c);
 if (a < 170)
  printf("충돌 %d", a);
 else if (b < 170)
  printf("충돌 %d", b);
 else if (c < 170)
  printf("충돌 %d", c);
 else
 printf("무사 통과");
}
~~~

### 3. 이 달은 며칠까지 있을까?(교과서 100쪽 문제03)
#include <stdio.h>

int main(void) {
  int year, month;
  printf("연도와 월을 입력하세요 : ");
  scanf("%d %d, &year, &month");
  printf("%d년 %d월의 마지막 날은", year, month);
  if(month==1|month==3|month==5|month==8|month==10|month==12)
   printf("%d", 31);
  else if(month==4|month==6|month==9|month==11)
  printf("%d", 30);
  else{
    if((year%4==0 && !(year%100==0))||year%400==0)
     printf("29");
    else
    printf("28");
  }
  printf("감사합니다");
  return 0;
}
~~~

### 4. 30분 전(교과서 102쪽 문제04)
#include <stdio.h>
int main(void) {
 int hour, min;
 printf("시간과 분을 입력하세요 :");
 scanf("%d %d", &hour, &min);
 printf("입력한 시간의 30분 전 시간은 ");
 if(min>=30)
 printf("%d시 %d분\n", hour, min-30);
 else
 {
   if(hour == 0)
   printf("%d시 %d분\n", 23, min+30);
   else
   printf("%d시 %d분\n", hour-1, min+30);
 }
 return 0;
}
~~~

### 5. 용돈으로 책 구매(교과서 104쪽 01)
#include <stdio.h>

int main(void) {
 int money, remain, book = 15000;
 printf("책의 가격은 15000원입니다.\n");
 printf("당신이 가진 용돈은 얼마인가요? : ");
 scanf("%d", &money);
 if (money >= book){
  remain = money - book;
  printf("책을 구입하였습니다, 이제 남은 용돈은 %d입니다.\n", remain);
  } else
 printf("책을 구입하지 못했습니다.");
  return 0;
}
~~~

### 6. 도어락 
#include <stdio.h>

int main(void) {
  int select;
  char cic='c', ic;
  int dpw=24680, pw;
  double dfig=1.23456789, fig;

  printf("장치 선택: \n");
  scanf("%d", &select);
  if (select==1){
  printf("IC 카드: ");
  scanf(" %c", &ic);
  }else if(select==2){
  printf("비밀번호: ");
  scanf("%d", &pw);
  }else{
    printf("지문: ");
    scanf("&if", &fig);
  }

  if(cic==ic||dpw==pw||dfig==fig)
  printf("문 열림~");
  else
  printf("디리릭!디리릭!");

  return 0;
}
~~~

### 7. 과목 점수 측정(교과서 105쪽 03)
#include <stdio.h>

int main(void) {
  int score;
  printf("과목의 점수를 입력하세요 : ");
  scanf("%d", &score);
  if (score >= 90) printf("수\n");
  else if (score >= 70) printf("미\n");
  else if (score >= 80) printf("우\n");
  else if (score >= 60) printf("양\n");
  else printf("가\n");
  return 0;
}
~~~

### 9.가위바위보
#include <stdio.h>

int main() {
  char com, user;
  com='s';

  printf("r/s/p: ");
  scanf("%c", &user);

  if(com==user)
   printf("비겼다");
  else if (com=='r' && user=='s' || com=='s' && user=='p' || com=='p' && user=='r')
   printf("졌다");
  else 
   printf("이겼다");

  return 0;
}
~~~
