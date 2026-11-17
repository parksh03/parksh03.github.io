# parksh03.github.io

박상혁의 개인 CV / 포트폴리오 사이트. 빌드 도구 없이 순수 HTML + CSS로 되어 있고,
GitHub Pages가 `main` 브랜치를 그대로 서빙합니다.

**사이트:** https://parksh03.github.io

## 구조

```
.
├── index.html          # 사이트 전체 내용 (한 페이지)
├── assets/
│   ├── style.css       # 모든 스타일 (라이트/다크/인쇄용 포함)
│   ├── profile.jpg     # ← 프로필 사진을 이 이름으로 넣으면 자동 표시
│   └── cv.pdf          # ← CV PDF를 이 이름으로 넣으면 헤더 링크가 연결됨
├── .nojekyll           # Jekyll 처리 비활성화 (파일을 그대로 서빙)
└── README.md
```

## 수정 방법

1. `index.html`을 열어 텍스트를 고칩니다. 섹션마다 `<!-- ─── SECTION ─── -->` 주석이 있습니다.
2. 브라우저로 `index.html`을 바로 열어서 확인합니다. 서버를 띄울 필요 없습니다.
3. 커밋하고 푸시하면 1~2분 안에 사이트에 반영됩니다.

```bash
git add -A
git commit -m "Update CV"
git push
```

## 채워야 할 부분

플레이스홀더 링크는 `data-todo` 속성이 붙어 있어서 화면에서 주황색 점선 + `↩` 표시로
눈에 띕니다. 실제 URL을 넣고 `data-todo`를 지우면 평범한 링크가 됩니다.

남은 항목을 한 번에 확인:

```bash
grep -n 'data-todo' index.html
```

- [x] 이름 로마자 표기 (Sanghyeok Park), 직함 (Undergraduate Student), 연구실 (CLink Lab)
- [x] 소속 (Pusan National University · School of Computer Science and Engineering · Artificial Intelligence Major)
- [x] 입학 연도 (2023)
- [ ] About 두 문단
- [ ] 학력 상세 (GPA, 복수전공 등 — 선택)
- [ ] 연구 관심 주제 3개
- [ ] 논문 목록 + paper/arXiv/code 링크
- [x] CLink Lab 합류 시점 (2025.11)
- [ ] 경력 내용 (bullets 채우기)
- [ ] 수상, 학회 봉사, 스킬
- [x] 이메일 (메인 parksh03@pusan.ac.kr / 서브 tnlfl8888@gmail.com)
- [x] GitHub (연구 parksh03 / 개인 프로젝트 parksh23)
- [x] LinkedIn URL
- [ ] Google Scholar URL (`data-todo` 2곳)
- [ ] `assets/cv.pdf`
- [ ] `assets/profile.jpg` — 넣기 전까지는 "사진" 자리표시 원이 보입니다

## PDF로 뽑기

브라우저에서 `Ctrl+P` → PDF로 저장. 인쇄용 스타일이 따로 들어 있어서 네비게이션과
사진이 빠지고 흑백 단색으로 깔끔하게 나옵니다.

## 커스텀 도메인

도메인이 있다면 `CNAME` 파일에 도메인 한 줄만 넣고 푸시한 뒤,
GitHub 저장소 Settings → Pages에서 도메인을 등록하면 됩니다.
