<script>
  import BaseModalContainer from './BaseModalContainer'

  export default {
    components: {
      BaseModalContainer
    }
  }
</script>

<template>
  <base-modal-container class="modal">
    <div class="modal-content">
      <div class="modal-header">
        <slot name="header" />
      </div>
      <div class="modal-body">
        <slot name="body" />
      </div>
      <div class="modal-footer">
        <slot name="footer" />
      </div>
    </div>
  </base-modal-container>
</template>

<style lang="sass">
  .modal
    ::v-deep .container
      width: 100%
      height: 100%

      padding: 25px
      border-radius: 10px

  .modal-content
    width: 100%
    height: 100%
    display: flex
    justify-content: center
    align-items: center
    flex-direction: column

    .modal-header, .modal-body, .modal-footer
      display: flex
      justify-content: center
      align-items: center
      width: inherit
      padding: 10px

    .modal-header
      font-weight: bold
      font-size: 30px

    .modal-body
      font-size: 20px
</style>
