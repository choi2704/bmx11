# 주말 훈련 관리 앱

모바일 중심의 팀 공유 웹앱 프로토타입입니다.

## 포함 기능
- 월간 훈련 달력 / 날짜별 시간·장소
- 공지 이미지와 중요내용
- 코치 + 아이 참석상태 (가능 인원은 아이만 계산)
- 댓글
- 회원 명단 추가/삭제
- 날짜별 지출 등록
- 영수증 이미지 첨부
- 전체 입출금 장부 / 잔액 계산
- 아이별 납부관리 화면 자리

## 현재 데이터 저장 방식
현재 버전은 **localStorage 데모**입니다. 같은 브라우저에서는 데이터가 유지되지만 다른 사람과 실시간 공유되지는 않습니다.

실제 팀 운영 버전은 Firebase의 Firestore, Storage, Authentication을 연결해 실시간 공유하도록 확장하면 됩니다.

## 내 컴퓨터에서 실행
Node.js 설치 후:

```bash
npm install
npm run dev
```

## GitHub에 올리기
GitHub에서 새 저장소를 만든 다음 이 폴더에서:

```bash
git init
git add .
git commit -m "Initial training team app"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## 배포
Vite 프로젝트이므로 Firebase Hosting, Vercel, Netlify 등으로 배포할 수 있습니다. GitHub Pages를 사용할 경우 Vite의 base 경로와 GitHub Actions 배포 설정을 추가하는 것을 권장합니다.

## 다음 단계
1. Firebase 프로젝트 생성
2. Firestore: 일정/명단/출석/댓글/납부/회계 데이터
3. Storage: 공지·영수증 이미지
4. Authentication: 사용자 식별
5. 실시간 listener 연결
6. 수정/삭제 이력(감사 로그) 추가
