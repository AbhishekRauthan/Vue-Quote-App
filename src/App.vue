<template>
  <div class="container">
    <NewQuoteVue @quoteAdded="AddNewQuote" />
    <QuoteGridVue :quotes="quotes" />
  </div>
</template>

<script>
import QuoteGridVue from "./components/QuoteGrid.vue";
import NewQuoteVue from "./components/NewQuote.vue";

export default {
  data: function() {
    return {
      quotes: [
        "some quote to see something",
        "some quote to see something",
        "some quote to see something",
        "some quote to see something",
        "some quote to see something",
        "some quote to see something",
      ],
      maxQuoutes: 10,
    };
  },
  methods: {
    AddNewQuote(qoute) {
      this.quotes.push(qoute);
    }
  },
  components: {QuoteGridVue, NewQuoteVue},
};
</script>

<style></style>
