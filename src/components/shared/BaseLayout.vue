<template>
	<ion-page>
		<ion-header>
			<ion-toolbar>
				<ion-buttons slot="start">
					<ion-back-button :default-href="defaultBackLink"></ion-back-button>
				</ion-buttons>
				<ion-title>{{titleProp}}</ion-title>
			</ion-toolbar>
		</ion-header>
		<ion-content >
			<slot/>
		</ion-content>
	</ion-page>
</template>

<script>
import {IonPage,IonHeader,IonTitle,IonToolbar,IonContent,IonBackButton,IonButtons} from "@ionic/vue";
export default {
  data() {
	return {

	};
  },
  props:["titleProp","defaultBackLink",],
  components:{
	IonPage,IonHeader,IonTitle,IonToolbar,IonContent,IonBackButton,IonButtons
  }
};
</script>

<style lang="css" scoped>
</style>
