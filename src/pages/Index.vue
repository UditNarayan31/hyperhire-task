<template>
  <div>
    <q-page>
      <div class="row">
        <!-- left content section -->
        <div class="col-7">
          <div class="main-container">
            <div class="left-tag" data-aos="zoom-in"
                data-aos-duration="300">
              풀타임, 파트타임
              <div class="tag-pointer"></div>
              </div>
            <div class="page-heading" data-aos="fade-up" data-aos-duration="500">최고의 실력을 가진 외국인 <br> 인재를 찾고 계신가요?</div>
            <div class="page-subheading" data-aos="fade-up" data-aos-duration="500">
              법률 및 인사관리 부담없이 1주일 <br>이내에 원격으로 채용해보세요.
            </div>
            <div class="page-subheading-small mobile-item">
              개발자가 필요하신가요?
            </div>
            <div class="row">
              <div class="col-3 mobile-item" v-for="(item, i) in content" :key="i" data-aos="zoom-in"
                data-aos-duration="500">
                <div>
                  <div class="hrline"></div>
                  <div class="content-title">{{ item.title }}</div>
                  <div class="content-subtitle">{{ item.subtitle }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- web carousel cards -->
        <div class="col-5">
          <div class="container">
            <input type="radio" name="slider" id="item-1" checked>
            <input type="radio" name="slider" id="item-2">
            <input type="radio" name="slider" id="item-3">
            <div class="cards">
              <label class="card" for="item-1" id="card-1">
                <div class="carosel-card text-center">
                  <img src="~assets/carousel.png" style="width:100px; height:100px; margin-top:40px" alt="card">
                  <h5 style="font-weight:900; font-weight:900; position:relative; bottom:25px;">Abishek Gupta</h5>
                  <div style="color:#4A77FF;font-weight:900; position:relative; bottom:60px;">마케팅 · <span>2y+</span>
                  </div>
                  <div style="position:relative; bottom:30px">
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>
                    <q-badge outline style="color: gray;">
                      인스타그램 관리
                    </q-badge>
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>

                  </div>
                </div>
              </label>
              <label class="card" for="item-2" id="card-2">
                <div class="carosel-card text-center">
                  <img src="~assets/carousel.png" style="width:100px; height:100px; margin-top:40px" alt="card">
                  <h5 style="font-weight:900; font-weight:900; position:relative; bottom:25px;">Abishek Gupta</h5>
                  <div style="color:#4A77FF;font-weight:900; position:relative; bottom:60px;">마케팅 · <span>2y+</span>
                  </div>
                  <div style="position:relative; bottom:30px">
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>
                    <q-badge outline style="color: gray;">
                      인스타그램 관리
                    </q-badge>
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>

                  </div>
                </div>
              </label>
              <label class="card" for="item-3" id="card-3">
                <div class="carosel-card text-center">
                  <img src="~assets/carousel.png" style="width:100px; height:100px; margin-top:40px" alt="card">
                  <h5 style="font-weight:900; font-weight:900; position:relative; bottom:25px;">Abishek Gupta</h5>
                  <div style="color:#4A77FF;font-weight:900; position:relative; bottom:60px;">마케팅 · <span>2y+</span>
                  </div>
                  <div style="position:relative; bottom:30px">
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>
                    <q-badge outline style="color: gray;">
                      인스타그램 관리
                    </q-badge>
                    <q-badge outline style="color:gray">
                      마케팅 콘텐츠 제작
                    </q-badge>

                  </div>
                </div>
              </label>
            </div>
            <!-- Carousel tags -->
            <div class="player" data-aos="zoom-in" data-aos-duration="500">
              <div class="upper-part">
                <div class="info-area" id="test">
                  <label class="card-info" id="card-info-1">
                    <div class="title">
                    <span class="tagcolor">$ 월 100만원</span>
                    </div>
                    <div class="sub-line">
                      <div class="subtitle">1 </div>
                      <div class="time">123</div>
                    </div>
                  </label>
                  <label class="card-info" id="card-info-2">
                    <div class="title">
                      <span class="tagcolor">$ 월 100만원</span>
                    </div>
                    <div class="sub-line">
                      <div class="subtitle">2 slide</div>
                      <div class="time">456</div>
                    </div>
                  </label>
                  <label class="card-info" id="card-info-3">
                    <div class="title">
                      <span class="tagcolor">$ 월 100만원</span>
                    </div>
                    <div class="sub-line">
                      <div class="subtitle">3rd slide</div>
                      <div class="time">789</div>
                    </div>
                  </label>
                </div>
              </div>
              <div class="pointer"></div>
            </div>
          </div>
        </div>

        <div class="col-12">
          <!-- mobile carousel -->
          <template>
            <div class="mobile-item-present">
              <q-carousel animated v-model="slide" infinite :autoplay="autoplay" arrows transition-prev="slide-right"
                transition-next="slide-left" @mouseenter="autoplay = false" @mouseleave="autoplay = true">
                <q-carousel-slide :name="1" img-src="https://cdn.quasar.dev/img/mountains.jpg" />
                <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" />
                <q-carousel-slide :name="3" img-src="https://cdn.quasar.dev/img/parallax2.jpg" />
                <q-carousel-slide :name="4" img-src="https://cdn.quasar.dev/img/quasar.jpg" />
              </q-carousel>

              <div class="q-mt-lg row">
                <div v-for="(check, c) in checkboxList" :key="c" class="col-6 text-white">
                  <img src="~assets/checkbox.png" class="q-mt-sm" style="width:18px; height:18px;" alt="">
                  <span class="q-ml-sm"> {{ check }}</span>
                </div>
                <div class="q-mt-md">
                  <a href="#" style="size:16px; font-weight:900; color:#FBFF23"> 개발자가 필요하신가요?</a>
                </div>
              </div>
            </div>
          </template>
        </div>
        <!-- web Carousel -->
        <div class="col-12">
          <div>
            <template>
              <div class="q-pa-md mobile-item">
                <q-carousel infinite :autoplay="autoplay" :autoplay-interval="5000" transition-prev="slide-right"
                  transition-next="slide-left" @mouseenter="autoplay = false" @mouseleave="autoplay = true"
                  v-model="slide" swipeable animated control-color="amber" padding arrows class="carousel-custom">
                  <q-carousel-slide :name="1" class="column no-wrap">
                    <div class="row fit items-center q-gutter-xs q-col-gutter no-wrap" style="margin-left:10px">
                      <div class="carousel-inner" v-for="(item, i) in 4" :key="i" data-aos="fade-in"
                        data-aos-duration="500">
                        <div class="row">
                          <div class="col-4">
                            <img src="~assets/slide1.png" alt=""
                              style="height:35px; width:35px; margin-top:12px; margin-left:10px">
                          </div>
                          <div class="col-8">
                            <div class="text-white" style="margin-left:20px; margin-top:25px; font-weight:900">
                              해외 마케팅
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </q-carousel-slide>
                  <q-carousel-slide :name="2" class="column no-wrap">
                    <div class="row fit items-center q-gutter-xs q-col-gutter no-wrap" style="margin-left:10px">
                      <div style="background-color:#FFFFFF33; border-radius:8px; min-width:280px;height:60px"
                        v-for="(item, i) in 4" :key="i">
                        <div class="row">
                          <div class="col-4">
                            <img src="~assets/slide2.png" alt=""
                              style="height:35px; width:35px; margin-top:12px; margin-left:10px">
                          </div>
                          <div class="col-8">
                            <div class="text-white" style="margin-left:20px; margin-top:25px; font-weight:900">
                              해외 마케팅
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </q-carousel-slide>
                  <q-carousel-slide :name="3" class="column no-wrap">
                    <div class="row fit items-center q-gutter-xs q-col-gutter no-wrap" style="margin-left:10px">
                      <!--  -->
                      <div style="background-color:#FFFFFF33; border-radius:8px; min-width:280px;height:60px"
                        v-for="(item, i) in 3" :key="i">
                        <div class="row">
                          <div class="col-4">
                            <img src="~assets/slide3.png" alt=""
                              style="height:35px; width:35px; margin-top:12px; margin-left:10px">
                          </div>
                          <div class="col-8">
                            <div class="text-white" style="margin-left:20px; margin-top:25px; font-weight:900">
                              해외 마케팅
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </q-carousel-slide>
                </q-carousel>
              </div>
            </template>
          </div>
        </div>
      </div>
    </q-page>
    <footer-component />
  </div>
</template>

<script>
import FooterComponent from 'src/components/FooterComponent.vue'
export default {
  components: { FooterComponent },
  name: 'PageIndex',
  data: () => ({
    slide: 1,
    autoplay: true,
    content: [
      { title: '평균 월 120만원', subtitle: '임금을 해당 국가를 기준으로 계산합니다.' },
      { title: '최대 3회 인력교체', subtitle: '막상 채용해보니 맞지 않아도 걱정하지 마세요. ' },
      { title: '평균 3일, 최대 10일', subtitle: '급하게 사람이 필요한 경우에도 빠른 채용이 가능합니다.' }
    ],
    carouselcontent: [
      {
        image: '~assets/carousel.png', title: 'Abishek Gupta', subtitle: 'subtitle', tags: ['abc', 'def', 'grh']
      },
      {
        image: '~assets/carousel.png', title: 'Abishek Gupta', subtitle: 'subtitle', tags: ['abc', 'def', 'grh']
      },
      {
        image: '~assets/carousel.png', title: 'Abishek Gupta', subtitle: 'subtitle', tags: ['abc', 'def', 'grh']
      }
    ],
    changeCarousel: [],
    checkboxList: ['한국어 능력', '업무 수행 능력', '겸업 여부', '평판 조회']
  }),

  methods: {
    nextCarousel() {

    },
    prevCarousel() {
      this.changeCarousel.push()
    }
  }
}
</script>
<style scoped>
.main-container {
  position: relative;
  left: 100px;
}

.page-heading {
  font-size: 42px;
  font-weight: 900;
  color: #fff;
  position: relative;
  top: 124px;
}

.page-subheading {
  font-size: 24px;
  font-weight: 900;
  line-height: 34px;
  color: white;
  position: relative;
  top: 150px;
}

.page-subheading-small {
  font-size: 18px;
  font-weight: 900;
  line-height: 27px;
  color: white;
  position: relative;
  top: 171px;
}

.hrline {
  border-top: 1px solid white;
  width: 129px;
  position: relative;
  top: 200px;
}

.content-title {
  color: #FFFFFF;
  font-size: 18px;
  line-height: 27px;
  font-weight: 900;
  position: relative;
  top: 220px;
}

.content-subtitle {
  color: #FFFFFF;
  font-size: 16px;
  line-height: 24px;
  font-weight: 900;
  position: relative;
  top: 220px;
  right: 10px;
  padding: 10px;
}

.carosel-card {
  width: 250px;
  height: 350px;
  background-color: #FFFFFF;
  position: absolute;
  top: 20px;
  justify-content: center;
  border-radius: 10px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

}


body {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 30px 10px;
  font-family: 'DM Sans', sans-serif;
  transition: background .4s ease-in;
  background-color: #c394f8;
  z-index: 2;
}

input[type=radio] {
  display: none;
}

.card {
  position: absolute;
  width: 60%;
  height: 100%;
  left: 0;
  right: 0;
  margin: auto;
  transition: transform .4s ease;
  cursor: pointer;
}

.container {
  width: 100%;
  max-width: 800px;
  max-height: 600px;
  height: 100%;
  transform-style: preserve-3d;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  position: relative;
  top: 150px;
}

.cards {
  position: relative;
  width: 100%;
  height: 100%;
  margin-bottom: 20px;
}

img {
  width: 100%;
  height: 100%;
  border-radius: 10px;
  object-fit: cover;
}

#item-1:checked~.cards #card-3,
#item-2:checked~.cards #card-1,
#item-3:checked~.cards #card-2 {
  transform: translatex(-40%) scale(.8);
  opacity: .4;
  z-index: 0;
}

