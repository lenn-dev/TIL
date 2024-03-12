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
## 자료형
### 1. 상수 (중요★★)
- 정수형 상수
  
- <img width="393" alt="Screenshot 2024-03-12 at 11 32 34 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/3b553a5b-a584-463a-8694-301b66813926"></br>


 - 실수형 상수: 소수점을 갖는 수

- <img width="451" alt="Screenshot 2024-03-12 at 11 34 20 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/7cbda15b-648b-4ad8-ad7d-454bb6035a8f"></br>


- 문자형 상수(단일 인용부호로 묶음)
☞ ‘A’ => ASCII 값 65, ‘a’ => ASCII 값 97 ☞ ‘B’ => ASCII 값 66, ‘b’ => ASCII 값 98
∫∫
☞ ‘Y’ => ASCII 값 89, ‘y’ => ASCII 값 121
☞ ‘Z’ => ASCII 값 90, ‘z’ => ASCII 값 122

- <img width="400" alt="Screenshot 2024-03-12 at 11 35 27 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/fdf3750c-1afd-402c-aec2-e5b378e9089e"></br>


- 문자열 상수(이중 인용부호로 묶음)

- <img width="432" alt="Screenshot 2024-03-12 at 11 36 23 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/6f6472a9-92cd-4e33-a3a4-dc70aab4a881"></br>


### 2. 변수의 특징과 정의 규칙 (중요★★★)
 
- 모든 변수는 __사용되기 전에 정의__ 한다.
- 변수명은 영문자로 시작되며 숫자나 밑줄(_)을 혼합하여 사용할 수 있다.
- 변수명은 __대문자와 소문자를 구별__ 하여 사용한다.
- 변수명으로 예약어는 사용할 수 없다.

### 3. 자료형의 종류 (중요★)

- <img width="434" alt="Screenshot 2024-03-12 at 11 41 22 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/fc030744-f2cb-4970-b24d-a20af8860be0"></br>

- 기본형
☞ 정수형: int, short, long, unsigned ☞ 실수형: float, double
☞ 문자형: char, unsigned char
☞ 열거형: enurn
☞ void형: void
- 확장형: 배열형, 함수형, 포인터형, 구조체형

### 4. 자료형의 범위 (중요★★★)
- 정수형의 범위
- <img width="432" alt="Screenshot 2024-03-12 at 11 43 10 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/c32c40b9-d90a-440d-95c6-317be5910a37">

☞ 단, 32비트의 경우 int와 unsigned int는 각각 4바이트
♣ 범위는 short int 와 int 만 알아둘 것, 나머지 것까지 외우면 머리 나빠집니다..^^
short int __-32768 ~ 32767__
int __-2147483648~ 2147483647__

- 실수형의 범위
- <img width="432" alt="Screenshot 2024-03-12 at 11 45 34 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/c3f80e36-9c56-4740-b556-80a89a7d72ed">

- 문자형의 범위
- <img width="432" alt="Screenshot 2024-03-12 at 11 46 16 AM" src="https://github.com/lenn-dev/TIL/assets/37726487/bef4c654-af07-42a0-8b19-39f75c605ce5">


#### 4a. 정수형과 문자형의 사용 예 (중요★★★)

<img width="500" alt="Screenshot 2024-03-12 at 2 34 27 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/c75e8964-6ac7-4cf1-924d-b6faf8c9c39a"></br>

<img width="500" alt="Screenshot 2024-03-12 at 2 28 18 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/89c93318-8d84-4d60-ae39-3f803ba5641e"></br>

<img width="500" alt="Screenshot 2024-03-12 at 2 30 56 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/52f435ef-6997-4b7d-8db4-57c39ebc48f9"></br>


## 선행처리기

### 1. 선행처리기 (중요★★)
- 컴파일러에 앞서 __미리 처리__ 되는 처리기
- 사용자가 정의한 각종 내용을 먼저 처리
- 반드시 #로 시작하고 문장의 끝에는 세미콜론(;)을 안 붙임 - 첫 칸부터 시작하고 한 줄에 하나의 명령


