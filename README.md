# **오픈소스응용프로그래밍 전범위 강의 필기노트**

2024 인하대학교 컴퓨터공학과 전공수업

## **목차**

### [[오픈소스응용프로그래밍] 01. 오픈소스 SW란?](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2001%20%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%20SW%E1%84%85%E1%85%A1%E1%86%AB.md)

- 오픈소스 SW란?
    - 오픈소스 SW
- 저작권과 라이센스
    - 저작권과 라이센스의 차이점
- 독점 소프트웨어와 자유 소프트웨어
    - 독점 소프트웨어
    - 자유 소프트웨어(Free SW)
        - GNU 프로젝트
        - 자유 소프트웨어의 원칙
- Copyleft 라이선스
    - GPL 라이선스
    - LGPL 라이선스
- Open Source
    - Permissive 라이선스
- FOSS
    - FOSS의 장점
- 공개 도메인 SW

### [[오픈소스응용프로그래밍] 02. Git 소개 및 버전 관리](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2002%20Git%20%E1%84%89%E1%85%A9%E1%84%80%E1%85%A2%20%E1%84%86%E1%85%B5%E1%86%BE%20%E1%84%87%E1%85%A5%E1%84%8C%E1%85%A5%E1%86%AB.md)

- Git 소개 및 버전 관리
    - Git 소개
    - Git과 GitHub
        - Git과 GitHub의 차이
    - Git을 사용하면 유리한 점
        - 버전관리
        - 백업
        - 협업
- Git 버전 관리
    - Git이 저장소를 관리하는 방법
        - Working tree
        - Stage
        - Repository
    - Stage 공간의 필요성
        - 수정된 부분 중 일부분만 commit 가능
        - commit 전 코드 리뷰 및 테스트 가능

### [[오픈소스응용프로그래밍] 03. 도커 컨테이너](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2003%20%E1%84%83%E1%85%A9%E1%84%8F%E1%85%A5%20%E1%84%8F%E1%85%A5%E1%86%AB%E1%84%90%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%82%E1%85%A5.md)

- 💖 도커 컨테이너
    - 도커 컨테이너
    - 도커 컨테이너의 동작 방식
    - 도커 컨테이너 관련 명령어
        - ⚡ create
        - ⚡ start
        - ⚡ stop
        - ⚡ attach
        - ⚡ rm
        - ⚡ run
    - 컨테이너 모니터링 도구 cAdvisor
    - Nginx

### [[오픈소스응용프로그래밍] 04. 도커의 데이터 관리](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2004%20%E1%84%83%E1%85%A9%E1%84%8F%E1%85%A5%E1%84%8B%E1%85%B4%20%E1%84%83%E1%85%A6%E1%84%8B%E1%85%B5%E1%84%90%E1%85%A5%20%E1%84%80%E1%85%AA%E1%86%AB%EB%A6%AC.md)

- 도커의 데이터 관리
    - 유니언 파일 시스템
- 💖 도커 볼륨
    - 언제 사용하나요?
    - 도커 볼륨 타입
        - Type1: Volume
        - Type2: Bind mount
        - Type3: tmpfs mount
- 💖 Reference

### [[오픈소스응용프로그래밍] 05. 도커 파일](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2005%20%E1%84%83%E1%85%A9%E1%84%8F%E1%85%A5%20%E1%84%91%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AF.md)

- 💖 도커 파일
    - 도커 파일 명령어
        - ⚡ FROM
        - ⚡ RUN
        - - ⚡ WORKDIR
- Buildkit
    - Build kit의 기능
    - Build kit 사용 방법

### [[오픈소스응용프로그래밍] 06. 코드 리뷰](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2006%20%E1%84%8F%E1%85%A9%E1%84%83%E1%85%B3%20%E1%84%85%E1%85%B5%E1%84%87%E1%85%B2.md)

- 💖 코드 리뷰
    - 코드 리뷰, 왜 필요한가요?

### [[오픈소스응용프로그래밍] 07. 디자인 패턴](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2007%20%E1%84%83%E1%85%B5%E1%84%8C%E1%85%A1%E1%84%8B%E1%85%B5%E1%86%AB%20%E1%84%91%E1%85%A2%E1%84%90%E1%85%A5%E1%86%AB.md)

