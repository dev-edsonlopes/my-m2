<template>
  <div id="main-container">
    <div id="container-left"></div>
    <div id="container-right">
      <form>
        <router-link to="/" id="logo-url">
          <img :src="logo" :alt="alt" id="logo" />
        </router-link>
        <div class="login-senha">
          <input type="email" v-model="email" placeholder="USUÁRIO" />
        </div>
        <div class="login-senha">
          <input type="password" v-model="password" placeholder="SENHA" />
        </div>
        <div class="btn">
          <input type="submit" @click="login" value="Entrar" />
        </div>
        <div class="btn">
          <input type="submit" @click="login" value="Criar conta" />
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "Login",
  props: ["logo", "alt"],
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    async login() {
        
    },
    createAccount() {

    },
  },
};
</script>
<style scoped>
#main-container {
  width: 100vw;
  height: 100vh;
  display: flex;
}
#container-left {
  width: 100%;
  height: 100%;
  position: relative;
  background-image: url("bg_login.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

#container-right {
  height: 100%;
  width: 50%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

form {
  width: 450px;
  height: 250px;
  display: flex;
  flex-direction: column;
}

form #logo {
  max-width: 400px;
  margin-bottom: 20px;
  margin-left: 25px;
}

form input {
  border: none;
  width: 100%;
  box-sizing: border-box;
  height: 35px;
  font-size: 1rem;
}
form input:focus {
  box-shadow: 0 0 0 0;
  outline: 0;
}
form .login-senha {
  margin: 10px 0px;
  border-bottom: 3px solid #50bf82;
  border-radius: 5px;
}

form > .btn {
  margin: 5px auto;
}
form > .btn > input {
  border: 1px solid #ccc;
  border-radius: 8px;
  background-color: #50bf82;
  color: #fff;
  height: 30px;
  width: 150px;
  cursor: pointer;
}
</style>