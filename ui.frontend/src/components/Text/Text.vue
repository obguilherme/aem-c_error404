<template>
  <div :class="className">
    <div
      v-if="richText"
      :id="modelId"
      data-rte-editelement
      v-html="getRichTextContent()"
    ></div>
    <div v-else :id="modelId" data-rte-editelement v-html="text"></div>
  </div>
</template>

<script>
import DOMPurify from 'dompurify'
import extractModelId from '../../utils/extract-model-id'

export default {
  name: 'Text',
  props: {
    cqPath: {
      type: String
    },
    richText: {
      type: Boolean
    },
    text: {
      type: String
    },
    className: {
      type: String
    }
  },
  computed: {
    modelId () {
      return extractModelId(this.cqPath)
    }
  },
  methods: {
    getRichTextContent () {
      return DOMPurify.sanitize(this.text)
    }
  }
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&display=swap');

.title {
  display: flex;
  flex-direction: column;
  max-width: 30vw;
  font-family: 'Space Mono', monospace;
  font-style: normal;
  font-weight: 700;

}
.paragraph {
  display: flex;
  flex-direction: column;
  max-width: 30vw;
  font-family: 'Space Mono', monospace;
  font-style: normal;
  font-weight: 400;

}

@media all and (max-width: 414px) {
  .title {
    font-size: 64px;
    line-height: 95px;
    letter-spacing: -0.035em;
    color: #333333;
    margin-bottom: 36px;
  }
  .paragraph {
    font-size: 24px;
    line-height: 36px;
    letter-spacing: -0.035em;
    color: #4F4F4F;
    margin-bottom: 64px;
  }
}

@media all and (min-width: 1366px) {
  .title {
    font-size: 64px;
    line-height: 95px;
    letter-spacing: -0.035em;
    color: #333333;
    margin-bottom: 36px;
  }
  .paragraph {
    font-size: 24px;
    line-height: 36px;
    letter-spacing: -0.035em;
    color: #4F4F4F;
    margin-bottom: 64px;
  }
}

</style>
