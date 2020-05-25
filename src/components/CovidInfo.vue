<template>
  <div class="container-fluid">
    <div class="container">
      <h1 class="covid-heading">What are coronaviruses?</h1>
      <div class="row align-items-center">
        <div class="col-lg-6 col-md-12 col-sm-12">
          <p class="covid-text">
            Coronaviruses are a large family of viruses that cause illness ranging
            from the common cold to more severe diseases such as Middle East Respiratory
            Syndrome and Severe Acute Respiratory Syndrome. 2019-nCoV is a new strain
            that has not been previously identified in humans and causes COVID19/coronavirus disease.
          </p>
        </div>
        <div class="col-lg-6 col-md-12 col-sm-12 text-center">
          <img src="../assets/covid-logo.png" width="300" alt />
        </div>
      </div>
    </div>
    <div class="container-fluid">
      <h1 class="text-center mt-5">How to Protect Yourself & Others</h1>
      <div class="row mt-5">
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/Hand.png" width="120" alt />
          <p class="mt-3">
            Wash your hands often with soap and water for at least 20 seconds especially
            after you have been in a public place, or after blowing your nose, coughing,
            or sneezing.
            If soap and water are not readily available, use a hand sanitizer that contains at least 60% alcohol.
            Cover all surfaces of your hands and rub them together until they feel dry.
          </p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/close.png" width="120" alt />
          <p class="mt-3">
            Avoid close contact with people who are sick, even inside your home. If possible,
            maintain 6 feet between the person who is sick and other household members.
            Remember that some people without symptoms may be able to spread virus.
          </p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/cloth-face-cover.png" width="120" alt />
          <p class="mt-3">
            Cover your mouth and nose with a cloth
            face cover when around others. In order not to get the sickness and
            to protect other people in case you are infected.
          </p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/cough.png" width="120" alt />
          <p class="mt-3">
            If you are in a private setting and do not have on your cloth face covering, remember to always cover your mouth
            and nose with a tissue when you cough or sneeze or use the inside of your elbow.
            Throw used tissues in the trash and immediately wash your hands with soap and water for at least 20 seconds.
          </p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/touch.png" width="120" alt />
          <p
            class="mt-3"
          >Avoid touching your eyes, nose, and mouth with unwashed hands. Viruses that cause colds can enter your body this way and make you sick</p>
        </div>
        <div class="col-lg-4 col-md-6 col-sm-12 text-center mt-2 mb-2">
          <img src="../assets/phone.png" width="120" alt />
          <p class="mt-3">
            Stay home, most people with COVID-19 have mild illness and can recover at home without medical care. Do not leave your home,
            except to get medical care. Do not visit public areas. Call before you get medical care. Be sure to get care if you have trouble breathing,
            or have any other emergency warning signs, or if you think it is an emergency.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CovidInfo"
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap");
h1 {
  color: #183577;
  font-weight: bolder;
  font-family: "Bebas Neue", cursive;
  margin-top: 10% !important;
}
.covid-text {
  line-height: 2.2;
  font-size: 16px;
}
p {
  color: #183577;
  font-size: 14px;
}
.covid-image {
  img {
    width: 100px;
  }
}
</style>