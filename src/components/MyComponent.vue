<template>
    <div class="main">
      <input v-model="prompt" type="text" placeholder="Inserisci la tua richiesta" />
      <button class="btn_invia" @click="sendRequest">Invia richiesta</button>
      <div class="risposta">
        <p v-if="response">{{ response }}</p>
      </div>
      
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  import { OPENAI_API_KEY } from '@/config';
  
  export default {
    data() {
      return {
        prompt: '',
        response: ''
      }
    },
    methods: {
      sendRequest() {
        axios({
          method: 'post',
          url: 'https://api.openai.com/v1/engines/text-davinci-003/completions',
          headers: { 'Authorization': `Bearer ${OPENAI_API_KEY}` },
          data: {
            prompt: this.prompt,
            max_tokens: 500
          }
        }).then(response => {
          this.response = response.data.choices[0].text;
        }).catch(error => {
          console.log(error);
        });
        this.prompt = '';
      }
    }
  }
  </script>

  <style scoped lang="scss">

  .main{
      height: 50% ;
      width:100%;
      padding: 30px 0px;
  }

  input{
      width: 90%;
      height: 40px;
      border: 1px solid #232323;
      border-radius: 4px;
      background-color: #16fe06;
      color: black;
      padding: 10px;
      text-align: left;
      border-radius: 45px;
      text-decoration-color: #232323;
  }

  .btn_invia{
      display: block;
      margin-left: 5%;
      height: 40px;
      width: 200px;
      background-color: yellow;
      margin-top: 30px;
      text-align: left;
      padding: 10px;
      border-radius: 45px;
  }

  .risposta{
      width: 100%;
      padding: 30px;
      margin: auto;
      
      p{
          text-align: center;
      }
  }







    
</style>
  