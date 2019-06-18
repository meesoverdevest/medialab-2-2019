<template>
  <v-app dark>
    <v-toolbar class="dark">
      <v-toolbar-title v-text="title"></v-toolbar-title>
    </v-toolbar>
    <v-content>
      <section>
        <v-parallax :src="require('./assets/Melkamer2.jpg')" height="500">
          <v-layout
            column
            align-center
            justify-center
            class="black--text"
          >
            <h1 class="mb-2 display-1 text-xs-center">Obserbird</h1>
            <div class="subheading mb-3 text-xs-center font-weight-medium">Jouw kleine vriend in surveillance!</div>
            <v-btn
              class="green lighten-1 mt-5"
              dark
              large
              href="/pre-made-themes"
            >
              Optimaliseer uw surveillance
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-layout column wrap class="my-5" align-center>
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline">Waarom de Obserbird?</h2>
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">data_usage</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Altijd in contact met hulpdiensten</div>
                    </v-card-title>
                    <v-card-text>
                      Met behulp van de Obserbird is het mogelijk om altijd in contact te staan met de benodigde hulpdiensten.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">satellite</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Een overzicht voor de hulpdiensten</div>
                    </v-card-title>
                    <v-card-text>
                      Overzicht voor de mensen in de meldkamer
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">build</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Ingrijpen voor het mis gaat</div>
                    </v-card-title>
                    <v-card-text>
                      Voordat situaties escaleren kunnen de hulpdiensten al inschakelt worden.
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

	  <section>
        <v-layout column wrap class="my-5" align-center>
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline">Team</h2>
              <!-- <span class="subheading">We make it possible!</span> -->
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap>
                <v-flex xs12 md6>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
      					  	<v-avatar size="180" color="grey lighten-4">
      							 <img alt="avatar">
      						  </v-avatar>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Mees Overdevest</div>
                    </v-card-title>
                    <v-card-text>
                      Verhaal
                    </v-card-text>
                    <v-card-text>
                      <p></p>
                    </v-card-text>
                  </v-card>
                </v-flex>

                <v-flex xs12 md6>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
        						<v-avatar size="180" color="grey lighten-4">
                       <img :src="require('./assets/cphoto.jpg')">
        						</v-avatar>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline">Carlo Tijmons</div>
                    </v-card-title>
                    <v-card-text>
                        Verhaal
                    </v-card-text>
                    <v-card-text>
                      <p>Inmiddels ben ik 3e jaars student op de Hogeschool Rotterdam. Tijdens mijn studie heb ik aan meerdere groepsprojecten gewerkt waar hardware en software gebruikt werd om diverse problemen op te kunnen lossen. Ieder project werd iteratief uitgewerkt om in een korte tijd veel verbetering te realiseren in het ontwikkel process.</p>
                    </v-card-text>
                  </v-card>

                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
      <v-layout column wrap class="my-5" align-center>
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
            <h2 class="headline">Team Foto</h2>
          </div>
        </v-flex>
        <v-flex xs12 sm4 class="my-3">
          <v-card class="elevation-0 transparent">
            <v-card-text class="text-xs-center">
              <v-card color="grey lighten-4">
                <img height=400 width=400 :src="require('./assets/teamfoto.jpeg')">
              </v-card>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </section>

     <!--  <section>
        <v-layout column wrap class="my-5" align-center>
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline">Deliverables</h2>
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">people</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Customer Journeys</div>
                    </v-card-title>
                    <v-card-text>
                      <a download href="/assets/deliverables/customer_journey_gewenste_situatie.pdf">Gewenste situatie</a><br>
                      <a download href="/assets/deliverables/customer_journey_huidige_situatie.pdf">Huidige situatie</a>
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">satellite</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Concept</div>
                    </v-card-title>
                    <v-card-text>
                      <a download href="/assets/deliverables/eindpresentatie.jpg">Eindpresentatie</a><br>
                      <a download href="/assets/deliverables/zwemwater_app.jpg">Zwemwater applicatie</a><br>
                      <a href="http://dashboard.biertjesman.nl">Dashboard</a>
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">build</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Proces</div>
                    </v-card-title>
                    <v-card-text>
                      <a download href="/assets/deliverables/brainstormen.jpg">Brainstormsessie</a><br>
                      <a download href="/assets/deliverables/PosterConcept.pdf">Concept Poster</a>
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
        <v-parallax :src="require('./assets/sentinel-3.jpg')" height="380">
          <v-layout column align-center justify-center>
            <div class="headline pa-2 grey darken-2 white--text mb-3 text-xs-center">Met behulp van satellietdata</div>
            <em class="grey pa-2 darken-2">Geven wij u preventieve inzichten in de staat van de sloten binnen uw waterschap!</em>
          </v-layout>
        </v-parallax>
      </section> -->

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-5">
            <v-flex xs12 sm4>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout">
                  <div class="headline">Over A20</div>
                </v-card-title>
                <v-card-text>
                  Wij van A20 houden van de A20, omdat je daar 130 km/u mag rijden.
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title>
                  <h2 class="headline">Contact</h2>
                  <div class="subheading">Geïnteresseerd, of heb je een vraag?</div>
                </v-card-title>
                <v-list class="transparent">
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="green--text text--lighten-1">phone</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>010-7944000</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="green--text text--lighten-1">place</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>Wijnhaven 99, Rotterdam</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                  <v-list-tile>
                    <v-list-tile-action>
                      <v-icon class="green--text text--lighten-1">email</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                      <v-list-tile-title>contact@a20.com</v-list-tile-title>
                    </v-list-tile-content>
                  </v-list-tile>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>

      <v-footer class="green darken-2">
        <v-layout row wrap align-center>
          <v-flex xs12>
            <div class="white--text ml-3">
              Made with
              <v-icon class="red--text">favorite</v-icon>by A20
            </div>
          </v-flex>
        </v-layout>
      </v-footer>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "Obserbird"
    }
  }
};
</script>