- 💖 디자인 패턴
    - 디자인 패턴이란?
    - 디자인 패턴이 탄생한 배경
        - 소프트웨어 개발에 있어서 경험의 중요성
        - 소프트웨어 설계 지식 공유
    - 디자인 패턴을 사용하면 어떤 점이 좋은가요?
        - 설계 과정의 속도를 높일 수 있습니다.
        - Reusable하고 flexible합니다.
        - 효율적으로 의사소통 할 수 있습니다.
    - 디자인 패턴을 반대하는 목소리들
        - 결국 과거의 반복
        - 과잉 사용
        - 좋은 프로그래밍 언어라면 디자인 패턴이 필요치 않다

### [[오픈소스응용프로그래밍] 08. 객체지향개발](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2008%20%E1%84%80%E1%85%A2%E1%86%A8%E1%84%8E%E1%85%A6%E1%84%8C%E1%85%B5%E1%84%92%E1%85%A3%E1%86%BC%E1%84%80%E1%85%A2%E1%84%87%E1%85%A1%E1%86%AF.md)

- 💖 객체지향개발
    - 추상화 (Abstraction)
    - 캡슐화 (Encapsulation)
    - 상속성 (Inheritance)
        - 상속성을 활용하는 예시: 접근 지정자 확장
        - 주의점
    - 다형성 (Polymorphism)
        - Overloading
        - Overriding
    - 정적 바인딩과 동적 바인딩
        - 정적 바인딩 VS 동적 바인딩

### [[오픈소스응용프로그래밍] 09.SOLID 원칙](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2009%20SOLID%20%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%8E%E1%85%B5%E1%86%A8.md)

- 💖 객체지향설계 원칙
    - SOLID 원칙
    - ⚡ Single Responsibility Principle
        - 예시: 적용 후
        - 예시: 적용 후
    - ⚡ Open Closed Principle
        - 예시: 적용 전
        - 예시: 적용 후
    - ⚡ Liskov Substitution Principle
        - 예시: 적용 전
        - 예시: 적용 후
    - ⚡ Interface Segregation Principle
        - 예시: 적용 전
        - 예시: 적용 후
    - ⚡ Dependency Inversion Principle
        - 예시: 적용 전
        - 예시: 적용 후

### [[오픈소스응용프로그래밍] 10. UML Diagram](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2010%20UML%20Diagram.md)

- 💖 UML
    - UML이란?
    - UML Diagram
        - ⚡ class
        - ⚡ visibility

### [[오픈소스응용프로그래밍] 11. 연관 관계](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2011%20%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%80%E1%85%AA%E1%86%AB%20%E1%84%80%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A8.md)

- ⚡ 연관 관계
    - 💛 양방향 연결 관계
    - 💛 역할이 부여된 연관 관계
    - 💛 다중 연관 관계
    - 💛 단방향 연관 관계
    - 💛 연관 클래스

### [[오픈소스응용프로그래밍] 12. 일반화 관계](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2012%20%E1%84%8B%E1%85%B5%E1%86%AF%E1%84%87%E1%85%A1%E1%86%AB%E1%84%92%E1%85%AA%20%E1%84%80%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A8.md)

- ⚡ 일반화 관계

### [[오픈소스응용프로그래밍] 13. 집합관계와 합성관계](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2013%20%E1%84%8C%E1%85%B5%E1%86%B8%E1%84%92%E1%85%A1%E1%86%B8%E1%84%80%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A8%E1%84%8B%E1%85%AA%20%E1%84%92%E1%85%A1%E1%86%B8%EC%84%B1%EA%B4%80%EA%B3%84.md)

- ⚡ 집합 관계
- ⚡ 합성 관계

### [[오픈소스응용프로그래밍] 14. 의존관계와 실체화관계](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2014%20%E1%84%8B%E1%85%B4%E1%84%8C%E1%85%A9%E1%86%AB%E1%84%80%E1%85%AA%E1%86%AB%E1%84%80%E1%85%A8%E1%84%8B%E1%85%AA%20%E1%84%89%E1%85%B5%E1%86%AF%E1%84%8E%E1%85%A6.md)

- ⚡ 의존 관계
    - 의존 관계와 연관 관계
- ⚡ 실체화 관계
- 💖 References

