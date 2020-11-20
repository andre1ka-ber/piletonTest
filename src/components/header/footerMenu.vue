<template>
  <div class="footer_menu">
      <ul>
        <li><i class="fa fa-calendar"></i><p>Календарь</p></li>
        <li><i class="fa fa-filter"></i><p>Фильтры</p></li>
        <li><i class="fa fa-search"></i><p>Поиск</p></li>
      </ul>
  </div>
</template>

<script>
export default {
  name: "footerMenu"
}
</script>

<style scoped>
.footer_menu {
  @apply .h-16 .w-full .flex .justify-center .items-center .fixed .bottom-0 .bg-white .z-50
}
.footer_menu ul,
.footer_menu ul li {
  @apply .justify-center .items-center .w-full
}
.footer_menu ul li {
  @apply .w-1/3
}
.footer_menu ul li i {
  @apply
}
.fa {
  @apply .mr-5
}
</style>