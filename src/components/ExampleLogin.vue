<template>
    <div>
      <label>
      Введіть логін
      <input type="text" v-model="userLogin">
      </label> <br>

      <label>
      Введіть пароль
      <input type="password" v-model.number="userPass">
      </label> <br>

      <button @click="checkPass">Go</button>

      <div v-if="checkAutorize">
          <div v-if="checkAutorize===loginValue.CORRECT">
            <img :src="imageSrc" alt="picture">
          </div>
          <div v-else-if="checkAutorize===loginValue.INCORRECT_IVAN" :class="getClass()"> Невірний пароль </div>
          <div v-else :class="getClass()"> Невірний логін або пароль</div>
       </div>
    </div>
</template>

<script>
import { loginValue } from './settings.js'
    export default {
        name : 'ExampleLogin',
        props: {
            imageSrc: {
                type: String,
                default:"data:image/jpeg;base64,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"
            },
            userDataArray: {
                type:Array,
                default: ()=>[]
            }

        },
        data () {
            return {
               userLogin:null,
               userPass :null,
               checkAutorize: null,
               loginValue,
         }
        },
        methods: {
          checkPass () {
              if(
                  this.userDataArray.some(
                      (item)=> this.userLogin===item.login && this.userPass===item.pass
                  )
                ) {
              this.checkAutorize = loginValue.CORRECT
              return
                }
              if (this.userLogin === 'Ivan'){
                  this.checkAutorize = loginValue.INCORRECT_IVAN
                
                  }
                  else
                  this.checkAutorize = loginValue.INCORRECT
             },
             getClass() {
                 if (this.userLogin === 'Ivan'){ return (this.loginValue.INCORRECT_IVAN = 'blue')} else
                 {return (this.loginValue = 'red')}
             }

       }
    }
</script>

<style lang="css" scoped>
.red {
    color: red;
}
.blue {
    color: blue;
}
</style>
