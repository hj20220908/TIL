# Python

## Python의 특징

- 인터프리터 기반의 객체지향 언어
- 플랫폼에 구애받지 않는 언어
- 동적 타이핑 방식의 언어
- 리플렉션을 지원하는 언어
- 확장성이 뛰어난 언어

## 자료형

### Number(숫자 자료형)

```python
print(5)
print(-10)
print(3.14)
print(1000)
print(5+3)
print(2*8)
print(2*(3+1))
```

### String(문자열 자료형)

```python
test = "Hello World!"

test = 'Hello World!'

# r’’ 로 문자열을 감싸주게 되면 raw라는 뜻으로 아무 의미없는 문자열이라는 것을 나타냄.
test = r'C:\Test'

first = 'Ji'
last = 'Ny'

print(first + last)  # JiNy
print(last * 5)      # NyNyNyNyNy
```

### Boolean(논리 자료형)

```python
print(5 > 10)
print(5 < 10)
print(True)
print(False)
print(not True)
print(not False)
print(not 5 > 10)
```

### 변수

```python
animal = "강아지"
name = "연탄이"
age = 4
hobby = "낮잠"
is_adult = age >= 3

print("우리집" + animal + "의 이름은 " + name + "에요.")
print(name + "는 " + str(age) + "살이며, " + hobby + "를 아주 좋아해요")
print(name + "는 어른일까요? " + str(is_adult))
```

- 숫자를 문자로 변환하지 않으면 아래와 같은 에러가 발생함

```txt
예외가 발생했습니다. TypeError
can only concatenate str (not "bool") to str
```

### 주석

```python
# 문장 하나 주석

'''
여러
문장
주석
'''
```

## 연산자

### 연산자

```python
print(5 + 6)   # 11
print(5 - 2)    # 3
print(3 * 8)   # 24
print(3 ** 3)  # 27, 제곱
print(8 / 2)    # 4.0, float형
print(8 // 2)   # 4, 몫 구하기, int형
print(8 % 3)   # 2, 나머지 구하기

print(10 > 3)
print(4 >= 7)
print(10 < 3)
print(5 <= 5)
print(3 == 3)
print(4 == 2)
print(3 + 4 == 7)

print(1 != 3)
print(not (1 == 3))

print((3 > 0) and (3 < 5))
print((3 > 0) & (3 > 5))
print((3 > 0) or (3 < 5))
print((3 > 0) | (3 > 5))
print((3 < 0) | (3 > 5))
```

### 숫자처리함수

```python
from math import *

print(abs(-5))  # 5
print(pow(4, 2))  # 4^2 = 16
print(max(5, 12))  # 12
print(min(5, 12))  # 5

print(round(3.14))  # 3
print(round(4.99))  # 5

print(floor(4.99))  # 내림, 4
print(ceil(3.14))  # 올림, 4
print(sqrt(16))  # 제곱근, 4
```

### 랜덤 함수

```python
from random import *
print(random())  # 0.0 ~ 1.0 미만의 임의의 값 생성
print(random() * 10)    # 0.0 ~ 10.0 미만의 임의의 값 생성
print(int(random() * 10))  # 0 ~ 10 미만의 임의의 값 생성

print()
print(int(random() * 10) + 1)  # 1~ 10 이하의 임의의 값 생성
print(int(random() * 10) + 1)  # 1~ 10 이하의 임의의 값 생성
print(int(random() * 10) + 1)  # 1~ 10 이하의 임의의 값 생성
print(int(random() * 10) + 1)  # 1~ 10 이하의 임의의 값 생성
print(int(random() * 10) + 1)  # 1~ 10 이하의 임의의 값 생성
print()
print(randrange(1, 45))  # 1 ~ 45 미만의 임의의 값 생성
print(randint(1, 45))   # 1 ~ 45 이하의 임의의 값 생성
```

## 문자열 처리

### 문자열

