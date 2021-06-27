<template>
    <div>
       <h3>Авіаквитки</h3>
       <h4>оберіть клас для подорожі</h4>
       <div>
           <select v-model="ticketsType">
              <option value="business">Бізнес клас</option>
              <option value="econom">Економ клас</option>
           </select>
       </div>

       <div v-if="ticketsType === 'business'">
           <select v-model="businessOption">
              <option value="conyak">Коньяк</option>
              <option value="newspaper">Преса</option>
           </select>
       </div>

       <div v-if="businessOption === 'conyak' ">
           <select >
              <option value="food">Аперетив</option>
              <option value="ice">Лід</option>
           </select>
       </div>

       <div v-if="ticketsType === 'econom'">
           <select>
              <option value="beer">Пиво</option>
              <option value="chips">Чіпси</option>
           </select>
       </div>

    </div>
</template>

<script>
    export default {
        name: 'AviaTickets',
        data() {
            return {
                ticketsType: null,
                businessOption: null
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>