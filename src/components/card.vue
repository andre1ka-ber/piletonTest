<template>
  <div class="card">
    <div class="card_wrapper">
      <div class="card_stat absolute">
        <span class="card_stat_sub soon" v-if="card.isSoon">SOON</span>
        <span class="card_stat_sub new" v-if="card.isNew">NEW</span>
        <span class="card_stat_sub popular" v-if="card.isPopular">POPULAR</span>
      </div>
      <a href="#">
        <div class="card_img">
          <img :src="require('../assets/images/cards/' + card.image)" alt="card image">
        </div>
        <div class="card_data">
          <div class="card_title">
            <h4>{{ card.title }}</h4>
            <p class="card_small_title"><small>{{ card.subtitle }}</small></p>
          </div>
          <div class="card_info">
            <div>
              <i class="fa fa-calendar-o"></i>
              <span>{{ card.date }}</span>
            </div>
            <div>
              <i class="fa fa-location-arrow"></i>
              <span>{{ card.location }}</span>
            </div>
            <div>
              <i class="fa fa-euro"></i>
              <span>{{ card.price }}</span>
            </div>
          </div>
        </div>
      </a>
      <button class="buy_btn">Buy ticket</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",
  props: ['card']
}
</script>

<style scoped>
  .card {
    @apply .my-1 .w-1/2 .overflow-hidden
  }
  .card_wrapper {
    @apply .border .border-gray-300 .rounded-b .mx-1
  }
  .card_img {
    @apply .w-full
  }
  .card_data {
    @apply .m-2
  }
  .card_title {
    @apply .font-bold
  }
  .card_small_title {
    @apply .text-sm .font-medium .text-gray-500
  }
  .card_info {
    @apply .my-2 .text-gray-800
  }
  .card_info span {
    @apply .text-gray-700 .ml-3 .text-sm
  }
  .card_stat_sub {
    @apply  .p-1 .mx-px .rounded .text-white .text-xs
  }
  .buy_btn {
    @apply .w-full .text-white .rounded .py-1
  }
  .buy_btn:hover {
    @apply .bg-green-500
  }


  .soon {
    background-color: orange;
  }
  .new {
    background-color: dodgerblue;
  }
  .popular, .buy_btn {
    background-color: limegreen;
  }
  .card_title {
    line-height: 1.2;
  }
</style>