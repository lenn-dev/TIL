1	자료형과 선행처리기	-상수와 변수 -자료형과 변수 선언 -선행처리기			강의</br>  
2	입,출력 함수와 연산자	-표준 입출력 함수 -각종 연산자			강의</br>  
3	실습	-컴파일러 사용법 -프로그램 작성방법 -프로그램 실습			실습</br>  

출석수업평가	맞춤형평가	추후 학교 홈페이지 공고</br>        	            
출석수업대체시험	온라인과제물	교재(2020) 1장~4장(멀티미디어 강의 1강~5강)  	</br>              
형성평가	진도20/연습문제0	학습진도율 및 연습문제	 </br>  
기말시험	온라인출석시험(객관식)	교재 전체(특히 4,5,6장)(해당 멀티미디어 강의 포함)  </br>  
### 목차
1. [C언어의 개요](#C-언어의-개요)
2. [자료형과 선행처리기](#자료형과-선행처리기)
3. [입.출력 함수와 연산자 1](#입출력-함수와-연산자-1)
4. [입.출력 함수와 연산자 2](#입출력-함수와-연산자-2)
5. [선택 제어문과 반복 제어문](#선택-제어문과-반복-제어문)
6. [함수와 기억 클래스 1](#함수와-기억-클래스-1)
7. [함수와 기억 클래스 2](#함수와-기억-클래스-2)
8. [배열과 포인터 1](#배열과-포인터-1)
9. [배열과 포인터 2](#배열과-포인터-2)
10. [배열과 포인터 3](#배열과-포인터-3)
11. [구조체와 공용체 1](#구조체와-공용체-1)
12. [구조체와 공용체 2](#구조체와-공용체-2)
13. [파일처리 함수 1](#파일처리-함수-1)
14. [파일처리 함수 2](#파일처리-함수-2)
15. [메모리 동적 할당](#메모리-동적-할당)

# C 언어의 개요
# 자료형과 선행처리기
3강 주제: 자료형과 선행처리기
1. 상수 (중요★★)
- 정수형 상수
  
- <img width="393" alt="Screenshot 2024-03-12 at 11 32 34 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/3b553a5b-a584-463a-8694-301b66813926"></br>


 - 실수형 상수: 소수점을 갖는 수

- <img width="451" alt="Screenshot 2024-03-12 at 11 34 20 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/7cbda15b-648b-4ad8-ad7d-454bb6035a8f"></br>


- 문자형 상수(단일 인용부호로 묶음)
☞ ‘A’ => ASCII 값 65, ‘a’ => ASCII 값 97 ☞ ‘B’ => ASCII 값 66, ‘b’ => ASCII 값 98
∫∫
☞ ‘Y’ => ASCII 값 89, ‘y’ => ASCII 값 121
☞ ‘Z’ => ASCII 값 90, ‘z’ => ASCII 값 122

- <img width="324" alt="Screenshot 2024-03-12 at 11 35 27 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/fdf3750c-1afd-402c-aec2-e5b378e9089e"></br>


  - 문자열 상수(이중 인용부호로 묶음)

- <img width="432" alt="Screenshot 2024-03-12 at 11 36 23 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/6f6472a9-92cd-4e33-a3a4-dc70aab4a881"></br>


2. 변수의 특징과 정의 규칙 (중요★★★)
 
- 모든 변수는 사용되기 전에 정의한다.
- 변수명은 영문자로 시작되며 숫자나 밑줄(_)을 혼합하여 사용할 수 있다. - 변수명은 대문자와 소문자를 구별하여 사용한다.
- 변수명으로 예약어는 사용할 수 없다.

3. 자료형의 종류 (중요★)

- <img width="434" alt="Screenshot 2024-03-12 at 11 41 22 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/fc030744-f2cb-4970-b24d-a20af8860be0"></br>

기본형
☞ 정수형: int, short, long, unsigned ☞ 실수형: float, double
☞ 문자형: char, unsigned char
☞ 열거형: enurn
☞ void형: void
확장형: 배열형, 함수형, 포인터형, 구조체형

4. 자료형의 범위 (중요★★★)
- 정수형의 범위
- <img width="376" alt="Screenshot 2024-03-12 at 11 43 10 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/c32c40b9-d90a-440d-95c6-317be5910a37">

☞ 단, 32비트의 경우 int와 unsigned int는 각각 4바이트
♣ 범위는 short int 와 int 만 알아둘 것, 나머지 것까지 외우면 머리 나빠집니다..^^
- 실수형의 범위
- <img width="339" alt="Screenshot 2024-03-12 at 11 45 34 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/c3f80e36-9c56-4740-b556-80a89a7d72ed">

- 문자형의 범위
- <img width="336" alt="Screenshot 2024-03-12 at 11 46 16 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/bef4c654-af07-42a0-8b19-39f75c605ce5">

4. 정수형과 문자형의 사용 예 (중요★★★)
 ```  
#include <stdio.h>
void main() // main 함수는 어떤 값을 돌려줄 필요가 없음 {
char ch;
int in;
ch = in = ‘A’;
printf(“\nch = %d\n”, ch); // %d는 십진수 출력을 의미 printf(“in = %d\n”, in);
ch = in = 100;
printf(“\nch = %c\n”, ch); // %c는 문자 출력을 의미 printf(“in = %c\n”, in);
}
```
실행결과 ch = 65 in = 65
ch = d in = d
```
#include <stdio.h> void main()
{
long int num1, num2;
num1=32767L+1; // L은 long(4바이트)을 의미, L을 안 붙이면 2바이트만 인식되므로 오류 num2=-32768L-1;
printf(“\num1= %ld ”,num1); // %ld는 long형이고, 십진수로 출력하라는 의미 printf(“\num2= %ld ”,num2);
}
```
실행결과: num1= 32768 num2= -32769
L을 안 붙였을 경우의 실행결과:
num1= -32768 (원하는 값이 안나옴 → 오류)
num2= 32767 (원하는 값이 안나옴 → 오류)
```
#include <stdio.h> void main()
{
int i, sum; // sum=0; 이라고 초기화 하는 부분이 없으므로 메모리에 원래 있던 값이 셋팅 for(i = 1; i <= 10; i++)
sum = sum + i;
printf(“1부터 10까지의 합 = %d\n”, sum); // 결과는 메모리에 있는 값에 따라 달라짐
}
```
실행결과:
1부터 10까지의 합 = 4260155
♣ 초기화하지 않으면 메모리에 있던 값이 그대로 반영되므로 위 실행결과처럼 항상 4260155가
나오는 것이 아니죠.. (그때 그때 달라요 ~~)
# 입출력 함수와 연산자 1
# 입출력 함수와 연산자 2
# 선택 제어문과 반복 제어문
