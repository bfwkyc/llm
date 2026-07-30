Git 초기 세팅.md좋은 질문이에요 👍  
앞서 겪으신 문제(브랜치 충돌, 파일 인코딩 깨짐 등)는 사실 **Git/GitHub 초기 세팅**을 올바르게 해두면 대부분 예방할 수 있습니다. 처음부터 안전하게 세팅하는 방법을 단계별로 정리해드릴게요.  

---

# 📌 Git/GitHub 초기 세팅 가이드

---
## 2. 저장소 생성
1. **GitHub에서 새 저장소 생성**  
   - 옵션에서 `Add a README file` 체크 → 원격 저장소에 기본 커밋이 생깁니다.  
   - 기본 브랜치는 `main`으로 자동 설정됩니다.  

2. **로컬에서 프로젝트 초기화**  
   ```bash
   git init
   ```
   - 로컬에 `.git` 폴더가 생깁니다.  

---

## 3. 원격 저장소 연결
```bash
git remote add origin https://github.com/사용자명/저장소명.git
git remote -v
```
- `origin`이라는 이름으로 GitHub 저장소 연결  
- 확인용으로 `git remote -v` 실행  

---

## 4. 브랜치 이름 맞추기
GitHub 기본 브랜치가 `main`이므로 로컬도 `main`으로 맞추는 게 안전합니다:
```bash
git branch -M main
```

---

## 5. 초기 Pull (히스토리 맞추기)
GitHub에 README가 이미 있으므로 먼저 가져옵니다:
```bash
git pull origin main --allow-unrelated-histories
```
- 원격과 로컬 히스토리를 강제로 병합  
- 충돌이 나면 수정 후 커밋  

---

## 6. 작업 흐름
1. 파일 수정  
2. 스테이징  
   ```bash
   git add .
   ```
3. 커밋  
   ```bash
   git commit -m "메시지 작성"
   ```
4. 푸시  
   ```bash
   git push -u origin main
   ```

---

## 7. 파일 이름 주의
- 한글 파일명은 로컬 환경에 따라 깨질 수 있으므로 **영문 파일명**을 권장합니다.  
- 예: `git 연결 관련 과정.md` → `git-process.md`  

---

## ✅ 이렇게 하면
- 브랜치 충돌 방지 (`main`으로 통일)  
- 원격 초기 커밋과 로컬 커밋 병합 문제 해결  
- 파일 이름 깨짐 문제 예방  

---

👉 CM님, 제가 이 과정을 **“Git 초기 세팅.md” 문서**로 정리해서 바로 저장할 수 있게 만들어드릴까요?