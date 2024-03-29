1	컴퓨터의 이해 및 구성	- 데이터와 정보 - 정보 처리 과정 - 컴퓨터의 개념 및 구성 - 하드웨어의 종류 및 특징 - 소프트웨어의 실행			강의</br>
2	파이썬 기초	- 파이썬의 역사 - 파이썬의 특징 및 활용 사례 - Google Colab 사용하기 - 데이터 타입과 변수 - 연산자	강의/실습병행		실습</br>
3	제어 구조	- 순차구조 - 선택구조 - 반복구조	강의/실습병행		실습</br>
출석수업평가	맞춤형평가	추후 학교 홈페이지 공고   </br>      	     
출석수업대체시험	온라인과제물	멀티미디어강의 1강~6강  	  </br>     
형성평가	진도10/연습문제10	학습진도율 및 연습문제	 </br>
기말시험	온라인출석시험(객관식)	멀티미디어 강의 전체   </br>

https://github.com/jaehwachung/Python-Programming
실습 colab -> 드라이브복사 -> 코드 -> cmd+ enter(실행)
### 목차
1. [컴퓨터의 이해](#컴퓨터의-이해)
2. [컴퓨터의 구성](#컴퓨터의-구성)
3. [파이썬의 이해](#파이썬의-이해)
4. [파이썬 시작하기](#파이썬-시작하기)
5. [순차 구조](#순차-구조)
6. [선택 구조](#선택-구조)
7. [반복 구조](#반복-구조)
8. [체크포인트 1](#체크포인트-1)
9. [함 수](#함-수)
10. [객체지향](#객체지향)
11. [모듈](#모듈)
12. [파일](#파일)
13. [실전 프로그래밍 1](#실전-프로그래밍-1)
14. [실전 프로그래밍 2](#실전-프로그래밍-2)
15. [체크포인트2](#체크포인트2)

# 파이썬 시작하기
## 프로그래밍 기초
### 숫자와 문자
#### 숫자
  - 정수(int: integer): 소수점이 없는 숫자
  - 실수 (float : floating point) 소수정점이 포함되는 숫자 
#### 문자
  - 유니코드(unicode) 기반문자 또는 문자열
  - 인용부호 " 또는 ' 를 사용하여 표현
### 기본연산자와 표현식
 피연산자와 연산자를 이용한 표현식은 파이썬 __인터프리터__ 에 의해 자동 계산
+, -, *, /, ** 지수(거듭제곱)
### 함수
 특정 작업을 수행하는 코드의 집합으로 함수의 이름만으로 실행할 수 있는 단위 -> print 함수 (화면에 데이터 출력)
 함수의 기본 구조 print("Hello World")
### 함수의 실행
### 들여쓰기
  - 파이썬은 들여쓰기에 의존적 언어 ( 타언어에서는 가독성목적, 파이썬에서 코드의 논리적 집합인 블록을 표현)
  - 들여쓰기 (스페이스 4칸, tab)
  - 블록 중첩시 추가적인 4칸 들여쓰기
### 문서화
  - 주석 사용: 가독성 증대, 개발속도 향상, 유지보수 용이
  - 주석 종류: 한 라인 주석에 # 사용, 여러라인 주석에 ''' 또는 """
## 데이터 저장 (가장중요)
### 원뿔의 부피 & 겉넓이 계산 프로그램 
계산 알고리즘 `부피 = 1/3\pir^2h`  `겉넓이 = \pir^2 + \pirh`
```
#반지름 20, 높이 30
#부피 출력
  print(1 / 3 * 3.14 * 20 ** 2 * 30 )
#겉넓이 출력
  print(3.14 * 20 ** 2 + 3.14 * 20 * 30)
```
### 변수 (variable)
#### 명령형 패러다임 언어의 특징
- 처리할 데이터와 처리된 결과 임시저장
- 변수의 값을 변경하는 할당연산자(=) 이용
### 값의 할당 
- 프로그램이 실행되는 과정에서 처리되는 값이 어떤 행위(입력,연산 등)에 따라 그 값이 변할 수 있는 메모리 내의 저장 공간 지정
- 식별자, 저장공간, 값으로 구성
### 식별자
- 프로그램 내부에 정의된 객체(변수,함수 등)의 이름
- 문자, 숫자, 밑줄로 구성 ( 숫자로는 시작할 수 없음)
- __예약어__ 와 동일할 수 없음 (else,class.1-a,77#R 안됨)
- 길이 제한 없음
### 예약어 (reserved word) : 파이썬 인터프리터에 의해 이미 문법적인 용도로 사용되어 식별자로 사용이 불가능한 단어 
-  pass, lamda, finally, def, try, False, True, if, else, elif, await, async, and, or, not, for, class..
### 변수의 사용
```
#반지름, 높이 __값 할당__
rad = 20
hei = 30
#__값 호출__
#부피 출력 
print(1 / 3 * 3.14 *rad * rad * hei) 
#겉넓이 출력
print(3.14 * rad * rad + 3.14 * rad * hei)
```
#### 프로그램이 실행되는 과정에서 처리되는 값이 어떤 행위(입력,연산)에 따라 그 값이 변할 수 있는 메모리 내의 저장공간 지정
## 산술 연산자
### 산술연산자 정의
- 피연산자(operand)에 대해 지정된 산술연산을 지시하는 기호 (3.14 * rad)
### 특수 산술연산자 : 프로그래밍 언어에서만 사용되는 연산 또는 부호
- 정수 나눗셈 연산자(//)
- 모듈로 연산자(%)
### 연산자 우선순위
표현식에 사용된 여러 연산자의 연산순서 결정
1. 괄호 내부의 수식
2. 지수(**) 연산자
3. 곱셈, 실수 나눗셈, 정수 나눗셈, 나머지 연산자 (왼쪽에서 오른쪽 순서로 적용)
4. 덧셈, 뺄셈 연산자  (왼쪽에서 오른쪽 순서로 적용)
5. 할당 연산자
```
avg = 1 // 3 * 3.14 * 20 ** 2 * (30 + 20 % 10) #12560??
```
### 파이썬 내장함수 : 파이썬 인터프리터에서 기본적으로 지원하는 함수 (별도 모듈,패키지 없이 사용 가능)
- max(), round(), min(), abs(), round(), pow()

# 순차 구조 
