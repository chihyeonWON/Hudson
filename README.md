# Hudson
빌드 자동화 CI(Continuous Integration:지속적 통합) 도구인 허드슨의 사용법 공부

## 지속적 통합 - CI도구

많은 개발자들은 빌드를 수행하기 위해 수동으로 작업하는 경우가 많은데 버전관리 시스템에 커밋, 체크아웃, 빌드, 테스트 등을 자동화하는 기능을 제공하는 것이 바로 CI도구 이다.   
CI(Continuous Integration: 지속적 통합)이란 여러 명으로 구성된 팀이 작업한 것을 자주(각 팀원이 하루에 한 번 이상, 매일 여러 번) 통합하는 것을 가리키는 소프트웨어 개발 단계로 개발자, 버전관리 저장소, 통합 빌드 머신 등으로 구성된다.   
지속적 통합 툴로는 Hudson, CruiseControl, Jenkins, Bamboo, TeamCity 등이 있다.   
CI 도구를 이용하면 여러 가지 프로젝트의 빌드를 자동화하고, 그 현황을 한눈에 살펴볼 수 있고, 빌드 상태나 JUnit 테스트 결과 등을 통합하여 자신이 원하는 형태로 생성해 볼 수 있다.

## 허드슨 개념

허드슨(Hudson)은 오픈소스 CI 서버로 소스 빌드 스크립트를 사용한 자동 빌드 및 빌드 결과를 개발자에게 피드백하는 메커니즘을 제공한다.   
허드슨의 중요한 기능 몇가지만 알아본다.
1. 소프트웨어 자동 빌드가 가능하다. 빌드 주기에 따른 일일 빌드 또는 주간 빌드 기능을 제공한다.
2. 지속적이고 자동화된 빌드 검증, 빌드 테스트가 가능하다.
3. 빌드 후속 절차 자동화가 가능하다. 컴파일된 코드의 패키징 및 테스트 리포팅 기능을 제공한다.
4. 빌드 결과 및 테스트 결과를 보여주는 대시 보드 기능을 제공한다.
5. JUnit 테스트 리포트나 코드 인스펙션 도구인 PMD 플러그인을 제공하며 연동을 통해 리포트를 제공한다.

허드슨에서는 플러그인을 사용하여 수많은 도구들과 연동할 수 있다.  
주로 사용하는 것을 정리하면 다음과 같다.

1. JUnit 테스트 연동 : JUnit 테스트 리포트를 출력, 테스트의 Progress 누적 그래프를 출력
2. 코드 인스펙션 및 정적 코드 분석 도구 연동 : Checkstyle, PMD, Findbugs 등
3. 테스트 리포트 코드 커버리지 도구 연동 : TestNG, Cobertura, Clover
4. 빌드 도구 연동 : Maven, Ant, Gradle 등
5. 형상관리 도구 연동 : Git, SVN, ClearCase, Dimensions, Bazaar, Mercurial, Bitkeeper, Harvest, PVCS 등
6. 이슈트래킹 시스템 (ITS : Issue Tracking System) 연동 : Redmine, JIRA 등
7. 웹 애플리케이션 서버 연동 : Tomcat, JBoss, Glassfish, WebSphere, FTP, SSH 등
8. 결과 보고와 피드백 : E-mail, Twitter, Jabber, IRC, RSS, Google calendar 등
