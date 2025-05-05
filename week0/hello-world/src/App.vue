<template>
  <!-- "Mustache"(이중 중괄호) 문법 -->
  <button @click="onClick">{{ text }}</button>
</template>

<script setup lang="ts">
import { ref } from "vue";

const text = ref("CLICK!");

function onClick() {
  text.value = "Hello World";
  // text.value가 업데이트 되어 바로 사용될 수 있음
  /**
   * 간단한 예제:
   * const text = {
      _value: ‘',
      value: {
        get() {
          return this._value;
        }, 
        set(v) {
          // Vue: 화면을 업데이트 해주세요
          // 화면 업데이트는 배치 작업을 통해 모아서 업데이트 되어서 딜레이가 있다
          this._value = v;
        }
      }
    }
   */
  window.alert(text.value);
}
</script>

<style></style>
