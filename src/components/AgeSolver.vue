<template>
    <div>
       <span v-if="isPensioner"> Можете відпочивати</span>
       <span v-else> Вам потрібно працювати</span>
    </div>
</template>

<script>
    export default {
        name : 'AgeSolver',
        props : {
            userAge: {
                type : Number,
                default : 0,
            },
            pensionerAge: {
                type: Number,
                default: 65,
            }
        },
        computed : {
            isPensioner(){
            return this.userAge>this.pensionerAge
            }
        }

    }
</script>

<style lang="scss" scoped>

</style>