<template>
  <div class="row">
    <form action="">
      <div class="col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2 col-xs-12 form-control">
        <label>Quote</label>
        <textarea class="form-control" rows="3" v-bind="qoute"></textarea>
      </div>
      <div class="col-md-6 col-md-offset-3 col-sm-8 col-sm-offset-2 col-xs-12 form-control">
        <button class="btn btn-primary" @click.prevent="createNewQuote">
          Add Quote
        </button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: function () {
    return {
      quote: ''
    }
  },
  methods: {
    createNewQuote()  {
      this.$emit('quoteAdded', this.quote);
      this.quote = '';
    }
  }
};
</script>

<style></style>
