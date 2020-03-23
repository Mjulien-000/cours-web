<template>
    <div id="cal">
    <input v-model="distance" type="value" placeholder="Distance">
    <select v-model="unite" id="unit-select">
      <option value="">--Choisir une unite de mesure--</option>
      <option value="km">km</option>
      <option value="m">m</option>
      <option value="cm">cm</option>
      <option value="mm">mm</option>
    
    </select>
    <br>
    <span> {{distance}} {{unite}} = {{calcul}} </span>
  </div>
</template>

<script>
export default {
    name: 'ValueConvert',
    data: function() {
        return {
        distance:1,
        unite:"km",
        }
    },
    calcul(){
      if(this.unite=="km"){
        return[this.distance*1000,this.distance*100000,this.distance*1000000]
      }
      if(this.unite=="m"){
        return[this.distance/1000,this.distance*100,this.distance*1000]
      }
      if(this.unite=="cm"){
        return[this.distance/100000,this.distance/100,this.distance*10]
      }
      if(this.unite=="mm"){
        return[this.distance/1000000,this.distance/1000,this.distance/10]
      }
      return 0;
      
  }
  
  }


</script>

<style>

</style>