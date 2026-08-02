# GOODSTOCK — F&B·유통 소싱·물류 랜딩페이지

**Live: https://hhhodo.github.io/goodstock-landing/**

F&B·유통(식품/외식/유통) 브랜드의 소싱·재고·콜드체인 물류·매장 운영을 잇는 파트너 GOODSTOCK의
원페이지 랜딩입니다. 브랜드명(GOODSTOCK)은 영어, 본문 콘텐츠는 한글로 작성했으며, 모든 이미지 슬롯은
실사진 대신 `#d9d9d9`(디자인 키트 `--color-placeholder` 그대로) 플레이스홀더로 처리했습니다.

## 레퍼런스 취득 경로

Figma MCP(`get_design_context`, fileKey=`BrVaTxFSnaAlv6IT2ZRvhs`, node-id=`27:7034`)로 실측했습니다.
응답이 지오메트리 전용(색상/타이포/라운드 값 없음, 좌표만 존재)이라 그리드·간격은 실측값을 그대로
따르고, 색상·타이포·라운드는 치트시트 규칙에 따라 프로젝트 디자인 토큰(`styles.css`)만 사용했습니다.

| 섹션 | 실측 근거 | 판정 |
|---|---|---|
| OUR SERVICES | 4컬럼 462.5px, 컬럼 gap 10px, 컬럼별 높이쌍 460+460 / 300+620 / 460+460 / 620+300(비대칭 매소너리) | 4열 매소너리 카드 그리드로 이식, 텍스트는 카드 좌하단 오버레이 |
| ISSUE CHECK(뉴스) | 4컬럼 446px, gap 12px, 2행 | 4×2 카드 그리드. 단, 상단 탭 필터("ALL/WORK/CULTURE…")·검색창·"VIEW MORE" 버튼은 페이지 이동/로드-더보기형 요소로 치트시트 하드룰(및 사용자 지시)에 따라 **제외** |
| INSIGHTS/REPORTS | 1920×1080 밴드 2단, 좌우에 "INSIGHTS"/"REPORTS" 대형 라벨 | full-bleed 6-6, 중앙 이미지 + 좌우 라벨 |
| TRACK RECORDS | 다크 섹션, 통계 라벨+숫자 반복 | full-bleed dark, 통계 3열 |
| 상단 GNB | ABOUT/SERVICES/INSIGHTS/MEDIA/CAREER (서브페이지 이동 전제) | 원페이지 랜딩이므로 이 페이지에 실제로 존재하는 섹션(서비스/소개/뉴스/인사이트)로만 앵커 재구성, CAREER 등 서브페이지형 메뉴는 제외 |
| FAMILY SITE 링크 목록 | 외부 사이트 이동 목록 | 페이지 이동형 요소로 제외 |

## Variant

```
variant: typo=medium / image=high / color=mono / image-radius=sharp /
         card-radius=sharp / button-radius=sharp / border=hairline /
         button-style=solid+outline / fw=700/400 / spacing=space-11
```

## 레이아웃 — 그리드 값

```
Header    — full-bleed (sticky, 로고 + 인페이지 앵커)
Hero      — full-bleed dark, 중앙 육각 그래픽 + 3줄 헤드라인
Services  — 4열 매소너리 카드 그리드(Figma 실측 460+460 / 300+620 / 460+460 / 620+300)
Intro     — 5-7 (이미지 좌 / 브랜드 소개+정보 리스트 우)
News      — 4열×2행 카드 그리드(Figma 실측 446px, gap 12px)
Insights  — full-bleed 6-6 (좌우 대형 라벨 + 중앙 이미지)
Track     — full-bleed dark, 통계 3열
Footer    — full-bleed dark
```

## 검증

- 섹션 태그 균형(`<section>`/`</section>` 개수 일치), CSS 변수 참조(`--color-primary-500/600/700`,
  `--fs-display-sm`, `--fs-h1` 등) 모두 `styles.css`에 실재함을 확인.
- 로컬 HTTP 서버(`python3 -m http.server`)로 정적 서빙 200 응답 확인.
- 색상·라운드·타이포는 임의 값 없이 전부 `styles.css` 토큰만 사용(치트시트 "No arbitrary colors/radius" 하드룰 준수).
