<script setup lang="ts">
import { ref } from 'vue';
import { useTranslate } from '@demo/use-translate';

const i18n = {
  'zh-CN': {
    text: '文本',
    inputAlign: '输入框内容对齐',
    alignPlaceHolder: '输入框内容右对齐',
  },
  'en-US': {
    text: 'Text',
    inputAlign: 'Input Align',
    alignPlaceHolder: 'Input Align Right',
  },
};

const t = useTranslate(i18n);
const value = ref('');
</script>

<template>
  <demo-block :title="t('inputAlign')">
    <van-cell-group inset>
      <van-field
        v-model="value"
        :label="t('text')"
        :placeholder="t('alignPlaceHolder')"
        input-align="right"
      />
    </van-cell-group>
  </demo-block>
</template>
