<template>
  <div class="container">
    {{ email }}
    <div class="row justify-content-center pt-5">
      <h3>Digite seu Email para Recuperação</h3>
    </div>
    <div class="row justify-content-center">
      <div class="form-group pt-2">
        <label for="recmail">Email</label>
        <input
          type="text"
          id="email"
          class="form-control"
          name="email"
          v-model="email"
        />
      </div>
    </div>
    <div class="row justify-content-center">
      <button class="btn btn-warning btn-lg m-2">Enviar</button>
    </div>
    <div class="row justify-content-center pt-2">
        <a href="/signin">Lembrei minha senha!</a>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      email: "",
    };
  },
};
</script>

<style>
</style>