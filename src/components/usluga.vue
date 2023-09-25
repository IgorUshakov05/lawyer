<template>
  <div class="contact">
    <div class="contacta">
      <hr>
      <div class="contacts">
        <h2>Что можем</h2>
      </div>
    </div>
    <div  class="gos">
      <div class="wige">
        <img class="hangs" src="/image2.png" alt="Руки">
      </div>
      <div class="letsGo">
        <div class="elems">
          <h3>Правовой аудит</h3>
          <p>Проведем анализ дебиторской задолженности вашей организации – выявим реальных и потенциальных неплательщиков, поставим их на учет и организуем работу по урегулированию задолженности.
            Проанализируем действующие договоры на предмет возможных претензий со стороны контрагентов и поможем их минимизировать, организуем учет исполнения обязательств.
          </p>
        </div>
        <div class="elems">
          <h3>Правовое сопровождение и контрактный менеджмент</h3>
          <p>Составим договоры в вашу пользу и с минимальной ответственностью, проконсультируем устно и письменно по вопросам в сферах гражданского, административного, корпоративного и трудового законодательства, поможем с деловой перепиской.
            Также можем взять ваш крупный или иной особо ценный договор на сопровождение «под ключ»: организуем учет исполнения обязательств, подготовим правовые заключения по любым вопросам в связи с исполнением договора, будем вести переписку и участвовать во всех переговорах с контрагентом.</p>
        </div>
        <div class="elems">
          <h3 class="mobx">Ведение<br>судебных дел</h3>
          <h3 class="desx">Ведение судебных дел</h3>
          <p>Защитим ваши интересы в суде: проанализируем спорную ситуацию, оценим перспективы, соберем доказательства и подготовим все процессуальные документы. При необходимости – организуем проведение любых экспертиз, обжалование и контроль исполнения судебного акта.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import '../../public/fonts/SegoeUI.ttf'
export default {
  name: "UslugaAl"
}
</script>

<style scoped>
.hangs {
  width: 90%;
  margin: auto;
}
.mobx {
  display: none;
}
.desx {
  display: block;
}
.contact {
  width: 96%;
  margin: auto;
  margin-top: 100px;
}

p {
  font-family: "Segoe UI";
}

h2 {
  color: #313C98;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 167.508%;
  letter-spacing: 2.206px;
}
hr {
  padding: 1px solid #242E87 ;
  background: #242E87;
}
.letsGo {
  display: flex;
  align-items: center;
  width: 100%;
  left: 0;
  position: absolute;
  right: 0;
  flex-wrap: wrap;
  align-content: stretch;
  top: 0 !important;
  justify-content: center;
  height: 100%;
}
.elems > h3 {
  color: #313C98;
  text-align: center;
  font-family: Segoe UI;
  font-size: 31.509px;
  font-style: normal;
  font-weight: 600;
  line-height: 95.008%; /* 29.936px */
  letter-spacing: 2.206px;
}
.elems {
  width: 30%;
}
.elems > p {
  color: #000;
  text-align: center;
  font-family: Segoe UI;
  margin-top: 30px;
  font-size: 14px;
  font-style: normal;
  font-weight: 300;
  line-height: 150.008%; /* 21.001px */
  letter-spacing: 0.56px;
}
.wige {
  width: 100%;
  height: 100%;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  top: 0;
  overflow: hidden;
}

.gos {
  width: 100%;
  height: 540px;
  overflow-x: hidden;
  margin: auto;
  margin-top: 20px;
  background-repeat: no-repeat;
  position: relative;
  background-size: 50%;
}

.contacta {
  position: relative;
}
.contacts {
  width: fit-content;
  background: white;
  padding: 0 12px;
  margin: auto;

  position: absolute;
  text-align: center;
  right: 0;
  top: -29px;
  left: 0;
}
.contacts > h2 {
  color: #313C98;
}

@media only screen and (max-width: 991px){
  .hangs {
    width: 145%;
    transform: rotate(50deg);
  }
  .letsGo {
    align-items: flex-start;
    position: relative;
    flex-wrap: wrap;
    align-content: flex-start;
    justify-content: center;
    flex-direction: column;
  }
  .wige {
    position: absolute;
  }
  .elems {
    width: 100%;
    margin-top: 40px;
  }
  .elems > h3, .elems  > p {
    text-align: left;

  }
  .elems > p {
    font-size: 17px;
  }
  .gos {
    width: 96%;
    height: fit-content;
  }
  .mobx {
    display: block;
  }
  .desx {
    display: none;
  }
}
</style>