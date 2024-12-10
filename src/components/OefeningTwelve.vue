<template>
  <div class="container mt-5 text-center">
    <h2>Inspirerende Quotes</h2>
    <p class="mt-4">{{ quotes[getal] }}</p>
    <button @click="Random" class="btn btn-primary">Krijg quote</button>
  </div>
</template>
<script>
import {ref} from "vue";

export default {
  setup(){
    const quotes = [
      "The best way to predict the future is to create it. - Peter Drucker",
      "Success is not the key to happiness. Happiness is the key to success. - Albert Schweitzer",
      "In the middle of every difficulty lies opportunity. - Albert Einstein",
      "Your time is limited, so don’t waste it living someone else’s life. - Steve Jobs",
      "Don’t watch the clock; do what it does. Keep going. - Sam Levenson",
      "The only way to achieve the impossible is to believe it is possible. - Charles Kingsleigh",
      "Hardships often prepare ordinary people for an extraordinary destiny. - C.S. Lewis",
      "Success usually comes to those who are too busy to be looking for it. - Henry David Thoreau",
      "The only limit to our realization of tomorrow is our doubts of today. - Franklin D. Roosevelt",
      "Believe you can and you’re halfway there. - Theodore Roosevelt"
    ];

    let getal = ref(0)

    const Random = () => {
      getal.value = Math.floor(Math. random() * 10)
    }
    return {quotes, getal, Random}
  }
}
</script>