<template>
 <div>
   <input v-model="cep" type="text">
   Buscando endereço para o cep {{cep}}
   {{result}}

   <ul>
     <li>Cidade: {{cidade}}</li>
   </ul>

 </div>


</template>

<script>
import axios from 'axios'

export default {
  data: function() {
    return {
      cep: '',
      result:'',
      cidade:''
    }
  },
  watch:{
    cep: function(cep){
      if (cep.length === 8) {
        axios
          .get(`https://viacep.com.br/ws/${cep}/json/`)
          .then((resposta) => {
            this.result = resposta
            this.cidade = resposta.data.localidade
          });
      }else{
        this.result = ''
        this.cidade = ''
      }
    }
  }

}

</script>
