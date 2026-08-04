# 숨김(주석) 처리된 섹션 아카이브

index.html에서 HTML 주석으로 가려져 있던 두 섹션의 원본 그대로 백업. 필요하면 그대로 복원 가능.

## OUR SERVICES — 8개 카드 매소너리 그리드

```html
<!-- 2. SERVICES -->
<section class="services section" id="services">
  <div class="container--flush">
    <div class="section-head" data-reveal>
      <h2 class="display-thin">OUR SERVICES</h2>
      <p class="section-head__eyebrow subtle">발주부터 정산까지, 사람 손을 거치지 않는 자동화 서비스를 만나보세요.</p>
    </div>
    <div class="services__grid">
      <div class="services__col">
        <div class="service-card service-card--even img" data-reveal>
          <img class="service-card__photo" src="assets/images/afinis-group-afinis-gasket-production-OnbSOhz0oig-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">자동발주</span><span class="en">AUTO ORDERING</span></span>
        </div>
        <div class="service-card service-card--even img" data-reveal>
          <img class="service-card__photo" src="assets/images/kim-r-k-MGv8t99Vg2U-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">AI 재고예측</span><span class="en">AI DEMAND FORECAST</span></span>
        </div>
      </div>
      <div class="services__col">
        <div class="service-card service-card--short img" data-reveal>
          <img class="service-card__photo" src="assets/images/simon-kadula-8gr6bObQLOI-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">스마트 물류센터</span><span class="en">SMART WAREHOUSE</span></span>
        </div>
        <div class="service-card service-card--tall img" data-reveal>
          <img class="service-card__photo" src="assets/images/thomas-delacretaz-nYpDFxl7Ew8-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">무인 매장 운영</span><span class="en">UNMANNED STORE OPS</span></span>
        </div>
      </div>
      <div class="services__col">
        <div class="service-card service-card--even img" data-reveal>
          <img class="service-card__photo" src="assets/images/white-rainforest-1ydzob4cphs-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">실시간 데이터 분석</span><span class="en">REALTIME ANALYTICS</span></span>
        </div>
        <div class="service-card service-card--even img" data-reveal>
          <img class="service-card__photo" src="assets/images/ant-rozetsky-SLIFI67jv5k-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">자동 정산 시스템</span><span class="en">AUTO SETTLEMENT</span></span>
        </div>
      </div>
      <div class="services__col">
        <div class="service-card service-card--tall img" data-reveal>
          <img class="service-card__photo" src="assets/images/kseniia-ilinykh-82ZiY5pzl1c-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">자동 품질검수</span><span class="en">AUTO QC</span></span>
        </div>
        <div class="service-card service-card--short img" data-reveal>
          <img class="service-card__photo" src="assets/images/adrian-sulyok-sczNLg6rrhQ-unsplash.jpg" alt="" loading="lazy">
          <span class="service-card__label"><span class="kr">자동화 유통 네트워크</span><span class="en">AUTOMATED NETWORK</span></span>
        </div>
      </div>
    </div>
  </div>
</section>
```

## TRACK RECORDS — 통계 3열

```html
<!-- 6. TRACK RECORDS — full-bleed dark -->
<section class="track section">
  <div class="container--flush">
    <div class="track__head" data-reveal>
      <h2 class="display-thin">TRACK RECORDS</h2>
      <p class="subtle">자동화 시스템으로 쌓아온 성과를 데이터로 증명합니다.</p>
    </div>
    <div class="track__stats" data-reveal>
      <div class="track__stat">
        <p class="num">150+</p>
        <p class="label">자동화 도입 브랜드</p>
      </div>
      <div class="track__stat">
        <p class="num">32개</p>
        <p class="label">무인 물류거점</p>
      </div>
      <div class="track__stat">
        <p class="num">99.8%</p>
        <p class="label">AI 예측 정확도</p>
      </div>
    </div>
  </div>
</section>
```

## 참고
- CSS(`.services__grid`, `.service-card*`, `.track`, `.track__*`)는 site.css에 그대로 남아있음 — 복원 시 별도 CSS 작업 불필요.
- 두 섹션 모두 index.html에서는 삭제되고 이 문서로만 보존됨(주석 처리 상태로 남겨두지 않음).
