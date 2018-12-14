<template>
  <ion-button shape="round" color="primary" fill="outline" @click="showModal">Show Modal</ion-button>
</template>

<script>
export default {
  name: 'app',
  methods: {
    async showModal() {
      // ボタンがクリックされたらionicのモーダルを表示
      const loading = await this.$ionic.loadingController.create({
        spinner: 'hide',
        duration: 5000,
        message: 'Please wait...',
        translucent: true,
        cssClass: 'custom-class custom-loading'
      });
      loading.present();
    }
  }
}
</script>

<style>
</style>