### [[오픈소스응용프로그래밍] 15. 전략 패턴](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2015%20%E1%84%8C%E1%85%A5%E1%86%AB%E1%84%85%E1%85%A3%E1%86%A8%20%E1%84%91%E1%85%A2%E1%84%90%E1%85%A5%E1%86%AB.md)

- ⚡ 전략 패턴
    - 전략패턴이 필요한 시나리오
    - 문제점
    - 예시: 전략패턴 도입 전
    - 예시: 전략패턴 도입 후

### [[오픈소스응용프로그래밍] 16. 상태 패턴](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2016%20%E1%84%89%E1%85%A1%E1%86%BC%E1%84%90%E1%85%A2%20%E1%84%91%E1%85%A2%E1%84%90%E1%85%A5%E1%86%AB.md)

- ⚡ State 패턴
    - state 패턴이 필요한 시나리오
    - 문제점

### [[오픈소스응용프로그래밍] 17. 테스트의 종류](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2017%20%E1%84%90%E1%85%A6%E1%84%89%E1%85%B3%E1%84%90%E1%85%B3%E1%84%8B%E1%85%B4%20%E1%84%8C%E1%85%A9%E1%86%BC%E1%84%85%E1%85%B2.md)

- 테스트의 단계
    - Test Oracle
    - Test Harness
- 💖 테스팅의 종류
    - 프로그램 실행 여부에 따른 구분
        - ⚡ 동적 테스트
        - ⚡ 정적 테스트
    - 테스트 목적에 따른 분류
        - ⚡ 회복(recovery) 테스트
        - ⚡ 안전(security) 테스트
        - ⚡ 강도(stress) 테스트
        - ⚡ 민감도 테스트(sensitivity test)
        - ⚡ 구조 테스트(structural) 테스트
        - ⚡ 성능(performance) 테스트

### [[오픈소스응용프로그래밍] 18. V모델](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2018%20V%E1%84%86%E1%85%A9%E1%84%83%E1%85%A6%E1%86%AF.md)

- 💖 테스트 단계와 V 모델
    - ⚡ 단위 테스트
    - ⚡ 통합 테스트
    - ⚡ 시스템 테스트

### [[오픈소스응용프로그래밍] 19. 블랙박스 테스팅](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2019%20%E1%84%87%E1%85%B3%E1%86%AF%E1%84%85%E1%85%A2%E1%86%A8%E1%84%87%E1%85%A1%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%90%E1%85%A6%E1%84%89%E1%85%B3%ED%8C%85.md)

- 💖 블랙박스 테스팅
    - 대표적인 블랙 박스 테스팅 기법
    - ⚡ 동등 분할 기법(Equivalence partitioning)
    - ⚡ 경계 값 분석 기법(Boundary value analysis)
    - ⚡ 오류 예측 기법(Error guessing)
    - ⚡ 원인 결과 그래프 기법(Cause-effect graph)

### [[오픈소스응용프로그래밍] 20. 원인-결과 그래프 기법 (Cause-effect graph)](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2020%20%E1%84%8B%E1%85%AF%E1%86%AB%E1%84%8B%E1%85%B5%E1%86%AB-%E1%84%80%E1%85%A7%E1%86%AF%E1%84%80%E1%85%AA%20%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%ED%94%84.md)

- 💖 원인 결과 그래프 기법(Cause-effect graph)
    - 원인 결과 그래프 기법
    - 원인 결과 그래프 기법의 단계
        - 1단계: 프로그램을 적절한 크기로 분할
        - 2단계: 원인과 결과를 찾음
        - 3단계: 원인-결과 그래프 작성
        - 4단계: 그래프에 제한조건을 표시
        - 제한 조건 그래프
        - 5단계: 의사 결정 테이블로 반환
        - 6단계: 테스트 케이스 작성

### [[오픈소스응용프로그래밍] 21. 화이트박스 테스팅](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2021%20%E1%84%92%E1%85%AA%E1%84%8B%E1%85%B5%E1%84%90%E1%85%B3%E1%84%87%E1%85%A1%E1%86%A8%E1%84%89%E1%85%B3%20%E1%84%90%E1%85%A6%E1%84%89%E1%85%B3%ED%8C%85.md)

- 💖 화이트박스 테스팅
    - 블랙박스 테스팅 vs 화이트박스 테스팅
        - 블랙박스 테스팅과 화이트 박스 테스팅의 공통점