```python
sentence = '나는 소년입니다'
sentence2 = "파이썬은 쉬워요"
sentence3 = """
나는 소년이고,
파이썬은 쉬워요
"""
print(sentence3)
```

### 슬라이싱

```python
jumin = "990120-1234567"
print("성별 : " + jumin[7])
print("연 : " + jumin[0:2])
print("생년월일 : " + jumin[:6])
print("뒤 7자리 : " + jumin[7:])
print("뒤 7자리 : " + jumin[-7:])

```

### 문자열처리함수

```python
python = "Python is Amazing"
print(python.lower())
print(python.upper())
print(python[0].isupper)  # 대문자인가 ? True : False
print(len(python))  # 문자열 길이
print(python.replace("Python", "Jave"))  # Jave is Amazing

index = python.index("n")   # 문자 위치 찾기
print(index)
index = python.index("n", index + 1)    # 두번째 위치
print(index)

print(python.find("n"))
print(python.find("Jave"))  # 값이 없을 경우 -1 반환
# print(python.index("Jave")) # 값이 없을 경우 오류 반환 -> 프로그램 종료
print(python.count("n")) # 2
```

### 문자열포맷

```python
print("a" + "b")
print("a", "b")
print()

# 방법1
print("나는 %d살입니다." % 20)  # #d : int 타입
print("나는 %s를 좋아해요" % "python")  # %s : string 타입
print("Apple 은 %c로 시작해요." % "A")  # %c : char 타입
print()

# %s
print("나는 %s살입니다." % 20)  # #d : int 타입
print("나는 %s색와 %s색을 좋아해요" % ("파란", "빨간"))
print()

# 방법 2
print("나는 {}살입니다.".format(20))  # #d : int 타입
print("나는 {}를 좋아해요".format("python"))  # %s : string 타입
print("나는 {}색와 {}색을 좋아해요".format("파란", "빨간"))
print("나는 {0}색와 {1}색을 좋아해요".format("파란", "빨간"))   # 나는 파란색와 빨간색을 좋아해요
print("나는 {1}색와 {0}색을 좋아해요".format("파란", "빨간"))   # 나는 빨간색와 파란색을 좋아해요
print()

# 방법 3
print("나는 {age}살이며, {color}색을 좋아해요".format(age=20, color="빨간"))
print("나는 {age}살이며, {color}색을 좋아해요".format(color="빨간", age=20))
print()

# 방법 4 (v3.6 이상~)
age = 20
color = "빨간"
print(f"나는 {age}살이며, {color}색을 좋아해요")
```

### 탈출문자

```python
# \n
print("백문이 불여일견\n 백견이 불여일타")
print()

print("저는 \"나도코딩\"입니다.")   # 저는 "나도코딩"입니다.
print('저는 "나도코딩"입니다.')     # 저는 "나도코딩"입니다.
print()

# \\ : 문장 내에서 \
print("c:\\Users")
print()

# \r : 커서를 맨 앞으로 이동 후 다음 문장으로 덮어씌움
print("Red Apple\rPine")    # PineApple
print("Red  Apple\rPine")   # Pine Apple
print()

# \b : 백스페이즈 (한 글자 삭제)
print("Redd\bApple")    # RedApple

# \t : tab
print("Red\tApple") # Red     Apple
```

## 자료구조

### 리스트 []

