<template>
    <div>
    <input type="number" v-model="premier"  placeholder="Premier nombre"/>
    <input v-model="signe" placeholder="Signe opératoire"/>
    <input type="number" v-model="deuxieme" placeholder="Second nombre"/>
    <span> {{premier}} {{signe}} {{deuxieme}} = {{operationResult}}</span>
    </div>
</template>

<script>
export default {
    name: 'Calculette',
    data: function() {
        return {
            premier: 1,
            signe: '+',
            deuxieme: 2,
            resultat: 0,
        }
    },
    computed: {
        operationResult() {
            switch(this.signe) {
                case '+':
                    return parseInt(this.premier) + parseInt(this.deuxieme);
                case '-':
                    return parseInt(this.premier) - parseInt(this.deuxieme);
                case '*':
                    return parseInt(this.premier) * parseInt(this.deuxieme);
                case '/':
                    return parseInt(this.premier) / parseInt(this.deuxieme);
                default:
                    return 0;
            }  
        }
    },
    methods: {
        addition(int1, int2) {
            this.resultat = int1 + int2;
        }
    }
}
</script>

<style>

</style>