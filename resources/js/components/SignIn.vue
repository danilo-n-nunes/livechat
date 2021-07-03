<template>
  <div class="container">
      {{email}} || {{pass}}
    <div class="row justify-content-center pt-5">
        <i style="font-size: 100px" class="bi bi-person-circle text-secondary"></i>
    </div>
    <div class="form-group pt-1">
      <div class="offset-md-4 col-md-4">
        <label for="email">Email</label>
        <input
          type="text"
          class="form-control"
          id="email"
          name="email"
          v-model="email"
        />
      </div>
    </div>
    <div class="form-group">
      <div class="offset-md-4 col-md-4">
        <label for="pass">PassWord</label>
        <input
          type="text"
          class="form-control"
          id="pass"
          name="pass"
          v-model="pass"
        />
        <label v-if="error" class="text-danger">Login e/ou senha incorreto(s)</label>
      </div>
    </div>
    <div class="row pt-2">
        <div class="col-md-4 offset-md-4">
            <button @click="login()" class="btn btn-primary btn-lg btn-block">Login</button>
        </div>
    </div>
    <div class="row pt-1 justify-content-center">
        <a href="/signup">Ainda não tem conta? Registre-se</a>
    </div>
    <div class="row pt-1 justify-content-center">
        <a href="#">Esqueceu a senha?</a>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      email: "",
      pass: "",
      error: false
    };
  },
  methods: {
      login(){
          console.log('preparando a conexão!');
          //axios.get("http://tuacor.com")
          
          if(this.email == "danilo@gmail.com" && this.pass == "123456"){
              window.location = '/home'
          }else{
              this.error = true
          }
      }
  },
  mounted(){
      //axios.get("http://tuacor.com")
      console.log('montado')
  }
};
</script>

<style>
</style>