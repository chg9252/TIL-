회사에서 프로젝트를 통합하고 고도화하는 과정에서
기존의 빌드인 Maven을 Gradle로 바꿨다.
<br>현업의 여러 개발자분들도 gradle이 생소하다 했는데 이 참에
maven과 gradle의 차이점을 찾아봤다.
<br>지금까지 당연하게 maven이라는 빌드 관리도구를 사용했었는데 이 기회에 좀 더 알아보고자 한다.
 

## 빌드 관리 도구(Build Tool)

프로그래밍의 빌드: 소스코드 파일들을 컴퓨터에서 실행할 수 있는 소프트웨어로 변환하는 과정으로, 컴파일, 이진코드화, 테스팅, 배포, 등 모든 과정의 집합이다. 빌드 도구는 이러한 빌드 과정을 '자동'으로 수행해주는 도구를 의미한다


## maven이란
프로젝트를 진행하면서 사용할 수많은 라이브러리들을 관리해주는 자바용 빌드도구이다.
### 특징:
라이브러리들과 연관된 라이브러리들까지 거미줄처럼 다 연동이 되어서 관리가 용이하다.
<br>LifeCycle: 정해진 Lifecycle에 의하여 작업을 수행하며, 전반적인 프로젝트 관리 기능을 포함하고 있다.
<br>프로젝트 모델링: Maven은 필요한 라이브러리를 pom.xml에 정의한다.
<br>플러그인을 통한 전역적인 재사용: Maven은 빌드에 대한 대부분의 책임을 각 플러그인에 위임한다.
<br>이러한 플러그인들은 Maven저장소(Repository)에 저장되어 진다

### POM - Project Object Model
Maven의 기능을 이용하기 위해 POM이 사용된다.
<br>POM은 약자 이름 그대로 Project Object Model의 정보를 담고 있는 파일이다.

<br>pom.xml에서 주로 다루는 기능들.
<br>프로젝트 정보 : 프로젝트의 이름, 라이센스 등
<br>빌드 설정 : 소스, 리소스, 라이프사이클별 실행한 플로그인 등 빌드와 관련된 설정
<br>빌드 환경 : 사용자 환경 별로 달라질 수 있는 프로파일 정보
<br>pom 연관 정보 : 의존 프로젝트(모듈), 상위 프로젝트, 포함하고 있는 하위 모듈 등

```

 <dependencies>
	<dependency>
	    <groupId>org.apache.tomcat</groupId>
	    <artifactId>tomcat-api</artifactId>
	    <version>10.0.18</version>
	</dependency>
	
	<!-- https://mvnrepository.com/artifact/org.springframework/spring-webmvc -->
	<dependency>
	    <groupId>org.springframework</groupId>
	    <artifactId>spring-webmvc</artifactId>
	    <version>5.3.16</version>
	</dependency>
 </dependencies>
```
<br><br><br>

## gradle이란?
Groovy를 기반으로 한 오픈소스 빌드 도구이다. Ant의 자유도와 Maven의 관례를 통한 접근성을 바탕으로 이전 빌드툴의 단점을 보완하여 개선된 서비스를 제공한다.

### 특징:
Ant처럼 매우 유연한 범용 빌드 도구.
<br>Maven과 같은 구조화 된 build프레임워크 (구조의 전환이 가능).
<br>Maven, Ivy등의 기존 저장소 인프라 또는 pom.xml 파일과 ivy.xml 파일에 대한 migration의 편이성 제공
<br>멀티 프로젝트 빌드 지원.
<br>의존성 관리의 다양한 방법 제공
Build script를 xml이 아닌 Groovy 기반의 DSL(Domain Specific Language)을 사용
<br>기존 Build를 구성하기 위한 풍부한 도메인 모델 제공.
<br>Gradle 설치 없이 Gradle Wrapper를 이용하여 빌드 지원

Ant, Maven과 같은 기존의 빌드툴은 xml형식을 이용하여 정적인 설정정보를 구성했다.
<br>Gradle은 Groovy라는 언어를 이용하여 코드로서 설정정보를 구성하기 때문에 구조적인 장점이 있다.

<br><br><br>

참고: https://galid1.tistory.com/194<br>
https://velog.io/@alicesykim95/Maven%EA%B3%BC-Gradle%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90<br>
https://dev-coco.tistory.com/65<br>
https://okky.tistory.com/179<br>
https://wangmin.tistory.com/50<br>
http://wiki.gurubee.net/display/SWDEV/Maven+Lifecycle<br>
