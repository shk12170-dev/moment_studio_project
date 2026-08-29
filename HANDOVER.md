# 과제 5 인수인계 문서 (HANDOVER)

- **저장소 버전 ID (Commit/Version)**: v1.0.0-a-handover
- **작업 일시**: 2026-08-28 16:00 (KST)

---

### 1. 목표
웹 응용 프로그램(Moment Studio)의 인라인 코드/이벤트를 제거하고, CSP(Content Security Policy) 준수 구조로 리팩토링하여 XSS 및 외부 리소스 보안을 강화한다.

### 2. 현재 상태
- `index.html`, `style.css`, `app.js` 3개 파일로 분리 완료.
- 인라인 `onclick`, `onchange` 및 인라인 `<style>` 완전 제거됨.
- Canvas `fillText()` 사용으로 DOM XSS 위험성 방어 확인됨.

### 3. 실행 명령
```bash
# 로컬 라이브 서버 실행 (Node.js http-server 예시)
npx http-server . -p 8080
# 브라우저 접속: http://localhost:8080/index.html