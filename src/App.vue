  <template>
    <main class="container">
      <div class="form-container">
        <!-- <CustomTextInput inputName="nombre" v-model="nombreUsuario" placeholder="Ingresa un valor" /> -->
        <h1 class="title">Realiza tu préstamo</h1>
        <p class="subtitle">Ingresa el motivo</p>
        <input class="input-text" type="text" placeholder=" Vivienda, Negocio, etc">
        <p class="subtitle-value">Ingresa el valor (COP)</p>
        <InputValue/>
      </div>
    </main>
  </template>

<script>
import CustomTextInput from "./components/CustomTextInput";
import InputValue from './components/InputValue.vue';


export default {
  components: {
    // CustomTextInput,
    InputValue
  },
};
</script>

<style>
*{
  margin: 0%;
  padding: 0%;
}
 #app {
  min-height: 100vh;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  background: linear-gradient(0deg, rgba(54,212,214,1) 0%, rgba(86,45,253,1) 100%);
  align-content: center;
  justify-content: center;
  margin: 0%;
  text-align: center;
} 
.container{
  display: grid;
  place-items: center;
  width: 100%;
  height: 100vh;
}
.form-container{
  width: 500px;
  height: 400px;
  margin: auto;
  background: rgba(255, 255, 255, 0.205);
  border-radius: 10px;
  backdrop-filter: blur(100px);
}
.title{
  color: rgb(255, 255, 255);
  margin: 40px auto;
}
.subtitle{
  margin: 15px auto;
  color: #f8f8f8;
}
.subtitle-value{
  margin: 20px auto 0 auto;
  color: #f8f8f8;
}
.input-text{
  height: 30px;
  width: 300px;
  border-bottom: 1px solid #f8f8f8;
  background: none;
  border-left: none;
  border-right: none;
  border-top: none;
}
.input-text:hover{
       color: rgb(119, 119, 119);
       background-color: rgb(193, 225, 253);
       border-top-right-radius: 10px;
    }

    ::placeholder { color: #f8f8f8; }
</style>
