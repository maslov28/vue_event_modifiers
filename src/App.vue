<template>
  <p>сверстать инпут, по клику на кнопку Enter выводить алерт с содержимым текстового поля</p>
  <input 
    type="text" 
    v-model="inputValue"
    @keypress.enter="showMessage"
  />
</template>

<script>
import {ref} from 'vue'
export default {
  setup() {
    const inputValue = ref('')

    function showMessage() {
      alert(inputValue.value)
    }

    return {
      inputValue,
      showMessage
    }
  }
}
</script>