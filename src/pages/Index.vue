<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-full.svg"
    >

    <q-page-sticky position="bottom-right" :offset="[18, 18]">
       <q-btn fab-mini color="green-8" icon="add" class="animate-pop" @click="newDevicePopup" />
    </q-page-sticky>

  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  methods: {
    newDevicePopup () {
      this.$q.dialog({
        title: 'Add new device',
        message: 'Enter IP address for device.',
        prompt: {
          model: '',
          type: 'text'
        },
        cancel: true,
        color: 'secondary'
      })
    }
  }
}
</script>
