<template>
  <v-app id="default">
    <v-main>
      <v-card class="mx-auto mt-4" width="80vw">
        <v-card-title> 내가 얻을 마일리지는? </v-card-title>

        <v-btn @click="makeResult" text color="orange lighten-2"
          >계산하기</v-btn
        >

        <div style="display: flex">
          <v-img
            class="mt-1 ml-3"
            :src="img.mile"
            max-height="30"
            max-width="30"
          >
          </v-img>
          <div class="mt-2 ml-2">: {{ result }}</div>
        </div>
        <div>
          <div height="120px" class="mt-6 ml-2">
            <v-img
              class="mx-auto"
              max-height="160px"
              max-width="160px"
              :src="items.common[1]"
            ></v-img>
            <div>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="0성 개수"
                v-model="soulDustCount.noStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="1성 개수"
                v-model="soulDustCount.oneStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="2성 개수"
                v-model="soulDustCount.twoStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="3성 개수"
                v-model="soulDustCount.threeStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="4성 개수"
                v-model="soulDustCount.fourStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="5성 개수"
                v-model="soulDustCount.fiveStar.common"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="잔여 조각"
                v-model="soulDustCount.leftDust.common"
              ></v-text-field>
            </div>
          </div>
          <div height="120px" class="mt-6 ml-2">
            <v-img
              class="mx-auto"
              max-height="160px"
              max-width="160px"
              :src="items.rare[1]"
            ></v-img>
            <div>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="0성 개수"
                v-model="soulDustCount.noStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="1성 개수"
                v-model="soulDustCount.oneStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="2성 개수"
                v-model="soulDustCount.twoStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="3성 개수"
                v-model="soulDustCount.threeStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="4성 개수"
                v-model="soulDustCount.fourStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="5성 개수"
                v-model="soulDustCount.fiveStar.rare"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="잔여 조각"
                v-model="soulDustCount.leftDust.rare"
              ></v-text-field>
            </div>
          </div>
          <div height="120px" class="mt-6 ml-2">
            <v-img
              class="mx-auto"
              max-height="160px"
              max-width="160px"
              :src="items.epic[1]"
            ></v-img>
            <div>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="0성 개수"
                v-model="soulDustCount.noStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="1성 개수"
                v-model="soulDustCount.oneStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="2성 개수"
                v-model="soulDustCount.twoStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="3성 개수"
                v-model="soulDustCount.threeStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="4성 개수"
                v-model="soulDustCount.fourStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="5성 개수"
                v-model="soulDustCount.fiveStar.epic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="잔여 조각"
                v-model="soulDustCount.leftDust.epic"
              ></v-text-field>
            </div>
          </div>
          <div height="120px" class="mt-6 ml-2">
            <v-img
              class="mx-auto"
              max-height="160px"
              max-width="160px"
              :src="items.superEpic[1]"
            ></v-img>
            <div>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="0성 개수"
                v-model="soulDustCount.noStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="1성 개수"
                v-model="soulDustCount.oneStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="2성 개수"
                v-model="soulDustCount.twoStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="3성 개수"
                v-model="soulDustCount.threeStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="4성 개수"
                v-model="soulDustCount.fourStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="5성 개수"
                v-model="soulDustCount.fiveStar.superEpic"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="잔여 조각"
                v-model="soulDustCount.leftDust.superEpic"
              ></v-text-field>
            </div>
          </div>
          <div height="120px" class="mt-6 ml-2">
            <v-img
              class="mx-auto"
              max-height="160px"
              max-width="160px"
              :src="items.ancient[1]"
            ></v-img>
            <div>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="0성 개수"
                v-model="soulDustCount.noStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="1성 개수"
                v-model="soulDustCount.oneStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="2성 개수"
                v-model="soulDustCount.twoStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="3성 개수"
                v-model="soulDustCount.threeStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="4성 개수"
                v-model="soulDustCount.fourStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="5성 개수"
                v-model="soulDustCount.fiveStar.ancient"
              ></v-text-field>
              <v-text-field
                class="mx-auto"
                style="width: 280px"
                label="잔여 조각"
                v-model="soulDustCount.leftDust.ancient"
              ></v-text-field>
            </div>
          </div>
        </div>
      </v-card>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  methods: {
    makeResult: function () {
      const commonMile = 1;
      const rareMile = 2;
      const epicMile = 5;
      const superEpicMile = 7;
      const ancientMile = 10;

      const noneStar = 20;
      const oneStar = 40;
      const twoStar = 70;
      const threeStar = 120;
      const fourStar = 190;
      const fiveStar = 290;

      let commonDust =
        this.soulDustCount.noStar.common * noneStar +
        this.soulDustCount.oneStar.common * oneStar +
        this.soulDustCount.twoStar.common * twoStar +
        this.soulDustCount.threeStar.common * threeStar +
        this.soulDustCount.fourStar.common * fourStar +
        this.soulDustCount.fiveStar.common * fiveStar;

      let rareDust =
        this.soulDustCount.noStar.rare * noneStar +
        this.soulDustCount.oneStar.rare * oneStar +
        this.soulDustCount.twoStar.rare * twoStar +
        this.soulDustCount.threeStar.rare * threeStar +
        this.soulDustCount.fourStar.rare * fourStar +
        this.soulDustCount.fiveStar.rare * fiveStar;

      let epicDust =
        this.soulDustCount.noStar.epic * noneStar +
        this.soulDustCount.oneStar.epic * oneStar +
        this.soulDustCount.twoStar.epic * twoStar +
        this.soulDustCount.threeStar.epic * threeStar +
        this.soulDustCount.fourStar.epic * fourStar +
        this.soulDustCount.fiveStar.epic * fiveStar;

      let superEpicDust =
        this.soulDustCount.noStar.superEpic * noneStar +
        this.soulDustCount.oneStar.superEpic * oneStar +
        this.soulDustCount.twoStar.superEpic * twoStar +
        this.soulDustCount.threeStar.superEpic * threeStar +
        this.soulDustCount.fourStar.superEpic * fourStar +
        this.soulDustCount.fiveStar.superEpic * fiveStar;

      let ancientDust =
        this.soulDustCount.noStar.ancient * noneStar +
        this.soulDustCount.oneStar.ancient * oneStar +
        this.soulDustCount.twoStar.ancient * twoStar +
        this.soulDustCount.threeStar.ancient * threeStar +
        this.soulDustCount.fourStar.ancient * fourStar +
        this.soulDustCount.fiveStar.ancient * fiveStar;

      let mile =
        commonDust * commonMile +
        rareDust * rareMile +
        epicDust * epicMile +
        superEpicDust * superEpicMile +
        ancientDust * ancientMile;

      this.result = mile;

      console.log(mile);
    },
  },

  data: () => ({
    result: 0,

    soulDustCount: {
      noStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      oneStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      twoStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      threeStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      fourStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      fiveStar: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
      leftDust: { common: 0, rare: 0, epic: 0, superEpic: 0, ancient: 0 },
    },

    items: {
      common: [
        "https://w.namu.la/s/66ada997caa3e5135fc72fca733386e73d27b13ace648cd0d1adf19dc01b5843d4fd7641b5ae2aba8b56222936ab4d84bff62f6c56657e911bc987bc6d36cd4c9a849d7d8b09bd7cbd62bb5a77e25bf870d4e80f67ccb21a63617a2ad7103183",
        "https://w.namu.la/s/0a275bfebf156c974a06655579097909519fe37f2f6441663a3958e98b8fdec4456e1e4c67b1701a746736dfdb67fb08cfab03cc7d15cdfbd9e31cd5e5b21c50622c1dc2606c8abe980bfe1855ffb4f135bacf6387f44e8884dc43c56bae4f9a",
      ],
      rare: [
        "https://w.namu.la/s/e085f5a33d2f7595967c24d480586c12766b9646627117a2c60f11ea4fe70b6952f3705a8ea7484ae046c19d591491196bb60da80e823c524db6d57f02dd4e54e5802b3063e45b9cefc0eca0803cc8c3299c7ebb5bcafce02916b3276c911689",
        "https://w.namu.la/s/6140401883d08406d318b0fd4c7da12a48d71527cd5b36a7232628689eecd07c984d85b37c2d1c22290355367c4b46b1cee92e7d69b796c34966502a1a67a08d338246a3433e91e1714272fb7147540789ad5dec113e768958c2afff46c056c9",
      ],
      epic: [
        "https://w.namu.la/s/9b54833f623002a6f947f633285f3f1c5aab20eed6bab6b6384e30221f4cd4c8dae162f9f9f4b1e246e4fbdc8b460bcda2f85fccdce48f650538d3ad70d7084ce70e3fa7c319ec75f2f21bf2772ff17836e8698192c1e39e34039201134e53cd",
        "https://w.namu.la/s/f15fb5d92f43a1ca959897f0596475a96ab37fd5d6aac451a6baea5abb995b4a56267a7a21a1640c64a1d14c3438226ac8142c9d6fd20ef7db9d4c56ccd76550fc188f2c449b9c81952ea628c7ce0bc9acabfb3f6580249c8ea1795e14b42c4b",
      ],
      superEpic: [
        "https://w.namu.la/s/507f2ccc0f0e59b0bf61bc7a5d0321f98e01a68caccf8af57350e8f7fc5ccfae9903ab72700ed470a142df96856396fcc7e042c78256dd8933ff95823cbbc33e363f752ae2a9eb25d809df39d36bfe2a0edb79879448ed32c151bc7bf8fb089a",
        "https://w.namu.la/s/a2dd581bcd25702dffd06a1893fd45b175116491f23bd46a43274619dc21cb311fd9e45490a318ffa6bf5699325def6abb79ea9f9d87cac47098fbc35368964f74407017c638e116daac39e1570dbc0d579f94c8742d583854a22c8b5761f1e6",
      ],
      ancient: [
        "https://w.namu.la/s/4baa7777b6f871c984c9bd3c08734dfc8f0f13a044b94e6ed7a88d7de0b31e78a19070823c0c46286bbc0d7ac310750b58231c9ae2f7bde7a15d96b7aebce43237ecdc083df2cdaa4c1c5e1b76ba833a85216aa53649061e163b46e421e37f9c",
        "https://w.namu.la/s/3de46094488eae6112b9f2b96a73352efc98ac636f1018658a3ff1c3949c820b8f3b16ac3ae5e63249a543f32de9281748a6778a98f657b4ee5bdfd5571d2345a9b40eca5468ec04830a887792db64a995262e09843ba689bce11d1b397191ce",
      ],
    },

    img: {
      mile: "https://w.namu.la/s/fde49961559c380537dca2c97f0771a837843e56f3bda56bc5fab64c7d8067fd7785378762cd8e3b9d934a9ac15c798ff3464c242ae28fe5b05a93dc4e627592e18f03121a1bebf553e145ff1fdb7b4e19975ae7c87740849d7478ff536a420b",
    },
  }),
};
</script>

<style>
#default {
  font-family: "CookieRunRegular", sans-serif !important;
}
@font-face {
  font-family: "CookieRunRegular";
  src: url("@/assets/fonts/CookieRunRegular.ttf");
}
</style>
