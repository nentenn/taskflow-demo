<template>
  <f7-page name="help">
    <f7-navbar title="Допомога" back-link="Назад" />

    <div class="app-content">
      <div class="page-heading">
        <h1>Як користуватися TaskFlow</h1>
        <p>Основні правила роботи</p>
      </div>

      <div class="info-card">
        <h3>Головна сторінка</h3>
        <p>
          Показує кількість усіх, виконаних і невиконаних
          завдань, а також три останні завдання.
        </p>
      </div>

      <div class="info-card">
        <h3>Сторінка завдань</h3>
        <p>
          Містить повний список завдань з описами.
          Зелена позначка означає, що завдання виконано.
        </p>
      </div>

      <div class="info-card">
        <h3>Навігація</h3>
        <p>
          Використовуйте нижню панель для переходів
          між основними сторінками.
        </p>
      </div>

      <div class="info-card">
        <h3>Демонстраційні дані</h3>
        <p>
          На цьому етапі додавання, редагування
          та видалення завдань недоступні.
        </p>
      </div>
    </div>

    <AppTabbar active="about" />
  </f7-page>
</template>

<script setup>
import AppTabbar from '../components/AppTabbar.vue';
</script>