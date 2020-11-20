<template>
  <transition>
    <div class="menu">
      <div class="menu_top">
          <button class="menu_top_btn" @click="closeMenu()">
            <i class="fa fa-bars"></i>
          </button>
      </div>
      <div class="menu_content">
        <ul class="menu_list first">
          <li><a href="#">Отмены и переносы</a></li>
          <li><a href="#">Условия возврата</a></li>
          <li><a href="#">Артисты</a></li>
          <li><a href="#">Площадки</a></li>
        </ul>
        <ul class="menu_list">
          <li><a href="#">О компании</a></li>
          <li><a href="#">Контакты</a></li>
          <li><a href="#">Кассы</a></li>
          <li><a href="#">Реквизиты</a></li>
          <li><a href="#">Способы оплаты</a></li>
          <li><a href="#">Электронный билет</a></li>
          <li><a href="#">Публичная оферта</a></li>
          <li><a href="#">Политика конфиденциальности</a></li>
          <li><a href="#">Субагенткий договор</a></li>
        </ul>
        <ul class="menu_list">
          <li><a href="#">Подарочные сертификаты</a></li>
          <li><a href="#">Промокоды</a></li>
          <li><a href="#">Баннеры</a></li>
        </ul>
        <ul class="menu_list">
          <li><a href="#">Корпоративным клиентам</a></li>
          <li><a href="#">ЛК организатора</a></li>
          <li><a href="#">Партнерская программа</a></li>
        </ul>
      </div>

    </div>
  </transition>
</template>

<script>
export default {
  name: "menu",
  methods: {
    closeMenu() {
      this.$emit('closeMenu')
    }
  }
}
</script>

<style>
.menu {
  @apply .w-full .bg-gray-400 .text-black .absolute .top-0 .left-auto .z-50 .fixed
}
.menu_list {
  @apply .pt-6
}
.first {
  @apply .pt-16
}
.menu_list li {
  @apply .p-3 .w-full
}
.menu_list li:hover {
  @apply .bg-gray-600 .text-blue-200 .cursor-pointer
}
.menu_top {
  @apply .fixed .h-16 .w-full .flex .bg-gray-400
}
.menu_top_btn {
  @apply .text-2xl .ml-6 .text-black
}
.menu_content {
  @apply .overflow-auto;
  scrollbar-width: none;
  max-height: 100%;
}



</style>