#item-1:checked~.cards #card-2,
#item-2:checked~.cards #card-3,
#item-3:checked~.cards #card-1 {
  transform: translatex(40%) scale(.8);
  opacity: .4;
  z-index: 0;
}

#item-1:checked~.cards #card-1,
#item-2:checked~.cards #card-2,
#item-3:checked~.cards #card-3 {
  transform: translatex(0) scale(1);
  opacity: 1;
  z-index: 1;
}

.player {
  background-color: #E9F7EF;
  border-radius: 8px;
  min-width: 300px;
  height: 55px;
  padding: 16px 10px;
  position: relative;
  bottom: 350px;
  right: 40px;
}
.left-tag{
  background-color: #E9F7EF;
  color: #40E2E8;
  font-weight: 900;
  border-radius: 8px;
  width: 200px;
  height: 55px;
  padding: 16px 10px;
  position: absolute;
  top: 50px;
  left: 0px;
}
.tag-pointer{
  position: absolute;
  top:45px;
  left: 20%;
  transform: translateX(-50%);
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-top: 20px solid #E9F7EF; /* Adjust thickness and color of the cone */
}
.pointer {
  position: absolute;
  top:45px;
  left: 50%;
  transform: translateX(-50%);
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-top: 20px solid #E9F7EF; /* Adjust thickness and color of the cone */
}

