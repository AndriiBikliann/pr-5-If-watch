<template>
    <div>
       <div>
           <h4>Оберіть категорію транспорту</h4>
           <select v-model="ticketCategory">
              <option value="bus">Автобус</option>
              <option value="plane">Літак</option>
              <option value="train">Поїзд</option>
           </select>
       </div>

       <div v-if="ticketCategory === 'bus'">
            <div>
                <h5>Оберіть місце у автобусі</h5>
                <input type="number">
            </div>
            <div>
                 <h5>Бажаєте замовити сніданок?
                 так <input type="checkbox" value="Так">
                 ні  <input type="checkbox" value="Ні">
                </h5>
           </div>
            <div>
                 <h5>Бажаєте замовити чай?
                 так <input type="checkbox" value="Так">
                 ні  <input type="checkbox" value="Ні">
                </h5>
           </div>
           <div>
                <h5>Бажаєте замовити wi-fi?
                 так <input type="checkbox" value="Так">
                 ні  <input type="checkbox" value="Ні">
                </h5>
           </div>
       </div>

       <div v-if="ticketCategory === 'plane'">
           <h4>Оберіть клас літака</h4>
           <select>
              <option value="econom">Економ</option>
              <option value="standart">Стандарт</option>
              <option value="business">Бізнес</option>
           </select>
           <div>
                <h5>Оберіть місце у літаку</h5>
                <input type="number">
            </div>
       </div>

       <div v-if="ticketCategory === 'train'">
           <h4>Оберіть вид вагону</h4>
           <select>
              <option value="stateroom">Купе</option>
              <option value="common">Плацкарт</option>
           </select>
           <div>
                <h5>Бажаєте замовити чай?
                 так <input type="checkbox" value="Так" checked>
                 ні  <input type="checkbox" value="Ні" checked>
                </h5>
           </div>
           <div>
                <h5>Постільну білизну потрібно?
                 так <input type="checkbox" value="Так" checked>
                 ні  <input type="checkbox" value="Ні" checked>
                </h5>
           </div>
       </div>


    </div>
</template>

<script>
    export default {
        
         name: 'TicketForm',
         data() {
            return {
                ticketCategory: null,
            }
        }
    }
</script>

<style lang="css" scoped>

</style>