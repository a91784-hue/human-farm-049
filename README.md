# 인간 사육장 — 관찰시설 v2 개선본

- [개선본 플레이](https://a91784-hue.github.io/human-farm-049/v2.html)
- [기존 v1 보존본](https://a91784-hue.github.io/human-farm-049/)
- [전체 소스 ZIP](human-farm-v2-source.zip)
- [테스트 보고서](TEST_REPORT.md)
- [v1/v2 Git 이력](human-farm-history.bundle)

이 브랜치에는 개선본 실행 파일과 전체 소스 압축본을 보관합니다. 기존 공개 루트의 index.html은 교체하지 않았습니다. 개발 소스 기준 커밋은 `2d92d181ca76f3e4797829caecabfebd5a5ead26`, 원본 보존 커밋은 `a027c4d8a05c8cab9832f954e30d6a34ab950faf`입니다.

## 실행과 수정

소스 ZIP을 내려받고 해제합니다. `human-farm-v2` 폴더에서 Node.js 18 이상으로:

```sh
npm start
```

http://127.0.0.1:4173 에 접속합니다. 별도 npm install은 필요하지 않습니다. `human-farm.html` 단독 실행도 가능합니다.

```sh
npm test
npm run check
npm run build
```

소스 ZIP에는 dist/ 모듈, 테스트, 자산 관리 문서, 검수 보고서, 실행 서버와 빌드 도구가 포함되어 있습니다. 상세 실행법은 압축본의 README.md와 QUICK_START.txt를 참고하세요.

Git 이력을 복원하려면 bundle 파일을 내려받은 폴더에서:

```sh
git clone human-farm-history.bundle human-farm-source
git -C human-farm-source switch overhaul/observatory-v2
```

`baseline/deployed-v1`은 변경 전 소스를 보존합니다.

## 변경 내용

환경 재질·조명·구조물, 성체 비둘기 모델, 카키 소매와 손, 구역별 합성 음향을 개선했습니다. 공간 기억 실험, 실제 문 통과에 따른 미로 판정, A/B 방 직접 탐색, 급이·시선·차폐 퍼즐, 행동별 관찰 기록을 강화했습니다. CCTV에는 실제 이동과 앉은 자세를 반영합니다.

자동 검사 54개를 통과했습니다. 공개 HTTPS 개선본에서 실제 이동 속도와 공용 상호작용을 쓰는 브라우저 진단으로 6챕터부터 엔딩까지 확인했습니다. 일반 입력 일부도 별도 확인했습니다.

상용 실사 에셋·정확한 첨부 얼굴·성우 녹음은 미구현입니다. 직접 청음, 전체 경로 수동 완주, 처음 플레이하는 사람의 15~20분 분량, 여러 PC 성능 검증은 완료하지 않았습니다. 자세한 범위는 테스트 보고서에 구분했습니다.

원작: 비둘기 새끼를 본 적이 있는가 / 나폴리탄 괴담 킴
