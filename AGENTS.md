# 📦 AR Korea WMS 프론트엔드 배포 지침서 (AGENTS.md)

본 저장소는 **AR Korea WMS의 독립 웹 프론트엔드(GitHub Pages 호스팅)** 저장소입니다.

---

### 1. 서비스 정보
* **배포 URL**: `https://hayulthegoat.github.io/gs-wms-html/`
* **로컬 Herd 주소**: `http://gs-wms-html.test`
* **목적**: 
  1. 구글 상단 경고 배너 없는 깨끗한 단독 화면 제공
  2. 카카오톡 단톡방 및 외부 공유용 무료 고속 호스팅 (VPS 트래픽 0원)

---

### 2. 구글 시트 실시간 데이터 연동
* 프론트엔드는 구글 Apps Script의 API(`?action=dashboard`)를 통해 실시간 수불 데이터를 JSON으로 가져옵니다.
* 주소 뒤에 `?api=구글_웹앱_URL`을 입력하면 브라우저 `localStorage`에 영구 저장되어 이후 접속 시 자동 연동됩니다.

---

### 3. 로그인 보안 제어
* `index.html` 내 `loginRequired` 변수:
  * `loginRequired: false` : 로그인 없이 누구나 즉시 열람 (기본값)
  * `loginRequired: true` : 아이디/비밀번호 인증 모달 활성화 (`arkorea` / `ark03614*`)