.upper-part {
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: 12px;
  height: 36px;
  overflow: hidden;
}

.play-icon {
  margin-right: 10px;
}

.card-info {
  width: calc(100% - 32px);
  display: block;
}

.card-info .title {
  color: #403d40;
  font-size: 14px;
  line-height: 24px;
}

.sub-line {
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.subtitle,
.time {
  font-size: 12px;
  line-height: 16px;
  color: #c6c5c6;
}

.time {
  font-size: 12px;
  line-height: 16px;
  color: #a5a5a5;
  font-weight: 500;
  margin-left: auto;
}

.progress-bar {
  height: 3px;
  width: 100%;
  background-color: #e9efff;
  border-radius: 2px;
  overflow: hidden;
}

.progress {
  display: block;
  position: relative;
  width: 60%;
  height: 100%;
  background-color: #2992dc;
  border-radius: 6px;
}

.info-area {
  width: 100%;
  position: absolute;
  top: 0;
  left: 30px;
  transition: transform .4s ease-in;
}

#item-2:checked~.player #test {
  transform: translateY(0);
}

#item-2:checked~.player #test {
  transform: translateY(-40px);
}

#item-3:checked~.player #test {
  transform: translateY(-80px);
}

.carousel-custom {
  background-color: transparent;
  position: relative;
  top: 90px;
  height: 300px
}

