<template>
<div class="twoSty">
  <div class="imga">
    <img src="/balance.png" class="im" alt="Весы">
  </div>
  <div class="AreWe"  >
    <h2>Почему мы</h2>
    <p class="textOne">
      Мы – группировка увлеченных своим делом юристов.
    </p>
    <p class="textTwo">
       Мы любим свою работу.
    </p>
    <p class="textThree">
       Особенно и очень – судебные процессы.
    </p>
    <p class="textFour">
       И только от любви к своему делу мы дотошно вникаем в суть каждого вопроса,отрабатываем десятки и сотни вариантов решения проблемы, придумываем нестандартные решения и можем ради этого не спать ночами.
    </p>
  </div>
</div>
  <div class="twoThree">
    <div class="textTwoOne">
      <p style="display: inline-block; color: #313C98;
    font-family: Segoe UI;
    font-size: 31.509px;
    font-style: normal;
    font-weight: 600;
    line-height: 167.508%;
    letter-spacing: 2.206px;" >Мы знаем,</p><p style="display: inline-block;">как победить в суде, как найти баланс между&nbsp;</p>
      <p class="need">&#171;хочется&#187;</p>
      <p>&nbsp;и&nbsp;</p>
      <p class="need">&#171;можно&#187;,</p>
      <p>&nbsp;как с помощью правовых решений не только сэкономить, но и заработать.</p>
    </div>

    <div class="arrow-container" @click="navigateToOne">
      <div class="arrow">
        <p class="rotate">К специалистам</p>
        <div class="arrowItem">
          <div class="circle"></div>
          <svg class="svg" width="32" height="112" viewBox="0 0 32 112" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M16 0L16 111" stroke="black"/>
            <path d="M1 95L16 111L31 95" stroke="black"/>
          </svg>
        </div>

      </div>
    </div>

    <div class="isNotEasy">
      <div class="trash"></div>
      <h2>Но с нами не будет просто</h2>
      <p class="tr">При решении любой задачи глубоко погружаемся в ее фактическую сторону (а знаете ее только вы), поэтому задаем много вопросов</p>
      <p>Любим залезть туда, куда не просят, чтобы предложить, как сделать еще лучше</p>
      <p>Внимательны до мелочей и ведем учет всего, чего возможно</p>
      <p>Всегда принципиальны в своей позиции</p>
    </div>
  </div>
  <div id="one" ></div>
</template>

<script>
export default {
  name: "IamProfile",
  data() {
    return {
      isVisible1: false,
    };
  }
};
</script>


<style scoped>
.arrow {
  display: flex;
  justify-content: space-around;
}
p,h2 {
  font-family: "Segoe UI";
  font-size: 17px;
  font-style: normal;
  font-weight: 300;
  display: inline-block;
  line-height: 150.008%; /* 25.501px */
  letter-spacing: 1.19px;
}
.isNotEasy {
  max-width: 54%;
}
.need {
  color: #313C98;
  font-weight: 500;
}
svg.svg {
  position: relative;
  z-index: 2;
}
.isNotEasy > p{
  display: block;
}
.arrowItem {
  position: absolute;
}
.twoSty {
  width: 96%;

  margin: auto;
  margin-top: 60px;
  display: flex;
  justify-content: space-around;
}
.textOne,.textTwo,.textThree, .textFour{
  display: inline-block;
}

.rotate {
  transform: rotate(-100grad);
  white-space: nowrap;
}

.arrow-container {
  position: relative;
  width:110px; /* Ширина SVG */
  height: fit-content; /* Высота SVG */
  margin-top: 60px;
}

.arrow {
  position: relative;
}

.circle {
  position: absolute;
  width: 70px; /* Диаметр круглешка */
  height: 70px; /* Диаметр круглешка */
  background-color: #F2F2F2; /* Цвет круглешка */
  border-radius: 50%; /* Для создания круглой формы */
  left: 50%;
  bottom: -22px; /* Круглешок будет прижат к нижней границе SVG */
  transform: translateX(-50%);
  transition: transform 0.3s ease-in-out; /* Плавное изменение положения */
}

.arrow-container:hover .circle {
  transform: translateX(-50%) translateY(-140%); /* При наведении курсора круглешок будет изменяться только по вертикали */
}


.isNotEasy > h2 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%;
  letter-spacing: 2.206px;
}
.isNotEasy > p, .isNotEasy > h2 {
  position: relative;
  z-index: 3;
}
.isNotEasy {
  position: relative;
  width: fit-content;
}
.trash {
  position: absolute;
  width: 96%;
  top: -4px;
  height: 120%;
  right: -26px;
  border-radius: 7px;
  background: #F2F2F2;
  z-index: 0;
}
.textOne:hover,.textTwo:hover,.textThree:hover, .textFour:hover{
  cursor: pointer;

  color: rgba(0, 0, 0, 0.34);
}
.isNotEasy > p {
  margin-top: 10px;
}
.tr {
  margin-top: 20px !important;
}
.arrow {
  width: 60px;
  height: 120px;
  margin: auto;
}
.textFive:after {
  content: '|';
  margin-left: -6.5px;
}
.textTwoOne {
  text-align: center;
  position: relative;
  margin-top: 20px;
  max-width: 325px;
}
.textFive {
  margin-top: 16px;
}
.im {
  width: 100%;
  height: auto;
  margin-top: 20px;
}
.AreWe > h2 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%; /* 52.779px */
  letter-spacing: 2.206px;
}
.twoThree {
  display: flex;
  justify-content: space-around;
  width: 96%;
  margin: auto;
  margin-top: 80px;
}
.AreWe {
  width: 60%;
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  justify-content: space-between;
}

.imga {
 max-width: 281px;
}
.textFive:hover:after {
  content: 'й';
}
@media only screen and (max-width: 991px) {
  .twoSty {
    width: 90%;
    margin: auto;
    margin-top: 60px;
    display: flex;
    justify-content: space-around;
    flex-direction: column-reverse;
  }
  * {
    margin: 0;
    padding: 0;
  }
  .isNotEasy {
    max-width: 100% !important;
  }
  .arrow-container {
    display: none;
  }
  .twoThree {
    flex-direction: column;
    width: 90%;
    margin-top: 7px;
    align-items: center;
  }
.AreWe {
  width: 100%;
}
  p.textOne {
    margin-top: 20px;
  }
  .isNotEasy {
    margin-top: 30px;
  }
h2 {line-height: 33px !important;}
.trash {
  width: 81%;
  top: -4px;
  height: 109%;
  right: 7px;
  border-radius: 7px;
  background: #F2F2F2;
  z-index: 0;
}
  .imga {
    width: 62%;
    margin: auto;
  }
}
.need {
  transition: 0.2s;
}
.need:hover {
  transform: scaleY(1.4);
}
</style>