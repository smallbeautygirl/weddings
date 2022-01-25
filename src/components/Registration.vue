<template>
  <section class="page-section" id="registration">
    <div class="container">
      <div class="text-center">
        <h2 class="section-heading text-uppercase">報名表</h2>
        <!-- <h3 class="section-subheading text-muted">
          Lorem ipsum dolor sit amet consectetur.
        </h3> -->
      </div>
      <form @submit.prevent="submit">
        <div class="formField">
          <p class="subtitle-2"><span class="text-red">*</span>姓名</p>
          <v-text-field
            v-model="name"
            :counter="5"
            label="姓名"
            :error-messages="errors"
            required
          ></v-text-field>
          <p class="subtitle-2"><span class="text-red">*</span>手機</p>
          <v-text-field
            v-model="phoneNumber"
            :counter="10"
            label="手機"
            :error-messages="errors"
            required
          ></v-text-field>
          <p class="subtitle-2"><span class="text-red">*</span>E-mail</p>
          <v-text-field
            v-model="email"
            :error-messages="errors"
            label="E-mail"
            type="email"
            required
          ></v-text-field>
          <p class="subtitle-2">
            <span class="text-red">*</span>是否參加婚禮？
          </p>
          <v-radio-group v-model="isParticipate">
            <v-radio label="參加" value="2"></v-radio>
            <v-radio label="不參加" value="1"></v-radio>
          </v-radio-group>
          <div v-show="isParticipate > 1">
            <p class="subtitle-2">
              <span class="text-red">*</span>與新人的關係
            </p>
            <v-radio-group v-model="relationship">
              <v-radio label="男方親友" value="男方親友"></v-radio>
              <v-radio label="女方親友" value="女方親友"></v-radio>
            </v-radio-group>
            <p class="subtitle-2">
              <span class="text-red">*</span>出席人數 (包含自己)
            </p>
            <v-text-field
              v-model="people"
              :error-messages="errors"
              type="number"
              required
            ></v-text-field>
            <p class="subtitle-2">
              <span class="text-red">*</span>是否需要紙本喜帖?
            </p>
            <v-radio-group v-model="weddingInvitation">
              <v-radio label="是，我想收到紙本的喜帖" :value="true"></v-radio>
              <div v-show="weddingInvitation">
                <v-text-field
                  v-model="address"
                  :error-messages="errors"
                  label="地址 (限臺灣)"
                  required
                ></v-text-field>
              </div>
              <v-radio
                label="否，我想收到電子的喜帖就好"
                :value="false"
              ></v-radio>
            </v-radio-group>
            <p class="subtitle-2"><span class="text-red">*</span>喜餅選擇</p>
            <v-radio-group v-model="weddingCake">
              <v-radio label="中式" value="中式"></v-radio>
              <v-radio label="西式" value="西式"></v-radio>
            </v-radio-group>
            <p class="subtitle-2">
              <span class="text-red">*</span>是否需遊覽車接送?
            </p>
            <v-radio-group v-model="carPickUp">
              <v-radio label="是" value="2"></v-radio>
              <div v-show="carPickUp > 1">
                <p class="subtitle-2">
                  <span class="text-red">*</span>搭乘地點
                </p>
                <v-radio-group v-model="place">
                  <v-radio label="屏東" value="屏東"></v-radio>
                  <v-radio label="高雄" value="高雄"></v-radio>
                  <v-radio label="台南" value="台南"></v-radio>
                  <!-- <v-radio label="其他" :value="true"></v-radio>
                  <div v-show="place">
                    <v-text-field
                      v-model="otherPlace"
                      :error-messages="errors"
                      label="搭乘地點"
                      required
                    ></v-text-field>
                  </div> -->
                </v-radio-group>
              </div>
              <v-radio label="否" value="1"></v-radio>
            </v-radio-group>
            <p class="subtitle-2">
              <span class="text-red">*</span>是否有特殊飲食需求?
            </p>
            <v-radio-group v-model="specialDietaryNeeds">
              <v-radio label="是，請安排素食餐點" value="2"></v-radio>
              <div v-show="specialDietaryNeeds > 1">
                <v-text-field
                  v-model="vegetarianDiet"
                  :error-messages="errors"
                  label="需求人數"
                  type="number"
                  required
                ></v-text-field>
              </div>
              <v-radio label="否，沒有特殊飲食限制" value="1"></v-radio>
            </v-radio-group>
            <p class="subtitle-2">
              <span class="text-red">*</span>是否有特殊座位需求?
            </p>
            <v-radio-group v-model="specialSeatingRequirements">
              <v-radio label="是，需要兒童座椅或餐具" value="2"></v-radio>
              <div v-show="specialSeatingRequirements > 1">
                <v-text-field
                  v-model="childSeat"
                  :error-messages="errors"
                  label="兒童座椅數量"
                  type="number"
                  required
                  class="vText"
                ></v-text-field>
                <v-text-field
                  v-model="childCutlery"
                  :error-messages="errors"
                  label="兒童餐具數量"
                  type="number"
                  required
                ></v-text-field>
              </div>
              <v-radio label="否，沒有特殊飲食限制" value="1"></v-radio>
            </v-radio-group>
          </div>
        </div>
        <p class="subtitle-2"><span class="text-red">*</span>給新人的話</p>
        <v-text-field
          v-model="message"
          :error-messages="errors"
          required
        ></v-text-field>
        <!-- <v-checkbox
          v-model="checkbox"
          :error-messages="errors"
          value="1"
          label="Option"
          type="checkbox"
          required
        ></v-checkbox> -->

        <v-btn class="mr-4" type="submit" :disabled="invalid"> submit </v-btn>
        <v-btn @click="clear"> clear </v-btn>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  data: () => ({
    invalid: false,
    errors: "",
    isParticipate: "",
    name: "",
    phoneNumber: "",
    email: "",
    relationship: "",
    people: 1,
    message: "新娘好漂釀",
    weddingInvitation: false,
    carPickUp: "",
    address: "",
    select: null,
    items: ["Item 1", "Item 2", "Item 3", "Item 4"],
    checkbox: null,
    place: "",
    specialDietaryNeeds: "",
    vegetarianDiet: "",
    specialSeatingRequirements: "",
    childSeat: "",
    childCutlery: "",
    otherPlace: "",
    weddingCake: "",
  }),

  methods: {
    submit() {
      this.$refs.observer.validate();
    },
    clear() {
      this.name = "";
      this.phoneNumber = "";
      this.email = "";
      this.select = null;
      this.checkbox = null;
      this.$refs.observer.reset();
    },
  },
};
</script>

<style scoped>
.formField {
  font-family: "Architects Daughter", cursive;
}
.subtitle-2 {
  margin-bottom: 3px;
}
.vText {
  margin-bottom: 1px;
}
</style>
