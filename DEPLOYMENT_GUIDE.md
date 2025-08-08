# 배포 가이드 (GitHub + Vercel)

## 1. GitHub 저장소 생성

1. [GitHub](https://github.com)에 로그인합니다
2. 우측 상단의 "+" 버튼을 클릭하고 "New repository"를 선택합니다
3. 저장소 이름을 입력합니다 (예: `vocabulary-app`)
4. "Public" 또는 "Private"을 선택합니다
5. "Create repository"를 클릭합니다

## 2. 로컬에서 Git 초기화 및 푸시

터미널에서 다음 명령어들을 실행합니다:

```bash
# Git 초기화
git init

# 모든 파일을 스테이징
git add .

# 첫 번째 커밋
git commit -m "Initial commit: 단어장 앱"

# GitHub 원격 저장소 추가 (YOUR_USERNAME과 REPO_NAME을 실제 값으로 변경)
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 메인 브랜치로 푸시
git branch -M main
git push -u origin main
```

## 3. Vercel 배포

### 방법 1: Vercel 웹사이트에서 배포

1. [Vercel](https://vercel.com)에 로그인합니다 (GitHub 계정으로 로그인 가능)
2. "New Project"를 클릭합니다
3. GitHub 저장소를 선택합니다
4. 프로젝트 설정을 확인하고 "Deploy"를 클릭합니다

### 방법 2: Vercel CLI 사용

```bash
# Vercel CLI 설치
npm install -g vercel

# 프로젝트 디렉토리에서 배포
vercel

# 프롬프트에 따라 설정:
# - GitHub 계정 연결
# - 프로젝트 이름 설정
# - 배포 설정 확인
```

## 4. 배포 후 설정

1. Vercel 대시보드에서 배포된 URL을 확인합니다
2. 필요시 커스텀 도메인을 설정할 수 있습니다
3. 환경 변수가 필요한 경우 Vercel 대시보드에서 설정합니다

## 5. 자동 배포

- GitHub 저장소에 변경사항을 푸시하면 Vercel이 자동으로 재배포합니다
- 각 커밋마다 새로운 배포가 생성됩니다

## 6. 문제 해결

### 배포가 실패하는 경우:
1. `vercel.json` 파일이 올바른지 확인
2. 모든 파일이 GitHub에 푸시되었는지 확인
3. Vercel 로그에서 오류 메시지 확인

### 파일이 제대로 로드되지 않는 경우:
1. 파일 경로가 올바른지 확인
2. CSS/JS 파일의 상대 경로 확인
3. 브라우저 개발자 도구에서 네트워크 탭 확인

## 7. 추가 최적화

- 이미지 최적화
- CSS/JS 압축
- 캐싱 설정
- CDN 활용

이러한 설정들은 Vercel 대시보드에서 추가로 구성할 수 있습니다.