- 💖 화이트박스 테스팅 기법들
    - ⚡ 기초 경로 검사(Base path testing)
    - ⚡ 제어 구조 검사
        - 💛 조건 검사
        - 💛 루프 검사
        - 💛 데이터 흐름 검사
    - ⚡ 문장 검증 기능
    - ⚡ 분기 검증 기능
    - ⚡ 조건 검증 기능
    - ⚡ 분기/조건 검증 기능
    - ⚡ 기본 경로 테스트

### [[오픈소스응용프로그래밍] 22. 문장 검증 기준](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2022%20%E1%84%86%E1%85%AE%E1%86%AB%E1%84%8C%E1%85%A1%E1%86%BC%20%E1%84%80%E1%85%A5%E1%86%B7%E1%84%8C%E1%85%B3%E1%86%BC%20%E1%84%80%E1%85%B5%EC%A4%80.md)

- 💖 문장 검증 기준
    - 제어 흐름 그래프
    - 문장 검증 기준이란?
    - 문장 검증 기준 예시
        - 1단계: 코드를 기반으로 제어 흐름 그래프 작성하기
        - 2단계: 가능한 모든 경로 구하기
        - 3단계: 위에서 구한 모든 경로 중 올바른 경로 선택
    - 문장 검증 기능의 문제점

### [[오픈소스응용프로그래밍] 23. 분기 검증 기준](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2023%20%E1%84%87%E1%85%AE%E1%86%AB%E1%84%80%E1%85%B5%20%E1%84%80%E1%85%A5%E1%86%B7%E1%84%8C%E1%85%B3%E1%86%BC%20%E1%84%80%E1%85%B5%E1%84%8C%E1%85%AE%E1%86%AB.md)

- 💖 분기 검증 기준
    - 분기 검증 기준(결정 검증 기준)
    - 분기 검증 기준의 단계
        - 제어 흐름 그래프 그리기
        - 가능한 모든 경로 구하기
        - 분기 검증 기준을 만족하는 경로 선택
    - 분기 검증 기준의 문제
        - 위의 예제에서 or 연산인 경우
        - 위의 예제에서 and 연산인 경우

### [[오픈소스응용프로그래밍] 24. 조건 검증 기능](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2024%20%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%20%E1%84%80%E1%85%A5%E1%86%B7%E1%84%8C%E1%85%B3%E1%86%BC%20%E1%84%80%E1%85%B5%E1%84%82%E1%85%B3%E1%86%BC.md)

- 💖 조건 검증 기준
    - 조건 검증 기준 선정하기
    - 분기/조건 검증 기준

### [[오픈소스응용프로그래밍] 25. 다중 조건 검증 기준](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2025%20%E1%84%83%E1%85%A1%E1%84%8C%E1%85%AE%E1%86%BC%20%E1%84%8C%E1%85%A9%E1%84%80%E1%85%A5%E1%86%AB%20%E1%84%80%E1%85%A5%E1%86%B7%E1%84%8C%E1%85%B3%E1%86%BC.md)

- 💖 다중 조건 검증 기준
    - 다중 조건 검증 기준이란?
    - mask 문제란?
        - and로 연결된 개별 조건식에서의 마스크 문제
        - or로 연결된 개별 조건식에서의 마스크 문제 해결 방법

### [[오픈소스응용프로그래밍] 26. 기본 경로 테스트](https://github.com/eeeemune/Lecture-note-OpenSourceSoftwareApplication/blob/main/%5B%E1%84%8B%E1%85%A9%E1%84%91%E1%85%B3%E1%86%AB%E1%84%89%E1%85%A9%E1%84%89%E1%85%B3%E1%84%8B%E1%85%B3%E1%86%BC%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%84%86%E1%85%B5%E1%86%BC%5D%2026%20%E1%84%80%E1%85%B5%E1%84%87%E1%85%A9%E1%86%AB%20%E1%84%80%E1%85%A7%E1%86%BC%E1%84%85%E1%85%A9%20%E1%84%90%E1%85%A6%E1%84%89%E1%85%B3%E1%84%90%E1%85%B3.md)

- 💖 기본 경로 테스트
    - 기본 경로 테스트란?
    - 기본 경로 테스트의 단계
        - 순서도 작성
        - 흐름 그래프 작성
        - 순환 복잡도 계산
        - 독립적 경로 정의
        - 테스트 케이스 작성
