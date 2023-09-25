<template>
  <div class="person">
    <div class="allInfo">
      <div class="oneInfo">
<div class="picMan">
  <div class="imgas">
    <img src="/one.png" alt="beautiful">
    <div class="bg"></div>
    <div class="name">
      <p>Екатерина Юргулевич</p>
    </div>
  </div>
</div>
<div class="obrazov">
  <div class="bga"></div>
  <p class="obrazova hell">Образование</p>
  <p class="obraDesc hell">Байкальский государственный университет экономики и права</p>
  <p class="low hell">Юрист</p>
</div>
      </div>
      <div class="twoInfo">
  <div class="slider">
    <div class="topS">
    <p class="exapmleCase">Примеры кейсов</p>
      <div class="buttonss dbu">
        <div @click="back" class="rigthButton"><svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="20" cy="20" r="20" transform="rotate(-180 20 20)" fill="#D9D9D9"/>
          <path d="M23 11L14 20L23 29" stroke="black"/>
        </svg>
        </div>
        <p style="user-select: none;margin: 0 10px;">{{ slide + 1 }}/{{ cases.length }}</p>
        <div  @click="next" class="leftButton"><svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="20" cy="20" r="20" fill="#D9D9D9"/>
          <path d="M17 29L26 20L17 11" stroke="black"/>
        </svg>
        </div>
      </div>
    </div>

    <Text-Sa :text="cases[slide].text"/>
    <div class="gb"></div>
    <div class="buttonss mbu">
      <div @click="back" class="rigthButton"><svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" transform="rotate(-180 20 20)" fill="#D9D9D9"/>
        <path d="M23 11L14 20L23 29" stroke="black"/>
      </svg>
      </div>
      <p style="user-select: none;margin: 0 10px;">{{ slide + 1 }}/{{ cases.length }}</p>
      <div  @click="next" class="leftButton"><svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="20" cy="20" r="20" fill="#D9D9D9"/>
        <path d="M17 29L26 20L17 11" stroke="black"/>
      </svg>
      </div>
    </div>
  </div>
        <div class="cariera">
          <div class="top">
            <h2>Карьера</h2>
          </div>
          <div class="shel">
          <div class="leftCar">
            <div class="lc">

              <p>от юрисконсульта в операционном офисе банка</p>
            </div>
            <div class="rc">
              <p>и главного юрисконсульта генподрядчика на строительство металлургических объектов
              </p>
            </div>
          </div>
          <div class="rigthCar">
            <div class="lc">
              <p>до руководителя судебного направления в строительной организации металлургического профиля</p>
            </div>
          </div>
          </div>
            <div class="gac"></div>

        </div>
      </div>
    </div>
  </div>
</template>

<script>
import '../../public/fonts/SegoeUI.ttf'
import  '../../public/fonts/Oswald/Oswald-Bold.ttf'
import TextSa from './TextS.vue'
export default {
  name: "PersonComponent",
  components: {
    TextSa
  },
  data() {
    return {
      slide: 0, // Изменено с 1 на 0, так как массив начинается с индекса 0
      cases: [
        { id: 1, text: "находясь на стороне кредитора провела работу по сбору доказательств и обоснованию правовой позиции, в результате чего контролирующее должника лицо было привлечено к субсидиарной ответственности на сумму более 40 млн. руб." },
        { id: 2, text: "доказала в суде необоснованность требований подрядчика об оплате 36 млн. руб. за работы несмотря на то, что заказчик эти работы принял" },
        { id: 1, text: "при отказе заказчика принимать работы по договору на геологоразведку доказала, что составленное подрядчиком ТЭО соответствует техзаданию, и помогла взыскать с заказчика 60 млн. руб. за работы и 16 млн. руб. неустойки" },
        { id: 2, text: "добилась взыскания с подрядчика 49 млн. руб. штрафной неустойки за нарушение сроков выполнения работ против 24 млн. руб. по сложившейся судебной практике" },
        // Добавьте остальные кейсы здесь
      ]
    }
  },
  methods: {
    back() {
      if (this.slide > 0) { // Проверяем, что слайд не находится в начале
        this.slide -= 1;
      }
    },
    next() {
      if (this.slide < this.cases.length - 1) { // Проверяем, что слайд не находится в конце
        this.slide += 1;
      }
    }
  }
}
</script>

<style scoped>
.slider {
  margin-top: 20px !important;
}
.leftCar, .rigthCar {
  width: 48.5%;
  position: relative;
  z-index: 5;

}
.mbu {
  display: none;
  margin-top: 20px;
}
.obrazov {
  position: relative;
  margin-top: 30px;
  width: 100%;
  height: fit-content;
}
.top {
  position: relative;
  z-index: 4;
}
.cariera {
  margin-top: 70px;
  position: relative;
}
.gac {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: 2;
  right: -14px;
  top: 0;
  border-radius: 7px;
  background: #F8F8F8;
}
.top > h2 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 19.619px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%; /* 32.863px */
  letter-spacing: 1.373px;
}
.rc {
  width: 50%;
  left: 46%;
  position: relative;
}
.shel {
  margin-top: 9px;
  display: flex;
  justify-content: space-between;
}
.topS {
  width:95%;
  display: flex;
  flex-direction: row;
  align-content: center;
  justify-content: space-between;
}

