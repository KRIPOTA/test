<script setup lang="ts">
  import { onBeforeMount, ref } from 'vue'

  import AppPageLayout from '../app/layouts/AppPageLayout.vue'

  onBeforeMount(() => {
    const tgApp = window['Telegram'].WebApp //нужно получить объект window.Telegram.WebApp Телеграмма
    tgApp.expand() //разворачиваем на все окно
    tgApp.MainButton.setText('Открыть WEP-APP') //Меняем текст на кнопке веббота в Телеграмме
    tgApp.MainButton.setParams({ color: '#000000', textColor: '#ffffff' }) // Изменяем все параметры
    console.log({ tgApp })
  })
</script>
<template>
  <AppPageLayout>
    <template #content><div>Здесь будет контент</div></template>
  </AppPageLayout>
</template>

<script setup lang="ts"></script>
