<script>
import BaseComponent from '@primevue/core/basecomponent'
import ToastStyle from '../toast/style'

export default {
  name: 'BaseToast',
  extends: BaseComponent,
  props: {
    group: {
      type: String,
      default: null
    },
    position: {
      type: String,
      default: 'top-right'
    },
    autoZIndex: {
      type: Boolean,
      default: true
    },
    baseZIndex: {
      type: Number,
      default: 0
    },
    breakpoints: {
      type: Object,
      default: null
    },
    closeIcon: {
      type: String,
      default: undefined
    },
    infoIcon: {
      type: String,
      default: undefined
    },
    warnIcon: {
      type: String,
      default: undefined
    },
    errorIcon: {
      type: String,
      default: undefined
    },
    successIcon: {
      type: String,
      default: undefined
    },
    closeButtonProps: {
      type: null,
      default: null
    },
    to: {
      type: String,
      default: null
    }
  },
  style: ToastStyle,
  provide() {
    return {
      $pcToast: this,
      $parentInstance: this
    }
  }
}
</script>
