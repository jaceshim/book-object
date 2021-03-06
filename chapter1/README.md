# 프로그래밍 패러다임
## p3
* 우리가 사용하는 패러다임은 '한 시대의 사회 전체가 공유하는 이론이나 방법, 문제의식 등의 체계'를 의미한다 
* 과학혁명이란 과거의 패러다임이 새로운 패러다임에 의해 대체됨으로써 정상과학의 방향과 성격이 변하는것을 의미한다. 이를 패러다임 전환(Paradigm Shift)이라고 부른다.

## p4
* 프로그래밍패러다임은 특정 시대의 어느 성숙한 개발자 공동체에 의해 수용된 프로그래밍 방법과 문제 해결 방법, 프로그래밍 스타일이라고 할 수 있다. 

## p6
* 하나 이상의 패러다임을 수용하는 언어를 다중패러다임 언어(Multiparadigm Language)라고 부른다 

# 객체, 설계

## p14
* 모듈이란 크기와 상관 없이 클래스나 패키지, 라이브러리와 같이 프로그램을 구성하는 임의의 요소를 의미한다. 로버트 마틴(Robert C. Martin) 
* 모든 소프트웨어 모듈에는 세 가지 목적이 있다
  * 실행 중에 제대로 동작하는것
  * 변경을 위해 존재하는 것
  * 코드를 읽는 사람과 의사소통하는 것 
* 마틴에 따르면 모든 모듈은 제대로 실행돼야 하고, 변경이 용이해야 하며, 이해하기 쉬워야 한다 

## p15
* 이해 가능한 코드란 그 동작이 우리의 예상에서 크게 벗어나지 않는 코드다 

## p17
* 객체 사이의 의존성이 과한 경우를 가리켜 __결합도(coupling)__ 가 높다고 말한다. 
* 결합도는 의존성과 관련돼 있기 때문에 결합 역시 변경과 관련이 있다

## p20
* 개념적이나 물리적으로 객체 내부의 세부적인 사항을 감추는 것을 __캡슐화(encapsulation)__ 라고 부른다. 캡슐화의 목적은 변경하기 쉬운 객체를 만드는 것이다. 캡슐화를 통해 객체 내부로의 접근을 제안하면 객체와 객체 사이의 결합도를 낮출 수 있기 때문에 설계를 좀더 쉽게 변경할 수 있게된다

## p21
* 객체를 인터페이스와 구현으로 나누고 인터페이스만을 공개하는 것은 객체 사이의 결합도를 낮추고 변경하기 쉬운 코드를 작성하기 위해 따라야 하는 __가장 기본적인 설계 원칙__ 이다 

## p25
* 캡슐화와 응집도의 핵심은 객체 내부의 상태를 캡슐화하고 객체 간에 오직 메세지를 통해서만 상호작용하도록 만드는 것이다 

## p26
* 밀접하게 연관된 작업만을 수행하고 연관성 없는 작업은 다른 객체에게 위임하는 객체를 가리켜 __응집도(cohesion)__ 가 높다고 한다 
* 객체의 응집도를 높이기 위해서는 객체 스스로 자신의 데이터를 책임져야 한다
* 객체는 자신의 데이터를 스스로 처리하는 자율적인 존재여쟈 한다. 그것이 객체의 응집도를 높이는 첫걸음이다
* 프로세스와 데이터를 별도의 모듈에 위치시키는 방식을 __절차 지향적 프로그래밍(Procedural Programming)__ 이라고 부른다
* 모든 처리가 하나의 클래스 안에 위치하고 나머지 클래스는 단지 데이터의 역할만 수행하기 때문
* 일반적으로 절차적 프로그래밍은 우리의 직관에 위해된다
* 더 큰 문제는 절차적 프로그래밍의 셍상에서는 데이터의 변경으로 인한 영향을 지역적으로 고립시키기 어렵다는 것이다 

## p27
* 절차적 프로그래밍은 프로세스가 필요한 모든 데이터에 의존해야 한다는 근본적인 무넺점 때문에 변경에 취약할 수 밖에 없다 
* 데이터와 프로세스가 동일한 모듈 내부에 위치하도록 프로그래밍하는 방식을 __객체지향 프로그래밍(Object-Oriented Programming)__ 이라고 부른다 
* 훌륭한 객체지향 설계의 핵심은 캡슐화를 이용해 의존성을 적절히 관리함으로써 객체 사이의 결합도를 낮추는 것이다
* 두 방식 사이에 근본적인 차이를 만드는 것은 __책임의 이동(shift of responsibility)[Shalloway01]이다. 여기서 책임을 기능을 가리키는 객체지향 세계의 용어로 생각해도 무방하다.

## p28
* 코드에서 데이터와 데이터를 사용하느 프로세스가 별도의 객체에 위치하고 있다면 절차적 프로그래밍 방식을 따르고 있을 확률이 높다 

## p29
* 객체가 어떤 데이트를 가지느냐보다는 객체에 어떤 책임을 할당할 것이냐에 초점을 맞춰야 한다 
* 설계를 어렵게 만드는 것은 __의존성__ 이라는 것을 기억하라. 해결 방법은 불필요한 의존성을 제거함으로써 객체 사이의 __결합도__ 를 낮추는 것이다.
* 객체 내부로 캡슐화하는 것은 객체의 __자율성__ 을 높이고 __응집도__ 높은 객체들의 공동체를 창조할 수 있게 한다 

## p33
* 어떤 기능을 설계하는 방법은 한 가지 이상일 수 있다
* 동일한 기능을 한 가지 이상의 방법으로 설계할 수 있기 때문에 결국 설계는 트레이드오프의 산물이다 
* __설계는 균형의 예술이다 훌륭한 설계는 적절한 트레이드오프의 결과물이라는 사실을 명심하라__
* 현실에서는 수동적인 존재라고 하더라도 일단 객체지향의 세계에 들어오면 모든 것이 능동적이고 자율적인 존재로 바뀐다. 레베카 워프스브록(Rebecca Wirfs-Brock)은 이처럼 능동적이고 자율적인 존재로 소프트웨어 객체를 설계하는 원칙을 가리켜 __의인화(anthropomorphism)__ 부른다 


## p34
* 일상적인 체계에서는 어떤 사건이 일어나기 위해 반드시 인간 에이전트가 필요한 반면 객체들은 그들 자신의 체계 안에서 [능동적이고 자율적인] 에이전트다.[Wirfs-Brock90]
* 설계란 코드를 배치하는 것이다 [Metz12]

## p35
* 우리가 짜는 프로그램은 두 가지 요구사항을 만족시켜야 한다. 우리는 오늘 완성해야 하는 기능을 구현하는 코드를 짜야 하는 동시에 내일 쉽게 변경할 수 있는 코드를 짜야한다[Metz12] 좋은 설계란 오늘 요구하는 기능을 온전히 수행하면서 내일의 변경을 매끄럽게 수용 할 수 있는 설계다.
* 변경을 수용할 수 있는 설계가 중요한 또 다른 이유는 코드를 변경할 때 버그가 추가될 가능성이 높기 때문이다.

## p36
훌륭한 객체지향 설계란 협력하는 객체 사이의 의존성을 적절하게 관리하는 설계다.