.buttonss {
  position: relative;
  z-index: 4;
  align-content: center;
  justify-content: space-between;
  align-items: center;
}
@font-face {
  font-family: Oswald;
  src: url('../../public/fonts/Oswald/Oswald-Light.ttf') format('truetype');
  font-weight: 400;
  font-display: swap; /* Использовать системный шрифт до загрузки Oswald */
}
.rigthButton:active, .leftButton:active {
  opacity: 0.5;
}
.slider {
  position: relative;
  width: 100%;
  height: fit-content;
}

h2,h3 {
  font-family: "Segoe UI";
}


.case {
  position: relative;
  z-index: 4;
  color: #000;
  font-size: 17px;
  font-style: normal;
  font-weight: 400;
  line-height: 167.508%; /* 28.476px */
  letter-spacing: 1.19px;
}
.lc>p, .rc > p{
  color: #000;
  font-size: 17px;
  font-style: normal;
  font-weight: 400;
  line-height: 167.508%; /* 28.476px */
  letter-spacing: 0.68px;
}
.lc >h3, .rc >h3 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 17px;
  font-style: normal;
  font-weight: 700;
  line-height: 167.508%; /* 28.476px */
  letter-spacing: 1.19px;
}
.exapmleCase {
  color: #313C98;
  position: relative;
  z-index: 5;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%; /* 52.779px */
  letter-spacing: 2.206px;
}

.gb {
  position: absolute;
  top: 50px;
  height: 100%;
  width: 94%;
  z-index: 3;
  right: 0;
  left: 0;
  margin: auto;
  border-radius: 7px;
  background: #F8F8F8;
  bottom: 0;
}
.hell {
  position: relative;
  z-index: 1;
}
.bga {
  background: white;
  position: absolute;
  height: 98%;
  top: -7px;
  z-index: 1;
  right: -9px;
  width: 97%;
  border-radius: 7px;
}
.obraDesc {
  color: #000;
  font-size: 17px;
  font-style: normal;
  font-weight: 400;
  line-height: 167.508%; /* 28.476px */
  letter-spacing: 0.68px;
}
.low {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 17px;
  font-style: normal;
  font-weight: 700;
  line-height: 167.508%; /* 28.476px */
  letter-spacing: 1.19px;
}
.obrazova {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 19.619px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%; /* 32.863px */
  letter-spacing: 1.373px;
}
.person {
  width: 95%;
  margin: auto;
  margin-top: 20px !important;
  overflow: hidden;
  background: #F2F2F2;
}
.picMan {
  width: fit-content;
  height: fit-content;
  margin: auto;
}
.bg {
  position: absolute;
  top: 29px;
  height: 84%;
  width: 94%;
  z-index: 1;
  right: 0;
  left: 8px;
  margin: auto;
  border-radius: 7px;
  background: #F8F8F8;
  bottom: 0;
}
p, h3 {
  font-family: "Segoe UI";
}
.name > p {

  text-wrap: nowrap;
  color: #FFF;
  font-size: 25px;
  font-family: Oswald;
  font-style: normal;
  font-weight: 700;
  text-align: center;
  line-height: 167.508%; /* 41.877px */
  letter-spacing: 2px;
  border-radius: 7px;
}
.imgas{
  width: 100%;
  position: relative;
  height: -moz-fit-content;
  height: fit-content;
  display: flex;
  flex-direction: column;

}
.imgas > img {
  position: relative;
  max-width: 240px;
  z-index: 2;
  margin: auto;
  margin-bottom: -4px;
  max-height: fit-content;
}







.name {
  width: 100%;
  height: -moz-fit-content;
  height: fit-content;
  position: relative;
  z-index: 2;
  box-sizing: border-box;
  background: #2637CB;
  border-radius: 3px;
}
.oneInfo,.twoInfo {
  width: 300px;
  height: fit-content;
}
.twoInfo {
  width: 60%;
}
.dbu {
  display: flex;
}

.allInfo {
  display: flex;
  width: 96%;
  margin: 10px auto;
  padding: 36px 0;
  height: fit-content;
  justify-content: space-around;
}
@media only screen and (max-width: 991px){
  .allInfo {
    flex-direction: column;
    margin: 0 auto;
  }
  .shel {
    flex-direction: column
  }
  .gb {
    height: 72%;
  }
  .mbu {
    width: 146px;
    position: relative;
    margin-left: 57%;
  }
  .person {
    width: 100%;
    background: linear-gradient(180deg, rgba(242, 242, 242, 0.00) 0%, #F2F2F2 6.31%, #F2F2F2 100%);
  }
  .leftCar, .rigthCar {
    width: 100%;
  }
  h3.mr {
    text-align: right;
  }
  .bga {
    height: 111%;
    top: -7px;
    z-index: 1;
    width: 74%;
    border-radius: 7px;
    margin: auto;
    right: 0;
    left: 0;
  }
  .mbu {
    display: flex;
  }
  .dbu {
    display: none;
  }
  .rigthCar > .lc {
    margin-top: 20px;
  }
  .twoInfo {
    width: 100%;
    margin-top: 10px;
    display: flex;
    flex-direction: column-reverse;
    justify-content: flex-start;
  }
  .name {
    width: 100% !important;
  }
  .cariera {
    margin-top: 23px;
    position: relative;
  }

  .person {
    width: 96%;
    margin: auto;
  }
  .rc {
    width: 50%;
    margin-left: 34%;
    left: 0;
  }
  .picMan {
    width: fit-content;
    height: fit-content;
    margin: auto;
  }
  .oneInfo {
    margin: auto;
    width: 100% !important;
  }
}

</style>