```python
subway = [10, 20, 30]
print(subway)
print()

subway = ["유재석", "조세호", "박명수"]
print(subway[1])    # 조세호

# 하하씨가 다음 정류장에서 다음 칸에 탐
subway.append("하하")   # ['유재석', '조세호', '박명수', '하하']
print(subway)
print()

# 정형돈씨를 유재석 / 조세호 사이에 태워봄
subway.insert(1, "정형돈")
print(subway)   # ['유재석', '정형돈', '조세호', '박명수', '하하']
print()

# 지하철에 있는 사람들 한 명씩 뒤에서 꺼냄
print(subway.pop())
print(subway)   # ['유재석', '정형돈', '조세호', '박명수']
print()
print(subway.pop())
print(subway.pop())
print(subway)   # ['유재석', '정형돈']
print()

# 같은 이름의 사람이 몇 명 있는지 확인
subway.append("유재석")
print(subway.count("유재석"))   # 2
print()

# 정렬도 가능
num_list = [5, 2, 4, 3, 1]
num_list.sort()
print(num_list)  # [1, 2, 3, 4, 5]

num_list.reverse()
print(num_list)  # [5, 4, 3, 2, 1]
print()

# 모두 지우기
num_list.clear()
print(num_list)  # []
print()

# 다양한 자료형 함께 사용
num_list = [5, 2, 4, 3, 1]
mix_list = ["조세호", 20, True]
print(mix_list) # ['조세호', 20, True]

# 리스트 확장
num_list.extend(mix_list)
print(num_list) # [5, 2, 4, 3, 1, '조세호', 20, True]
```

### Dictionary(사전 자료형)

```python
cabinet = {3: "유재석", 100: "김태호"}
print(cabinet[3])  # 유재석
print(cabinet[100])  # 김태호
print()

# get()
print(cabinet.get(3))
# print(cabinet[5]) # 값이 없을 경우, 오류를 발생시키고 종료함
print(cabinet.get(5))   # None, 오류를 발생시키지 않고 다음 명령어를 실행함
print(cabinet.get(5, "사용 가능"))  # 값이 없을 경우 "사용 가능" 출력

print(3 in cabinet)  # 3이라는 데이터가 있는가 ? True : False
print()

# 목욕탕 영업시작
cabinet = {"A-30": "유재석", "B-100": "김태호"}

# 새 손님
cabinet["c-20"] = "조세호"
print(cabinet)  # {'A-30': '유재석', 'B-100': '김태호', 'c-20': '조세호'}
cabinet["A-30"] = "김종국"
print(cabinet)  # {'A-30': '김종국', 'B-100': '김태호', 'c-20': '조세호'}
print()

# 간 손님
del cabinet["A-30"]
print(cabinet)  # {'B-100': '김태호', 'c-20': '조세호'}
print()

print(cabinet.keys())   # dict_keys(['B-100', 'c-20'])
print(cabinet.values())  # dict_values(['김태호', '조세호'])
print(cabinet.items())  # dict_items([('B-100', '김태호'), ('c-20', '조세호')])

# 목욕탕 폐점
cabinet.clear
print(cabinet) # []
```

### Tuple(튜블 자료형)

- 내용 변경과 추가할 수 없음
- list보다 속도가 빠름

```python
menu = ("돈까스", "치즈까스")
print(menu[0])
print(menu[1])
# menu.add("생선까스") # tuple은 add 함수를 제공하지 않음, 오류 발생 후 종료

name = "김종국"
age = 20
hobby = "코딩"
print(name, age, hobby)

# Tuple 활용
(name, age, hobby) = "김아무개", 30, "독서"
print(name, age, hobby) # 김아무개 30 독서
```

### set

- {}를 쓰지만 사전과 다름 주의
- 집합형 함수 존재 (intersection, union, difference)

```python
# 중복이 안됨, 순서 없음
my_set = {1, 2, 3, 3, 3}
print(my_set)   # {1, 2, 3}

java = {"유재석", "김태호", "양세형"}
python = set(["유재석", "박명수"])

# 교집합 (java와 python을 모두 할 수 있는 개발자)
print(java & python)    # {'김태호', '박명수', '양세형', '유재석'}
print(java.intersection(python))  # 교집합

# 합집합 (java를 할 수 있거나 python을 할 수 있는 개발자)
print(java | python)    # {'김태호', '박명수', '양세형', '유재석'}, 순서는 보장되지 않음
print(java.union(python))  # 합집합

# 차집합 (java는 할 수 있지만 python은 할 줄 모르는 개발자)
print(java - python)  # {'김태호', '양세형'}
print(java.difference(python))  # 차집합

# python 할 줄 아는 사람이 늘어남
python.add("김태호")
print(python)   # {'김태호', '유재석', '박명수'}

# java를 잊어버림
java.remove("김태호")
print(python)   # {'김태호', '유재석', '박명수'}
```