.carousel-inner {
  background-color: #FFFFFF33;
  border-radius: 8px;
  min-width: 280px;
  height: 60px;
  margin-left: 8px
}

.mobile-item {
  display: block;
}

.mobile-item-present {
  display: none;
}
.tagcolor{
  color: #00C696;
  font-weight: 900;
}

@media only screen and (max-width: 600px) {
  .page-heading {
    font-size: 26px;
    font-weight: 900;
    color: #fff;
    position: relative;
    top: 124px;
    right: 65px;
  }

  .page-subheading {
    font-size: 18px;
    font-weight: 900;
    color: white;
    position: relative;
    top: 150px;
    right: 65px;
  }

  .carosel-card {
    display: none;
  }

  .player {
    background-color: #E9F7EF;
    border-radius: 8px;
    min-width: 320px;
    padding: 16px 10px;
    position: relative;
    top: 80px;
    right: 105px;
  }

  .mobile-item {
    display: none;
  }

  .mobile-item-present {
    display: block;
    width: 280px;
    position: relative;
    left: 40px;
    top: 260px;
  }
  .left-tag{
  background-color: #E9F7EF;
  font-size: 14px;
  color: #40E2E8;
  font-weight: 900;
  border-radius: 8px;
  width: 150px;
  height: 45px;
  padding: 16px 10px;
  position: absolute;
  top: 60px;
  left: -70px;
}
.tag-pointer{
  position: absolute;
  top:35px;
  left: 20%;
  transform: translateX(-50%);
  width: 0;
  height: 0;
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-top: 20px solid #E9F7EF; /* Adjust thickness and color of the cone */
}

}
</style>
