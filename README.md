# 🧠 Mindary - 감정을 기록하고 마음을 정리하는 다이어리

> **“임금님 귀는 당나귀 귀”처럼, 마음속 이야기를 몰래 털어놓고 정리할 수 있는 감정 기록 서비스**

---

## 🪄 프로젝트 소개

**Mindary**는 2030 현대인을 위한 감정 기록 다이어리입니다.  
바쁜 일상 속에서도 간편하게 감정을 기록하고, 주간·월말 워드클라우드 결산을 통해 **자신의 감정 흐름을 시각적으로 파악**할 수 있어요.

---

## 📌 주요 기능

| 기능 | 설명 |
|------|------|
| 🗓️ 감정 기록 | 엑셀 스타일 UI로 하루의 감정을 간편하게 기록 |
| 🪄 워드클라우드 결산 | 주간/월말 키워드 시각화 제공 |
| 📅 캘린더 기반 습관 챌린지 | 기록 체크 및 성취도 확인 기능 |
| 🔐 카카오 소셜 로그인 | OAuth 기반 로그인 구현 |
| 🔍 아카이브 페이지 | 작성한 기록 검색 및 필터링 가능 |

---

## 🔧 리팩토링 포인트

### 🔁 카카오 로그인 에러 해결
- 인가 code를 넘겨 받을 때 프론트엔드와 백엔드 간의 field 명 불일치의 오류 해결
- 최초 카카오 로그인한 자는 회원가입을 진행할 수 있게 로직 수정 
- 카카오 개발자 콘솔의 **도메인 등록**, **access_token 수동 테스트** 등 테스트 케이스 반영

### 🖼️ 결산 이미지 다운로드 개선
- 이전에는 이미지가 없을 경우 404나 서버 에러 발생
- → 이제는 기록이 없는 경우 **HTTP 204 응답과 함께 사용자에게 경고 메시지 표시**
- 파일 경로가 없을 때 자동 생성되도록 처리

---

## 🧠 기술 스택

- **Frontend**: React, Styled-components, Axios
- **Backend**: Django, Django REST Framework, JWT Auth
- **NLP**: krwordrank, WordCloud
- **Infra**: AWS EC2, GitHub

---


## 🧑‍💻 팀원 소개

| 역할 | 이름 |
|------|------|
| 기획 | 진예원 |
| 디자인 | 박소은 |
| 프론트엔드 | 강민석, 원채영 |
| 백엔드 | 김태경, 문덕영 |

---

## 🖼️ 데모 이미지
![image](https://github.com/user-attachments/assets/bc18958b-de46-46a0-a229-3ecea5a401ac)
![image](https://github.com/user-attachments/assets/854e3c17-ecc6-41eb-9feb-1040281fcbe7)

---

## 🗂️ 프로젝트 구조

```bash
Mindary-Refactoring/
├── FRONTEND-refactor/
│   └── ... (React 코드)
├── BACKEND-refactor/
│   └── ... (Django REST API 코드)
└── README.md