### 자료구조의 변경

```python
# 커피숍
menu = {"커피", "우유", "주스"}
print(menu, type(menu))  # {'커피', '주스', '우유'} <class 'set'>

menu = list(menu)
print(menu, type(menu))  # ['주스', '커피', '우유'] <class 'list'>

menu = tuple(menu)
print(menu, type(menu))  # ('커피', '주스', '우유') <class 'tuple'>

menu = set(menu)
print(menu, type(menu))  # {'커피', '주스', '우유'} <class 'set'>
```

## 제어문

### if

```python
weather = input("오늘 날씨는 어때요? : ")
if weather == "비":
    print("우산을 챙기세요")
elif weather == "마스크":
    print("마스크를 챙기세요")
else:
    print("준비물이 필요 없어요.")
```

### for

```python
for waiting_no in [0, 1, 2, 3, 4]:
    print("대기번호 : {0}".format(waiting_no))  # 0~4

for waiting_no in range(1, 6):
    print("대기번호 : {0}".format(waiting_no))  # 1~5
```

### while

```python
customer = "토르"
index = 5
while index >= 1:
    print("{0}님, 커피가 준비 되었습니다. {1}번 남았어요.".format(customer, index))
    index -= 1
    if index == 0:
        print("커피는 폐기처분되었습니다.")
```

### continue break

```python
absent = [2, 5]  # 결석
no_book = [7]
for student in range(1, 11):
    if student in absent:
        continue
    elif student in no_book:
        print("오늘 수업 여기까지. {0}는 교무실로 따라와".format(student))
        break
    print("{0}, 책을 읽어봐".format(student))
```

### 한줄 for

```python
students = [1, 2, 3, 4, 5]
print(students) # [1, 2, 3, 4, 5]
students = [i+100 for i in students]
print(students) # [101, 102, 103, 104, 105]
```

## 함수

```python
# 함수
def open_account():
    print("새로운 계좌가 생성되었습니다.")

open_account()
```

### 전달값과 반환값

# 함수

```python
def open_account():
    print("새로운 계좌가 생성되었습니다.")
open_account()

# 전달값과 반환값
def deposit(balance, money):  # 입금
    print("입금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance + money))
    return balance + money

balance = 0
balance = deposit(balance, 1000)
print(balance)

# 기본값
def profile(name, age=17, main_lang="파이썬"):
    print("이름 {}, 나이: {}, 사용언어:{}".format(name, age, main_lang))
profile("유재석")   # 이름 유재석, 나이: 17, 사용언어:파이썬

# 키워드
profile(main_lang="자바", name="유재석")    # 이름 유재석, 나이: 17, 사용언어:자바

# 가변인자
def profile2(name, age, lang1, lang2, lang3, lang4, lang5):
    print("이름 {}, 나이: {}".format(name, age), end=" ")
    print(lang1, lang2, lang3, lang4, lang5)

# 이름 유재석, 나이: 20 Python java C C++ C#
profile2("유재석", 20, "Python", "java", "C", "C++", "C#")

def profile3(name, age, *language):
    print("이름 {}, 나이: {}".format(name, age), end=" ")
    for lang in language:
        print(lang, end=" ")
    print()

profile3("김태호", 25, "Kotilin", "java")   # 이름 김태호, 나이: 25 Kotilin java
```

# Reference

[파이썬 강의(기본편)]() <br/>
[Myungseo Kang](https://blog.myungseokang.dev/posts/python-basic-grammar1/)
