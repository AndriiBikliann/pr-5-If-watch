<template>
    <div class="container"
      :class="{
          'right': corecttanslate === true
      }"
    >
        
        
       <div>
           <img :src="imageSrc" alt="">
       </div>

       <div>
           {{enTranslate}}
       </div>

       <label>
           Ваш переклад
           <input type="text" v-model="userTranslate">
       </label>

       <div>
           <button @click="checkTranslate">
               Перевірити
           </button>
       </div>

       <div v-if="corecttanslate">
           Вірно
       </div>

       <div v-if="incorecttanslate">
           Не вірно
       </div>

    </div>
</template>

<script>
    export default {
        name: "WordCard",
        props: {
            imageSrc: {
                type: String,
                default: 'no image'
            },
            enTranslate: {
                type:String,
                default:null
            },
            uaTranslate: {
                type: String,
                default:null
            }
        },
        data() {
            return {
                userTranslate: null,
                corecttanslate: null,
                incorecttanslate: null
            }
        },
        methods: {
            checkTranslate() {
                if (this.userTranslate === this.uaTranslate) {
                return (this.corecttanslate = true);
                } else {
                return (this.incorecttanslate = true);
                }
            }
        },
    }
</script>

<style lang="css" scoped>
img {
    width: 150px;
    height: 150px;
}
.right {
    background-color: green;
}


</style>