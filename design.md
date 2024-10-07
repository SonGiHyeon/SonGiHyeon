## 문제점

탄소배출권 거래가 투명하지 못하고, 나라마다 다른 통화 문제점

## 해결책

블록체인에서 거래를 하며 투명하게 기록하고, 공통 토큰으로 결제를 함

## 구조도

![image](https://github.com/user-attachments/assets/62494a62-bf9f-415c-b653-3caa9e4e5182)


## 흐름도

- 메인 페이지 접속 → 처음 오게 되면 회원가입, 회원가입이 되어있는 사용자는 로그인
- 로그인 완료한 사용자는 탄소 배출량 조회, 거래 시작, 거래 내역 조회 기능을 사용할 수 있다
- 탄소 배출량 조회: 주요 6국가에 대해서 전일대비 탄소 배출량이 얼마나 변했는지 확인할 수 있다
- 거래 시작: 거래창에서는 사용자가 자신의 국가리를 선택하고 배출권을 얼마나 구매할 지 결정한다
- 거래 내역 조회: 거래창에서 제출 버튼을 누르면 그 정보가 거래 내역에 그대로 나타난다

![image](https://github.com/user-attachments/assets/4f2d595f-214b-4511-b1bf-a6097eecd2fe)


## 디자인

(피그마 or PPT 도형)

- 메인 페이지

![image](https://github.com/user-attachments/assets/8f016fa2-cab2-4f07-a63a-114ff9299832)


- 탄소 배출량 조회

![image](https://github.com/user-attachments/assets/ecfbc96e-b25b-4965-a0a2-103edebc5128)


- 거래창

![image](https://github.com/user-attachments/assets/2d0a875f-e959-428b-bfd6-208efcad2054)


- 거래내역

![image](https://github.com/user-attachments/assets/ba0d2a43-9017-4086-b30e-c91059ad19c5)


- 회원가입

![image](https://github.com/user-attachments/assets/9c1769c2-eda9-4312-88f3-845cf4fdadd9)


- 로그인

![image](https://github.com/user-attachments/assets/79749fab-69a4-44d5-9984-1bf1d4917b48)


- 마이페이지

![image](https://github.com/user-attachments/assets/e36fe735-2140-496b-84bb-4c0884d02456)


## 기능

1. **웹 서버**
    1. 기본적인 웹서비스 제공, 백엔드 담당
2. **사용자 계정 등록/로그인**
    1. 로그인 후 서비스 이용 가능, 백엔드 담당, DB 사용
    2. 메인: `/main`
    3. 회원가입: `/register`
    4. 로그인: `/login`
    5. 마이페이지: `/me`
    
3. **탄소 배출량 조회**
    1. 외부 API로 조회, 백엔드 담당
    2. 탄소 배출량 조회: `/status`
    
4. **탄소 배출권 거래**
    1. 이더리움 네트워크 접근으로 거래, 블록체인 담당
    2. 거래창: `/trade`
5. **거래 내역 확인**
    1. 이더리움 네트워크 접근으로 조회, 블록체인 담당
    2. 거래내역:  `/transaction history`

## 역할

- **기획자**(1): 서비스 기획
    - 기술 스택: 문서화(markdown), 그림, PPT, Figma(선택)
- **프론트엔드**(2): 기능구현, UI
    - 기술 스택: React or Next.js
- **백엔드**(1): 서버 구축
    - 기술 스택: FastAPI, Python, PostgreSQL
- **블록체인**(1): 네트워크, 프론트엔드 기능구현
    - 기술 스택: js, Ethereum, Solidity

## 계획표

- 1단계: 기획 및 요구사항 정의
- 2단계: 프론트엔드 및 백엔드 초기 개발
- 3단계: 블록체인 통합 및 테스트
- 4단계: 최종 테스트 및 배포
