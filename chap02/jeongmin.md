# 2장

## 의존성 주입

스프링이란 오픈 소스의 경량 프레임워크다.

스프링 프레임워크에는 여러 가지 컴포넌트가 존재한다.

-AOP, ORM, 스프링 웹

스프링워크의 핵심을 한 단어로 표현한다면, 의존성 주입을 말할 수 있다.

한 오브젝트가 의존하는 오브젝트를 생성하는 것이 아니라 외부에서 넘겨받는 것을 의존성 주입이라고 한다.

이런 의존성 주입을 아주 전문적으로 해주는 것이 의존성 주입 컨테이너이고, 그 의존성 주입 컨테이너 중 하나가 바로 스프링 프레임 워크이다.

## @SpringBootApplication

이 어노테이션은 해당 클래스가 스프링 부트를 설정하는 클래스임을 의미한다.

해당 어노테이션이 달린 클래스가 있는 패키지를 베이스 패키지로 간주한다.

스프링은 베이스 패키지와 그 하위 페키지에서 자바 빈을 찾아 스프링의 의존성 주입 컨테이너 오브젝트 즉, ApplicationContext에 등록한다. 그리고 애플리케이션 실행 중 어떤 오브젝트가 필요한 경우 의존하는 다른 오브젝트를 찾아 연결해준다.

@Autowired

: 자동으로 다른 오브젝트를 찾아 연결

@Component

: 스프링에게 이 클래스를 자바 빈으로 등록시키라고 알려주는 어노테이션 이다.

@Bean

: @component 를 추가하지 않고 스프링을 통해 빈을 관리할때 사용

lombok

## 레이어드 아키텍처

애플리케이션을 구성하는 요소들을 수평으로 나눠 관리하는 것이다.

## 모델, 엔티티

## DTO

Data Transfer Object 

- 비즈니스 로직을 캡슐화 하기 위하여 사용
- 클라이언트가 필요한 정보를 모델이 전부 포함하지 않은 경우가 많아 사용
    
    ex) 에러메시지가 필요한 경우 DTO 에 추가하여 사용
    

## REST API

Representational State Transfer의 약자로 아키텍처 스타일이다.

아키텍처 패턴 : 어떤 반복되는 문제 상황을 해결하는 도구 

아키텍처 스타일 : 반복되는 아키텍처 디자인을 의미

REST 제약조건 

- Client - Server
- Stateless : 클라이언트가 서버에 요청을 보낼 때 이전 요청의 영향을 받지 않음
- Cacheable Data
- Uniform Interface
- Layered System
- Code-On-Demand

컨트롤러 레이어 : 스프링 REST API 컨트롤러

HTTP는 GET / POST / PUT / DELETE / OPTIONS 등과 같은 메서드와 URI를 이용해 서버에 요청을 보낸다.

## ResponseEntity

## 서비스 레이어 : 비즈니스 로직

서비스 레이어는 컨트롤러와 퍼시스턴스 사이에서 비즈니스 로직을 수행하는 역할을 한다.

## 퍼시스턴스 레이어 : 스프링 데이터 JPA

Todo 아이템을 데이터베이스에 저장 → 관계형 데이터베이스 → 데이터베이스 클라이언트 설치

(클라이언트는 데이터베이스에 연결하는 작업을 도와준다)

이렇게 쿼리한 결과를 자바 애플리케이션 내에서 사용하려면, JDBC를 사용해야 한다.

JDBC 드라이버는 자바에서 데이터베이스에 연결할 수 있도록 도와주는 라이브러리다.

**데이터베이스와 스프링 데이터 JPA 설정**

H2는 In-Memory 데이터베이스로 로컬환경에서 메모리상에 데이터베이스를 구축해 준다.
