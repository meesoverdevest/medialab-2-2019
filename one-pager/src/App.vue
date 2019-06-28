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
              href="https://a20.biertjesman.nl/"
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
                      <v-icon x-large class="green--text text--lighten-1">streetview</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Beeld en Contact Voor Hulpdiensten</div>
                    </v-card-title>
                    <v-card-text>
                      Met behulp van de Obserbird is het mogelijk voor de hupldiensten om in real-time informatie deelen met andere eenheden in het veld. De Obserbird maakt het mogelijk voor de hulpdiensten in de meldkamer om mee te kijken met de eenheden in het veld. Ook kan er communicatie plaats vinden tussen de Meldkamer en eenheden in het veld. Hiermee willen wij ervoor zorgen om de coördinatie tussen eenheden te stimuliseren zodat er sneller, juist en accuraat gehandeld kan worden.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">view_comfy</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Een Overzicht Voor De Meldkamer</div>
                    </v-card-title>
                    <v-card-text>
                      Het Obserbird systeem maakt het mogelijk voor de meldkamer om mee te kijken met de veld eenheden die gebruik maken van het product. De eenheden in het veld kunnen naar de Medlkamer singaleren als ze een assistentie vereisen. Hierdoor kan de meldkamer meteen schakelen naar het beeld van de desbetreffende hulpdienst. 
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-0 transparent">
                    <v-card-text class="text-xs-center">
                      <v-icon x-large class="green--text text--lighten-1">commute</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Ingrijpen voor het mis gaat</div>
                    </v-card-title>
                    <v-card-text>
                      Voordat situaties escaleren kunnen de hulpdiensten al inschakelt worden. Als het blijkt dat de desbetreffende hulpdienst versterking nodig heeft van andere colega's dan kan de meldkamer de dichtstbijzijnde eenheden aansturen.
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

    <section>
      <v-layout column wrap class="my-5" align-center>
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
              <h2 class="headline">Bewijzen en Deliverables</h2>
            </div>
          </v-flex>


          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>

                <v-flex xs12 md6>
                  <v-card-text primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Presentaties</div>
                  </v-card-text>
                  <v-card-text>
                    <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/presentation/d/1XZE1PhEHmJ-rtWfxk3zGrPAYWSMApvC_Ufu5pQhISJ8/edit?usp=sharing"
                      target="_blank"
                    >
                      Tussen Presentatie
                    </v-btn>
                    <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/presentation/d/1Jou5yeyIv64Q4XflLTkRy7llFYMGvphPcqI8MGVZ7Rc/edit?usp=sharing"
                      target="_blank"
                    >
                      Eind Presentatie
                    </v-btn>
                  </v-card-text>
                </v-flex>

                <v-flex xs12 md6>
                  <v-card-text primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Individueel development-ontwikkeldocument</div>
                  </v-card-text>
                  <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/presentation/d/1XZE1PhEHmJ-rtWfxk3zGrPAYWSMApvC_Ufu5pQhISJ8/edit?usp=sharing"
                      target="_blank"
                    >
                      Mees
                    </v-btn>
                    <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/presentation/d/1XZE1PhEHmJ-rtWfxk3zGrPAYWSMApvC_Ufu5pQhISJ8/edit?usp=sharing"
                      target="_blank"
                    >
                      Carlo
                    </v-btn>
                  <!-- <v-card-text>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent pulvinar nisl quis ipsum bibendum, vitae molestie libero maximus. Mauris congue tellus a nisl pharetra vulputate. Suspendisse feugiat elit eget efficitur tincidunt. Mauris congue, nibh et condimentum facilisis, purus ante fringilla ipsum, a malesuada eros sapien in ipsum. Nam elementum sodales magna sed maximus. Curabitur commodo condimentum diam, sed condimentum leo interdum et. Morbi scelerisque diam maximus, hendrerit libero eu, tincidunt justo. Maecenas blandit lorem non libero varius, eu ullamcorper dui viverra. Donec in diam vitae mauris volutpat pharetra eu et velit. Morbi ultrices sapien ut metus volutpat, ac hendrerit turpis sollicitudin. Ut in magna sed mauris gravida porttitor.</p>
                  </v-card-text> -->
                </v-flex>

                <v-flex xs12 md6>
                  <v-card-text primary-title class="layout justify-center">
                    <div class="headline text-xs-center">Prototypes</div>
                  </v-card-text>
                  <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/document/d/1Dw3DYW0Gf0fcrLYL_faSzgIRvwZ1UMF4XlLa2Rjns2A/edit?usp=sharing"
                      target="_blank"
                  >
                  Opzet Concept en Expert Interview
                </v-btn>
                  <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://drive.google.com/drive/folders/1gaL4HRJwfyrQ7PA2NCeY5YbMBl_FLy0D?usp=sharing"
                      target="_blank"
                  >
                  Wireframes
                </v-btn>
                <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://drive.google.com/file/d/1gcB0YF4G_Ydxt9Q1A0aShmU0NBtkBkvq/view?usp=sharing"
                      target="_blank"
                  >
                  Action Cam VLC Stream demonstratie video 
                </v-btn>
                <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://docs.google.com/document/d/1PIJCGE70KY3oX5JJ1SNo4bGf_M_9HFoyRbDf8lWIZWE/edit?usp=sharing"
                      target="_blank"
                  >
                  StoryBoard
                </v-btn>
                <v-btn 
                      class="green lighten-1 mt-5 layout justify center"
                      dark
                      large
                      href="https://obserbird.biertjesman.nl/"
                      target="_blank"
                  >
                  Obserbird Dashboard
                </v-btn>
                  <v-card-text>
                    
                  </v-card-text>
                </v-flex>

                <v-flex xs12 md6>
                  <v-card-text primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Github</div>
                  </v-card-text>
                  <v-card-text class="layout justify-center">
                    <a href="https://github.com/meesoverdevest/medialab-2-2019" target="_blank"><img width=200 height=200 :src="require('./assets/github.png')"></a>
                  </v-card-text>
                  <v-card-text primary-title class="layout justify-center">
                      <i>Klik op de photo hierboven om naar onze <br> Github repositorie verwezen te worden</i>
                  </v-card-text>
                </v-flex>


              </v-layout>
            </v-container>
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
