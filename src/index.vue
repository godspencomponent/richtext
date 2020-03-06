<template>
  <div class="component mce-editor">
    <div v-html="scopeGet('text')"></div>
  </div>
</template>

<script>
  import {VueExtend} from 'godspen-lib'

  export default {
    mixins: [VueExtend.mixin],
    name: 'richtext',
    label: process.env.LABEL,
    style: process.env.STYLE,
    props: {
      text: {
        type: [String, Number],
        editer: {
          type: 'richtext',
          label: '文字内容',
          desc: '具体的内容数据'
        },
        default: '输入文字'
      }
    },
    computed: {
    },
    editorMethods: {
    },
    methods: {
    }
  }
</script>

<style lang="stylus" rel="stylesheet/stylus" type="text/stylus" scoped>
  @import './mce-editer.css';

  .component {
    width: 100%;
  }
</style>
