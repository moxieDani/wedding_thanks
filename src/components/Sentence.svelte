<script lang="ts">
import thankyou from '@/assets/thankyou.jpg';
const 문구1 = `WE ARE GREATEFUL FOR YOUR BLESSINGS`;

const 문구2 = `아름다운 부부로 첫 출발하는
저희를 지켜봐 주시고
축복해 주셔서
진심으로 감사드립니다.`;
const 문구3 = `행복하게 잘 살겠습니다.`;

</script>

<section class="greeting-section">
  <div style="border-top: 1px solid #000; margin: 0 auto 3rem; width: 30%;"></div>
  <div class="sec-tit great-vibes flex-center">Thank you</div>
  <div class="sec-sub-tit">{문구1}</div>
  <div class="flex-center">
    <img src={thankyou} width="60%" style="margin-bottom: 2rem;"/>
  </div>
  <div class="sec-txt">{문구2}</div>
  <div class="sec-txt">{문구3}</div>
  <div class="info flex-center" style="display: flex; align-items: center; margin-bottom:3rem;">
    <p class="gwangye" style="margin: 0;">신랑<br><span class="slsb">권기순</span></p>
    <p class="gwangye" style="margin: 0; display: flex; align-items: center;"> 
        <span class="slsb" style="font-size: 1rem;">❤️</span>
    </p>
    <p class="gwangye" style="margin: 0;">신부<br><span class="slsb">박서은</span></p>
  </div>
  <div style="border-bottom: 1px solid #000; margin: 0 auto 3rem; width: 30%;"></div>
</section>

<style>
.greeting-section {
  padding: 3.125rem 0;
}
.greeting-section .sec-tit {
  position: relative;
  margin-top: 4rem;
  margin-bottom: 1rem;
  font-size: 3rem;
  line-height: 1.25rem;
  text-align: center;
  color: #111;
}
.greeting-section .sec-txt-name {
  margin-bottom: 2rem;
  font-size: 1.2rem;
  font-weight: 300;
  line-height: 2rem;
  color: #111;
  text-align: center;
  white-space: pre-wrap;
}
.greeting-section .sec-sub-tit {
  margin-bottom: 1rem;
  font-size: 0.8rem;
  font-weight: 300;
  line-height: 2rem;
  color: #111;
  text-align: center;
  white-space: pre-wrap;
}
.greeting-section .sec-txt {
  margin-bottom: 1rem;
  font-size: 1rem;
  font-weight: 300;
  line-height: 2rem;
  color: #111;
  text-align: center;
  white-space: pre-wrap;
}
.greeting-section .info {
  font-size: 0;
  line-height: 0;
  padding-top: 10%;
  text-align: center;
}
.greeting-section .info .row {
  display: table-row;
}
.greeting-section .info p {
  display: table-cell;
  vertical-align: top;
}
.greeting-section .info .honju {
  font-size: 0;
  text-align: right;
}
.greeting-section .info .honju .gt-span {
  display: inline-block;
  vertical-align: top;
  font-weight: 700;
  font-size: 1rem;
  letter-spacing: 0.14em;
  line-height: 1.5rem;
  text-align: center;
  white-space: pre-wrap;
}
.greeting-section .info .honju .bul {
  position: relative;
  width: 0.75rem;
  height: 1.5rem;
  overflow: hidden;
}
.greeting-section .info .honju .bul:after {
  content: '.';
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  display: block;
  font-size: 0.813rem;
  font-weight: 400;
  line-height: 1;
  text-align: center;
}
.greeting-section .info .gwangye {
  height: 2.5rem;
  padding-left: 0.188rem;
  font-size: 0.9rem;
  font-weight: 300;
  line-height: 1.625rem;
}
.greeting-section .info .slsb {
  vertical-align: top;
  font-weight: 700;
  font-size: 1.2rem;
  letter-spacing: 0.14rem;
  line-height: 1.5rem;
  text-align: center;
}
</style>
