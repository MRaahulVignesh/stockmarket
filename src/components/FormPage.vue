<template>
  <div class="form-page-container">
    <div class = "title-container">
        <h2>ADD CRYPTOS</h2>
    </div>
    <div class="form-container">
  <Form>
  </Form>
</div>
  </div>
</template>

<script>
import Form from './Form.vue'
  export default {
    data() {
      return {
      }
    },
    components: {
        Form
    },
  }
</script>

<style scoped>
.form-page-container {
  padding: 2rem;
  height: 80vh;
  min-height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}

.title-container {
  width: 100%;
  height: 20%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.form-container {
  border-style: solid;
  border-width: 5px;
  border-color: black;
  padding: 1rem;
  border-radius: 8px;
  width: 50%;
  height: 75%;
  min-width: 350px;
  background-color: white;
}

.title-container h2 {
    font-size: 3rem;
}

@media(max-width: 750px) {
  .form-container {
    min-width: 300px;
    width: 50%;
    height: 80%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .form-page-container {
  margin: auto;
  padding: 1rem;
}

.title-container {
  height: 15%;

}


.title-container h2 {
  font-size: 2rem;
  }
}

</style>
