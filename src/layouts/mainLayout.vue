<template>
  <div class="w-full">
    <MainHeader />

    <Slider />

    <div class="cards my-32">
      <div class="cards_row -mx-1">
        <Card
            v-for="card in cards"
            :key="card.id"
            :card = card
        />
      </div>

    </div>

    <MainFooter />
  </div>
</template>

<script>
import MainHeader from '@/components/mainHeader'
import MainFooter from '@/components/mainFooter'
import Card from '@/components/card'
import Slider from '@/components/slider'

export default {
  data() {
    return {
      cards: [
        {
          id: 1,
          title: "First Name",
          subtitle: "Other",
          date: "26 November 13:00 - 15:00 ",
          location: "Cathouse",
          price: '30.00 EUR',
          image: "1.webp",
          isSoon: false,
          isPopular: false,
          isNew: false
        },
        {
          id: 2,
          title: "Another name",
          subtitle: "Other",
          date: "26 November 13:00 - 15:00 ",
          location: "Cathouse",
          price: '30.00 EUR',
          image: "2.webp",
          isSoon: false,
          isPopular: true,
          isNew: false
        },
        {
          id: 3,
          title: "Default name",
          subtitle: "Other",
          date: "26 November 13:00 - 15:00 ",
          location: "Somewhere",
          price: '30.00 EUR',
          image: "1.webp",
          isSoon: false,
          isPopular: false,
          isNew: true
        },
        {
          id: 4,
          title: "Funny Bunny",
          subtitle: "Other",
          date: "Some date",
          location: "Venekultuuri Keskus ",
          price: '30.00 EUR',
          image: "2.webp",
          isSoon: false,
          isPopular: false,
          isNew: false
        },
        {
          id: 5,
          title: "Looks fine",
          subtitle: "Other",
          date: "26 August 03:00",
          location: "Somewhere",
          price: '30.00 EUR',
          image: "3.webp",
          isSoon: true,
          isPopular: false,
          isNew: true
        },
        {
          id: 6,
          title: "Testing",
          subtitle: "Other",
          date: "26 August 03:00 ",
          location: "Somewhere",
          price: '30.00 EUR',
          image: "1.webp",
          isSoon: false,
          isPopular: true,
          isNew: false
        }
      ]
    }
  },
  components: {
    MainHeader,
    MainFooter,
    Card,
    Slider
  }
}
</script>

<style scoped>

  .cards {
    @apply .w-4/5 .mx-auto .flex
  }
  .cards_row {
    @apply .flex .flex-wrap .overflow-hidden
  }

</style>