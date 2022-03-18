<template>
	<base-layout titleProp="All my memories">
		<h2>These are my memories</h2>
		<ion-list>
			<ion-item
				v-for="memory in memories"
				:router-link="`/memories/${memory.id}`"
				:key="memory.id"
			>
			<ion-img :src="memory.image"></ion-img>
			{{memory.title}}</ion-item>
		</ion-list>
	</base-layout>
</template>

<script>
import {IonList, IonItem, IonImg} from "@ionic/vue";
export default {
	components:{
		IonList, IonItem, IonImg
	},
	data(){
		return{
			memories:[
				{id:"m1", title:"Artcal'O memory", image:"artcalo.jpeg",description:"Description Memory"},
				{id:"m2", title:"Ange memory", image:"../../public/assets/img/njenje.jpeg",description:"Description Memory"},
				{id:"m3", title:"Marley memory", image:"../../public/assets/img/togos.jpeg",description:"Description Memory"},
				{id:"m4", title:"TheIko memoriy", image:"../../public/assets/img/iko.jpeg",description:"Description Memory"},
				{id:"m5", title:"TutuBunso memoriy", image:"../../public/assets/img/tutu.jpeg",description:"Description Memory"},
			]
		}
	}
};
</script>

<style lang="css" scoped>
</style>
