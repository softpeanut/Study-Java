## OOP(Object-Oriented Programming)

##### 객체 지향 프로그래밍이란?

컴퓨터 프로그램을 명령어의 목록으로 보는 시각에서 벗어나 여러 개의 독립된 단위(=객체)들의 모임으로 파악하는 것이다. 

각각의 객체는 메시지를 주고받고, 데이터를 처리할 수 있다.

## Class

##### Class란?

객체를 정의하는 틀 또는 설계도와 같은 의미이다. 이러한 클래스를 가지고 여러 객체를 생성하여 사용한다. 

클래스는 객체의 상태를 나타내는 필드와 객체의 행동을 나타내는 메소드로 구성된다.

###### 필드 :  클래스에 포함된 변수

###### 메소드 : 어떠한 특정 작업을 수행하기 위한 명령문의 집합

## 객체와 인스턴스의 차이

- ##### 객체 : 클래스에 선언된 모양 그대로 생성된 실체

- ##### 인스턴스 : 객체를 소프트웨어에 실체화 한 것

객체는 모든 인스턴스를 대표하는 포괄적인 의미를 갖는다.

인스턴스라는 용어는 반드시 클래스와 객체 사이의 관계로 한정지어서 사용할 필요는 없다.

인스턴스는 원본으로부터 생성된 복제본을 의미한다.

```
public class Animal {
  ...
}
// 객체와 인스턴스
public class Main {
  public static void main(String[] args) {
    Animal tiger, lion;
    tiger = new Animal();
    lion = new Animal();
  }
}
```

## 접근 제한자

##### 접근 제한자란?

하나의 객체가 다른 객체에 접근하려고 하거나 상속관계에서 상위 클래스가 하위 클래스에게 얼마나 많은 정보에 접근을 시킬지 접근 정도를 표시할 때 사용된다.

- public : 패키지, 클래스가 동일하지 않아도 모든 접근이 가능한 제한자이다.

  > 모든 접근이 가능하다.

- protected : 같은 패키지에서만 접근을 허용하고 다른 패키지에서 접근하려면 해당 클래스를 상속받을 시에만 접근이 가능한 제한자이다.

  > 같은 패키지 내부에 있는 클래스, 하위 클래스(상속받은 경우)에서 접근이 가능하다.

- default : 접근 제한자를 적지 않으면 default 접근 제한자이다.

  > 자동으로 선언되어 지므로 변수, 메소드 앞에 명시적으로 적으면 안된다.
  >
  > 같은 패키지 내에서만 접근이 가능하다.

- private : 동일 패키지, 다른 패키지 모두 접근이 불가능하고 같은 클래스 내에서만 접근을 허용하는 제한자이다.

  > 같은 클래스 내에서만 접근이 가능하다.

## 생성자

##### 생성자란?

객체가 객체화 될 때 호출되는 특수 함수, 새 키워드를 사용할 때 자바 생성자의 목적은 새로 생성된 객체를 쓰기 전에 초기화하는 것이다.

##### 생성자의 특징

생성자는 해당 클래스의 객체를 초기화한다. 일반적으로 생성자는 초기화가 필요한 객체의 필드를 초기화한다. 

1. 클래스명과 동일하다.
2. 결과형 리턴값을 가지지 않는다. (void도 사용안함)
3. 클래스 객체가 생성될 때 반드시 하나의 생성자가 호출된다.
4. 멤버 필드의 값을 초기화 한다. 
5. 하나의 클래스 내부에 생성자가 하나도 없으면 default 생성자가 있는 것으로 간주한다.
6. 하나의 클래스에는 매개 변수의 개수와 자료형이 틀린 생성자들을 여러개 만들 수 있다.
7. 생성자의 첫번째 라인으로 this(매개변수) 생성자를 사용하여 또 다른 생성자 하나를 호출할 수 있다.

## new 키워드

##### new 키워드란?

new는 클래스 타입의 객체를 생성해주는 역할을 담당한다. new 키워드를 통해 메모리에 데이터를 저장할 공간을 할당받고 그 공간의 참조값을 객체에게 반환하여 주고 이어서 생성자를 호출하게 된다.

![img](http://postfiles16.naver.net/MjAxNzAzMTFfOTMg/MDAxNDg5MTYyNjE4NzMw.nJSpcbg3xVNe4lVU_KGM15y1yjySr5eREgRABPi38_8g.kOeoQY8MXUaDEC5x4fXjgi9Qma0M-yHTD0P-_VqiW20g.PNG.heartflow89/image.png?type=w773)

