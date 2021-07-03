<template>
  <div class="container">
      {{name}} {{email}} {{pass1}} {{pass2}}
      <div class="form-group pt-5">
          <div class="col-md-4 offset-md-4">
              <label for="name">Nome</label>
              <input type="text" id="name" class="form-control" name="name" v-model="name">
          </div>
      </div>
      <div class="form-group">
          <div class="col-md-4 offset-md-4">
              <label for="emal">Email</label>
              <input type="text" id="email" class="form-control" name="email" v-model="email">
          </div>
      </div>
      <div class="form-group">
          <div class="col-md-4 offset-md-4">
              <label for="pass1">Password</label>
              <input type="text" id="pass1" class="form-control" name="pass1" v-model="pass1">
          </div>
      </div>
      <div class="form-group">
          <div class="col-md-4 offset-md-4">
              <label for="pass2">Repita o Password</label>
              <input type="text" id="pass2" class="form-control" name="pass2" v-model="pass2">
          </div>
      </div>
      <div class="row col-md-4 offset-md-4">
          <button class="btn btn-success btn-lg btn-block">
              Cadastrar
          </button>
      </div>
      <div class="row justify-content-center pt-1">
          <a href="/signin">Já possui conta? Entre</a>
      </div>
  </div>
</template>

<script>
export default {
    data: ()=>{
        return {
            name: '',
            email: '',
            pass1: '',
            pass2: ''
        }
    },
    methods: {
        cadastrar(){
            alert('cadastro')
            if(this.pass1 != this.pass2){
                alert('Passwords diferentes')
            }
        }
    },
    mounted(){
        console.log('montado')
    }
}
</script>

<style>

</style>