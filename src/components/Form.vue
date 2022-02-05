<template>
  <div>
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
    <div class="form-input-container">
      <b-form-group
        id="input-group-1"
        label="Exchange:"
        label-for="input-1"
        description="The Exchange the trade was done on"
      >
        <b-form-input
          id="input-1"
          v-model="form.exchange"
          placeholder="Enter exchange "
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Last Size:" label-for="input-2" description="The amount of crypto volume done at the last price in the base currency.">
        <b-form-input
          id="input-2"
          type="number"
          v-model="form.lastsize"
          placeholder="Enter last size"
          required
        ></b-form-input>
      </b-form-group>

    <b-form-group id="input-group-3" label="Last Price:" label-for="input-3" description="The last price the last trade was executed at.">
        <b-form-input
          id="input-3"
          type="number"
          v-model="form.lastprice"
          placeholder="Enter last price"
          required
        ></b-form-input>
      </b-form-group>
      </div>
      <div class="form-button-container">
      <b-button type="submit" >Submit</b-button>
      </div>
    </b-form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          lastsize: '',
          lastprice: '',
          exchange: '',
        },
        options: [
          { item: 'T', name: 'T (last trade message)' },
          { item: 'Q', name: 'Q (top-of-book trade message)' },
        ],
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
    }
  }
</script>

<style scoped>
.form-input-container {
    margin: auto;
}
.form-button-container {
    margin: auto;
    padding-top: 1rem;
}
</style>
