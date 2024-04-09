<template>
  <q-layout view="lHh Lpr lFf" class="home-page">
    <q-header class="header-toolbar">
      <div class="row">
        <div class="col-4">
          <div class="header-section">
            <q-btn text flat class="text-capitalize">
              <img alt="Quasar logo" src="~assets/group.png" style="width: 20px; height: 15px">
              <span class="q-ml-sm"> Hyperhire</span>
            </q-btn>
          </div>
        </div>
        <div class="navbar-mobile-item">
          <q-icon name="remove"></q-icon>
        </div>
        <div class="col-4 navbar-items">
          <div class="row justify-center">
            <div>
              <q-btn color="white" flat label="채용" style="margin-top:5px;">
                <img src="~assets/caret-down.png" style="width: 15px; height: 15px; margin-left:5px;" alt="">
                <q-menu>
                  <q-list>
                    <q-item>
                      <p class="text-weight-bold">채용</p>
                    </q-item>
                    <q-item v-for="n in options" :key="n" dense clickable>
                      <q-item-section @click="selectedOptionFn(n)">{{ n }}</q-item-section>
                    </q-item>
                  </q-list>
                </q-menu>
              </q-btn>
            </div>
            <div class="inline-item">
              {{ selectedOption }}
            </div>
          </div>
        </div>
        <div class="col-4 navbar-items">
          <div style="position:relative;left:265px;top:10px"> <q-btn flat
              style="background-color:#FFFFFF;color:#4A77FF;font-weight:600">문의하기</q-btn></div>
        </div>
      </div>
    </q-header>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  components: {},
  data: () => ({
    selectedOption: '해외 개발자 원격 채용',
    options: [
      '해외 개발자 원격 채용',
      '외국인 원격 채용 (비개발 직군)',
      '한국어 가능 외국인 채용'
    ],
  }),
  methods: {
    updateLabel() {
      const label = this.$refs.selectRef.label;
      this.$refs.selectRef.$el.querySelector('.q-field__label').innerText = label;
    },
    selectedOptionFn(text) {
      this.selectedOption = text
    }
  }
}
</script>
<style scoped>
/* In your CSS file or component */
.home-page {
  background-image: url('~assets/background.png');
  /* Additional CSS properties for styling the background */
}

.header-toolbar {
  background-color: transparent !important;

}

.header-section {
  position: absolute;
  left: 90px;
}

.inline-item {
  margin-left: 50px;
  margin-top: 12px;
  /* Add spacing between inline items */
}

.custom-select .q-field__native {
  border-color: red;
}

.navbar-items {
  display: block;
}

.navbar-mobile-item {
  display: none;
}

@media only screen and (max-width: 600px) {
  .header-section {
    position: absolute;
    left: 10px;
    top: 5px;
  }

  .navbar-items {
    display: none;
  }

  .navbar-mobile-item {
    display: block;
    position: absolute;
    left: 310px;
    top: 10px;
  }
}
</style>