### 2. 선행처리기 사용시 주의할 점 (중요★★)
- 반드시 __#__ 로 시작
- 명령문 끝에는 세미콜론(;)을 __붙이지 않음__
- 한 줄에 하나의 명령만 사용
- 소스 프로그램의 __첫 부분__에 위치

### 3. 선행처리기의 종류
<img width="403" alt="Screenshot 2024-03-12 at 8 53 49 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/19245ce7-d3e7-4c53-8730-dbac5717c8e2">

#### 3a. 파일포함
__#include__ 
- #include는 C언어에서 제공되는 헤더파일(*.h)를 자신의 소스파일에 읽어들여 함께 컴파일 하고자 할 때 사용
- C 프로그램에서 표준함수인 printf( ), scanf( ) 등을 사용하려면
-  이 함수들의 원형(prototype)이 선언되어 있는 표준 입출력 헤더파일인 stdio.h를 #include 시켜야 함
```
형식: 
#include<파일명> 
#include "파일명"
사용예 : 
#include <stdio.h>
#include "stdio.h"
#include "∖tc∖lib∖math.h"
기능:
 #include 다음에 제시된 파일을 현재 프로그램에 포함시킨다.
- <파일명>은 표준 디렉토리(보통 include 디렉토리)에서 파일을 찾아 포함
- "파일명"은 현재 사용 중인 디렉토리나 지정된 디렉토리에서 파일을 찾아 포함하며, 또는 드라이브나 경로를 사용
```

#### 3b. 매크로 정의 (중요★★) - 단순치환, 상수,함수 정의할 때 많이 사용
 __#define__ 
#define은 매크로를 정의할 때 사용
- 매크로(macro)
  - 선행처리기 #define을 사용하여 단순 치환되는 자료
  - 프로그램 작성시에 명령이나 수식 또는 상수값이 자주 사용될 때 이들을 대표하는 이름을 붙여 사용하는 대상
- 매크로 정의
  - 매크로 상수 정의
  - 매크로 함수 정의

__매크로 상수 정의__
```
- 형식:
#define 매크로명 자료
#undef 매크로명
- 사용예:
# define PI 3.141592
- 이는 프로그램 내의 __PI는 3.141592로 치환__하라는 것
- 기능:
프로그램에 나오는 매크로명을 지정한 자료로 치환한 후 컴파일하거나(#define), 정의를 해제(#undef)한다.
``` 
<img width="466" alt="Screenshot 2024-03-12 at 9 07 39 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/95eaaf0e-7fb5-4594-800d-9372bf095625"></br>

 __매크로 함수 정의__ (중요★★★)
 ```
 형식:
#define 매크로명(인수)(수식)
#define 매크로명(인수, 인수) (수식)
사용예:
#define AREA(x)(3.141592*(x)*(x)) //AREA(x) 라는 함수는 (3.141592*(x)*(x)) 로 정의된다.
#define HAP(a, b) (a+b)
장점 :
- 선행처리기에 의한 __단순 치환 방식__이므로, 전달 인자의 자료형을 명시할 필요가 없고, 또 어떠한 자료형 변수를 인자로 전달해도 잘 동작한다.
- __한 두 줄의 코드인 경우 함수로 정의하는 것보다 속도가 빠르다.__
```

<img width="472" alt="Screenshot 2024-03-12 at 9 16 30 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/8e5a3c3a-33c0-4d52-b5ec-56b5c6d2f050"></br>

__조건부 컴파일 (중요★)__
- #if #else #elif #endif
  - 조건에 따라 프로그램을 컴파일하는 명령
  - 최적의 코드로 프로그램을 작성할 수 있기 때문에 __시스템의 성능 향상__
- #if 와 #elif 다음에는 컴파일 여부를 결정하는 __조건문 필요__
  - 조건문은 선행처리과정에서 진위 여부를 판단할 수 있어야 함
  - 변수지정이나 함수 호출 불가
  - 주로 매크로 값이 사용
    
<img width="491" alt="Screenshot 2024-03-12 at 9 18 33 PM" src="https://github.com/lenn-dev/TIL/assets/37726487/cbce017f-0acd-452c-a375-f2cfb66cec7d">




# 입출력 함수와 연산자 1
# 입출력 함수와 연산자 2
# 선택 제어문과 반복 제어문
