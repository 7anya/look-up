<template>
  <div>
    <md-dialog-confirm
      :md-active.sync="active"
      md-title="Details of xxxx"
      md-content="Let Google help apps determine location. <br> This means sending <strong>anonymous</strong> location data to Google, even when no apps are running."
      md-confirm-text="Agree"
      md-cancel-text="Disagree"
      @md-cancel="onCancel"
      @md-confirm="onConfirm" />

    <md-button class="md-primary md-raised" @click="active = true">Details</md-button>
    <span v-if="value">Value: {{ value }}</span>
  </div>
</template>

<script>
  export default {
    name: 'DialogConfirm',
    data: () => ({
      active: false,
      value: null
    }),
    props: {
      name: String
    },
    methods: {
      onConfirm () {
        this.value = 'Agreed'
      },
      onCancel () {
        this.value = 'Disagreed'
      }
    }
  }
</script>