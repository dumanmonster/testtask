<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div class="header">
    <div class="header__block"></div>
    <div class="header__nav">
      <RouterLink class="header__nav-item" to="/favorites">
        <img src="./assets/icons/favorites.svg" alt="Favorites" />
        <span class="header__nav-item-text">Избранное</span>
      </RouterLink>
      <RouterLink class="header__nav-item" to="/stock">
        <img src="./assets/icons/stock.svg" alt="Stock" />
        <span class="header__nav-item-text">Склад</span>
      </RouterLink>
      <RouterLink class="header__nav-item" to="/deals">
        <img src="./assets/icons/deals.svg" alt="Deals" />
        <span class="header__nav-item-text">Сделки</span>
      </RouterLink>
    </div>
  </div>
  <RouterView />
</template>

<style lang="scss" scoped>
@import '@/assets/_variables.scss';
.header {
  display: flex;
  gap: 20px;
  flex-direction: column;
  &__block {
    background-color: #e0e3ee;
    height: 40px;
    border-radius: 0px 0px 10px 10px;
  }
  &__nav {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-items: center;

    &-item {
      position: static;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      height: 50px;
      width: 86px;
      gap: 5px;
      border-radius: 10px;
      padding: 6px 0px 7px 0px;
      text-decoration: none;
      &-text {
        font-size: 13px;
        font-weight: 500;
        color: $primary-text;
      }
      &:hover {
        background-color: $primary-background;
      }
    }
  }
}
</style>
