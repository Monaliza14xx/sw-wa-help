<template>
  <center>
    <img width="250px" src="@/assets/logo.jpeg" alt="" />
    <h2 id="text">WhatsApp help</h2>
    <p id="text">ພຽງແຕ່ທ່ານປ້ອນເບີໂທ ແລະ ຂໍ້ຄວາມ ກໍ່ສາມາດສົ່ງຂໍ້ຄວາມໄດ້</p>
    <v-text-field
      v-model="phoneNumber"
      label="ເບີໂທລະສັບ"
      placeholder="ກະລຸນາໃສ່ເບີໂທ ຕົວຢ່າງ: 020xxx ຫຼື 20xxx"
      :rules="[{ required: true }]"
      rounded
      outlined
      maxlength="11"
    />
    <v-text-field
      v-model="msg"
      label="ຂໍ້ຄວາມ"
      placeholder="ກະລຸນາໃສ່ຂໍ້ຄວາມທີ່ຢາກສົ່ງ"
      :rules="[{ required: true }]"
      outlined
      rounded
    />
    <v-btn
      height="8vh"
      width="100%"
      depressed
      rounded
      @click="onSubmit"
      color="#169fc6"
      ><h3 class="white--text">ສົ່ງຂໍ້ຄວາມ</h3></v-btn
    >
  </center>
</template>

<script>
export default {
  layout: 'empty',
  data() {
    return {
      code: '+856',
      phoneNumber: null,
      msg: null,
      url: 'https://api.whatsapp.com/send',
    }
  },
  methods: {
    onSubmit() {
      if (this.phoneNumber == null || this.msg == null) {
        alert('ກະລຸນາປ້ອນເບີໂທ ແລະ ຂໍ້ຄວາມ')
      } else {
        window.location.href =
          this.url +
          '/?phone=' +
          this.code +
          this.phoneNumber +
          '&text=' +
          this.msg
      }
    },
  },
}
</script>

<style>
</style>