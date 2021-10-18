
<template>
  <div class="gui-card"  v-bind:style="efeitoClick" v-on:click="clickEfeito()" v-on:mouseout ="removeclickEfeito">
    <div class="gui-card__media">  
     <img class="gui-card__img" v-bind:src="imagen" alt=""/>
     </div>
    <div class="gui-card__details">
     <div class="gui-card__title">
        {{titulo}}
     </div>
     </div>
    </template>
    <script>
     export default{
         props:['titulo', 'imagem'],
         data(){
             return{
                 efeitoClick:null
             }
         },
         methods:{
             clickEfeito:function(){
            this.efeitoClick='transform:scale(1.9); margin-right:110px';
             },
             removeclickEfeito:function(){
                 this.efeitoClick=null;

             }
         }
     }
    </script>

    <style lang="scss" >
     h1{
         color:red;
     }
    </style>
 