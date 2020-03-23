<template>
    <div>
    <input v-model="text"/>
    <span>{{text|majusculeText}}</span>
    </div>
</template>

<script>
export default {
    name: 'Majuscule',
    data: function() {
        return {
            text:"Allez poto!",
            
        }
    },
    filters: {
        majusculeText(text){
            return text.toUpperCase();
        }
    }
}
</script>

<style>

</style>