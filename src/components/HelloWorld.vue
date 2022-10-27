<template>
  <v-app>
    <v-app-bar :color="color" app dark>
      <v-img class="mx-10" src='../../public/logo.png' contain max-height="70" max-width="70"></v-img>
      <v-toolbar-title> Henkel REGHAIA </v-toolbar-title>
      <v-spacer></v-spacer>
      <span><strong>MOP-QC-RCV A1.00 / </strong>  Révision : <strong>02</strong> / Date : <strong>20.02.2022</strong></span>
    </v-app-bar>
      <v-container fluid>  
        <v-row class="align-center">
          <!-- <v-img src='../../public/labo3.jpg'></v-img> -->
          <v-col class="align-center">
          <v-row justify="center">
          </v-row>
               <v-card  tile class="hierarchy2 elevation-6 mt-4 d-flex flex-column">
                <v-card-text>
                <h2>Test method RCV</h2>
                <h3>Système de Management Intégré</h3>
               </v-card-text>
         </v-card>
          <v-btn class="ma-8 align-center" outlined :color="color" @click="active = !active, ChangeTitle()">{{this.text}}</v-btn>
        <v-card tile flat class="mx-6 my-6">
         <h2 class="titre">1. Objet</h2>
            <p>Cette procédure décrit les étapes à suivre pour effectuer une analyse RCV.</p>
         <h2 class="titre">2.	Domaine d'application </h2>
          <p>Cette procédure s’applique au laboratoire Henkel Reghaia.</p>
        <h2 class="titre">3. Document de Référence</h2>
         <v-list-item two-line>
            <v-list-item-content>
                <v-list-item-title><strong>- ISO 9000 :</strong></v-list-item-title>
                <v-list-item-subtitle>Systèmes de management de la qualité — Principes essentiels et vocabulaire.</v-list-item-subtitle>
                <v-list-item-title><strong>- ISO 9001 :</strong></v-list-item-title>
                <v-list-item-subtitle>Systèmes de management de la qualité — Exigences.</v-list-item-subtitle>
                <v-list-item-title><strong>- ISO 9002 :</strong></v-list-item-title>
                <v-list-item-subtitle>Systèmes de management de la qualité — Lignes directrices pour l’application de l’ISO 9001:2015.</v-list-item-subtitle>
            </v-list-item-content>
        </v-list-item>
        <h2 class="titre">4. Définitions et Abréviations</h2>
            <p>RCV : résistance à la compression verticale.</p>
        <h2 class="titre">5. Responsabilités et Autorités</h2>
        <p>Le technicien contrôle qualité est responsable sur l’analyse.</p>
        <h2 class="titre">6. Processus</h2>
         <v-list-item two-line>
                <v-list-item-content>
                    <v-list-item-title>- Centrer l’emballage entre les 02 plateaux de l’équipement.</v-list-item-title>
                    <v-list-item-title>- Utiliser les accessoires nécessaires pour les caisses et pour les flacons.</v-list-item-title>
                    <v-list-item-title>- Enregistrer l’espace entre les plateaux.</v-list-item-title>
                    <v-list-item-title>- Effectuer une série d’essai.</v-list-item-title>
                    <v-list-item-title>- Effectuer le rapport d’essai.</v-list-item-title>
                    <v-list-item-title>- Sauvegarde le rapport.</v-list-item-title>

                </v-list-item-content>
            </v-list-item>
              
            </v-card>
        </v-card>
        <v-card tile class="hierarchy2 elevation-6 mt-4 d-flex flex-column jaune">
              <v-card-text>
                <strong>PR SHEQ VR A.5-01– Procédure de Veille Réglementaire</strong> <br> <div class="red--text"> Propriété exclusive de HENKEL Algérie Unité de Production Réghaia. <br> Toute reproduction intégrale ou partielle ainsi que son utilisation par, ou la communication à, des tiers, sans accord préalable écrit de l’auteur est illicite.</div> Le R-SMI est responsable de la gestion et l’application de cette procédure.
              </v-card-text>
             </v-card>
        </v-col>
          </v-row>
        
      </v-container>

    <v-bottom-navigation v-model="value" app :background-color="color" dark :input-value="active">
      <v-btn value="1" height="100%" width="100%" :color="color">
        <span>Objet</span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="2" height="100%" width="100%" :color="color">
        <span>Domaine d’application </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="3" height="100%" width="100%" :color="color">
        <span>Document de Référence </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="4" height="100%" width="100%" :color="color">
        <span>Définitions et Abréviations </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="5" height="100%" width="100%" :color="color">
        <span>Responsabilités/Autorités </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="6" height="100%" width="100%" :color="color">
        <span>Processus </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      <v-btn value="7" height="100%" width="100%" :color="color">
        <span>Annexes </span>
        <v-icon>mdi-bookmark-outline</v-icon>
      </v-btn>
      
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    color: "#ff0011",
    active: true,
    text: "cacher le menu",
    
  }),
  methods: {
    ChangeTitle(){
      if(this.text == "cacher le menu"){
        this.text = "afficher le menu";
      }else{
        this.text = "cacher le menu";
      }
    }
  }
};
</script>

<style scoped>
.background {
  background-color: #f5eb7d;
}
.titre{
  color: #ff0011;
}
.tab{
  background-color: #fa3722;
}
</style>