# HERO — 이미지 버전 백업 (영상 버전으로 교체하기 전 원본 그대로 기록)

영상 히어로로 교체하기 직전 상태. 필요하면 이 코드 그대로 복원 가능.

## HTML (index.html 44~50행)

```html
  <!-- 1. HERO -->
  <section class="hero">
    <div class="container--flush">
      <img class="hero__illustration" src="assets/images/milad-fakurian-Y7jY9iblRKM-unsplash.png" alt="" data-reveal aria-hidden="true">
      <h1 class="hero__title" data-reveal>신선함이 이어지는<br>유통의 미래를<br>그립니다</h1>
    </div>
  </section>
```

## CSS (css/site.css 52~77행)

```css
/* ---------- hero ---------- */
/* nav가 fixed로 겹치므로 상단 여백을 nav 높이(80px) + 섹션 여백만큼 확보 */
.hero{position:relative;background-color:var(--color-primary-900);color:var(--text-default-inverse);
  background-image:radial-gradient(circle,var(--color-primary-700) 1.5px,transparent 1.5px);
  background-size:28px 28px;
  padding-block:calc(80px + var(--space-9)) var(--space-11);overflow:hidden;}
.hero__illustration{display:block;width:min(480px,70%);height:auto;object-fit:contain;
  margin-inline:auto;margin-bottom:var(--space-9);
  filter:drop-shadow(0 24px 40px rgba(0,0,0,.18));
  animation:hero-float 5s ease-in-out infinite;}

@keyframes hero-float{
  0%,100%{transform:translateY(0);}
  50%{transform:translateY(-16px);}
}
@media (prefers-reduced-motion:reduce){
  .hero__illustration{animation:none;}
}
.hero__title{text-align:center;font-weight:var(--fw-base);
  font-size:clamp(36px,7vw,140px);line-height:1.02;letter-spacing:-0.01em;}
.hero__sub{text-align:center;margin-top:var(--space-6);color:var(--text-subtle-inverse);}

@media (max-width:768px){
  .hero{background-size:20px 20px;}
  .hero__illustration{width:min(280px,80%);margin-bottom:var(--space-7);}
}
```

## 참고
- 이 시점엔 hero__sub(서브카피)가 HTML에서 이미 제거된 상태였음(직전 요청으로 삭제).
- 도트 배경(radial-gradient) + 중앙 이미지(둥둥 애니메이션, object-fit:contain, drop-shadow) + 헤드라인 구조.
