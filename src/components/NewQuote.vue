<template>
  <div class="row">
    <form>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label for="inputquote">Quote</label>
        <textarea id="inputquote" class="form-control" rows="3" v-model="quote" ></textarea>
      </div>
      <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <button  @click.prevent="createNew" class="btn btn-primary">Add Quote</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      quote: ''
    }
  },
  methods: {
    createNew() {
      this.$emit('newQuote', this.quote)
      this.quote = ''
    }
  }
}
</script>

<style scoped>

</style>
