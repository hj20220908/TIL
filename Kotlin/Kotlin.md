# Kotlin
## 함수

```kotlin
class Student(val name : String, val birthYear : Int) {
  fun price() {
      Log.d("연습용", this.name)
  }
  
  fun getMyAgeIn2021() : Int {
    val myAge = 2021 - this.birthYear + 1
    return myAge
  }
}
```

## 생성자 - Constructor
* 사용법
  * 생성자를 만드는 방법 - 주(Main) 생서앚 (!) / 보조 생성자
  ```kotlin
  class 클래스이름 (필요변수 : 타입, 필요변수2 : 타입2)
  class Room(price : Int, address : String)
  ```
  * 만들어둔 생성자를 사용하는 방법
  ```kotlin
  // JAVA : new 클래스이름(필요한 변수);
  // Kotlin : 클래스이름(필요한 변수)
  // ex. Room을 갹체화
  // new Room(8000, "서울시 마포구"); // JAVA
  Room(8000, "서울시 마포구") //Kotlin
  ```
* 트깅 사항
  * 주 생성자를 정의할 때 변수의 이름 앞에 val/var을 붙이면, 클래스 멤버변수로 활용가능

## 상속 - Inheritance
* 코틀린 문법
  * 클래스를 만들 때 => 내 부모가 누구인지 지정
    * class 클래스이름 : 부모클래스(어떤 생성자 기반)
* 특이 사항
  * 대부분의 상속에서, 부모 클래스의 생성자 중 기본 생성자를 기반으로 상속받는다.
  * 일부 부모 클래스의 경우, 기본생성자를 지원하지 않는 경우도 있다.
    * : 부모클래스() 형태를 사용할 수 없다. (빈 광호 지원 X)
    * () 내부에, 부모클래스가 요구하는 변수를 넣어서 다른 생성자를 사용하도록 해야 함.
    * 자식 클래스의 주 생성자를 통해서 받아낸 재료를 부모에게 전달해서 사용.

## null 관리
* 언어 설계의 주요 목표중 하나 : NullPointException으로부터 자유로운 언어를 만들고 싶다.
* JAVA에는 없는 별도의 null 처리 문법 제공. (Swift와 유사함)
  * 변수를 만들 때, 자료형에 특별히 명시를 하지 않으면, 해당 변수에는 절대로 null을 대입할 수 없게 되어있다.
  * 만약 필요에 의해 null이 들어올 수 있는 여지를 남겨야 한다면, 자료형 뒤에 ?를 붙여야만 null 대입이 가능해짐

## 자료형 변환 - Casting
* 기본 클래스
  * 각각의 클래스마다, 다른 형태로 변환시켜주는 함수들이 내장되어있다.
    * val num1 = 10 : String "10"로 변환 => num1.toString()
    * val str = "1988" : Int 1988 로 변환 => str.toInt()
* 그 외의 클래스
  * as : JAVA의 참조형 변수간의 캐스팅에 대응되는 키워드
    * 변경시킬대상 as 변환해줄 자료형
    * intent.getSerializaleExtra("이름표") as Room
* 참고 사항
  * 코틀린에서는 Double, Int, Sting같은 기본형끼리의 변환은 as를 사용하는게 불가능함

## 코를린에서의 반복문 + ArrayList 개념
* while
  * while
  * for-each 문법을 사용.
* 배열 / ArrayList
  * 일반형 배열 대신 대부분 ArrayList를 활용.
  * ArrayList : 자료구조의 한 종류 => 특징. 저장공간의 크기가 사실상 무제한 + 실제로 등록된 데이터가 몇개인지 확인 가능 - size
  * 코틀린의 for : ArrayList를 가지고 내용물을 하나씩 꺼내보는 형태의 반복.
* 사용법
```kotlin
val mProjects = ArrayList<Project>()

for (p in mProjects) {
    Log.d("프로젝트 제목", p.title)
}
for (i in 0..4) {
    // i에 0, 1, 2, 3, 4가 순서대로 반복
}
for (i in 0 until 5) {
  // i에 0, 1, 2, 3, 4가 순서대로 반복
}
```