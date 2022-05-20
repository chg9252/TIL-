회사에서 프로젝트를 통합하고 고도화하는 과정에서
기존의 빌드인 Maven을 Gradle로 바꿨다.
현업의 여러 개발자분들도 gradle이 생소하다 했는데 이 참에
maven과 gradle의 차이점을 찾아봤었다.
지금까지 당연하게 maven이라는 빌드 관리도구를 사용했는데 잘됐다
 

## 빌드 관리 도구(Build Tool)

프로그래밍의 빌드: 소스코드 파일들을 컴퓨터에서 실행할 수 있는 소프트웨어로 변환하는 과정으로, 컴파일, 이진코드화, 테스팅, 배포, 등 모든 과정의 집합이다. 빌드 도구는 이러한 빌드 과정을 자동으로 수행해주는 도구를 의미한다


## maven이란
프로젝트를 진행하면서 사용할 수많은 라이브러리들을 관리해주는 자바용 빌드도구이다.
### 특징:
라이브러리들과 연관된 라이브러리들까지 거미줄처럼 다 연동이 되어서 관리가 용이하다.
LifeCycle: 정해진 Lifecycle에 의하여 작업을 수행하며, 전반적인 프로젝트 관리 기능을 포함하고 있다.
프로젝트 모델링: Maven은 필요한 라이브러리를 pom.xml에 정의한다.
플러그인을 통한 전역적인 재사용: Maven은 빌드에 대한 대부분의 책임을 각 플러그인에 위임한다. 이러한 플러그인들은 Maven저장소(Repository)에 저장되어 진다

POM - Project Object Model
Maven의 기능을 이용하기 위해 POM이 사용된다.
POM은 약자 이름 그대로 Project Object Model의 정보를 담고 있는 파일이다.
pom.xml에서 주로 다루는 기능들.
프로젝트 정보 : 프로젝트의 이름, 라이센스 등
빌드 설정 : 소스, 리소스, 라이프사이클별 실행한 플로그인 등 빌드와 관련된 설정
빌드 환경 : 사용자 환경 별로 달라질 수 있는 프로파일 정보
pom 연관 정보 : 의존 프로젝트(모듈), 상위 프로젝트, 포함하고 있는 하위 모듈 등




참고: https://galid1.tistory.com/194
https://velog.io/@alicesykim95/Maven%EA%B3%BC-Gradle%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90
https://dev-coco.tistory.com/65
https://okky.tistory.com/179
https://wangmin.tistory.com/50
http://wiki.gurubee.net/display/SWDEV/Maven+Lifecycle
