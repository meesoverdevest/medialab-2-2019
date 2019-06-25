<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawerRight"
      fixed
      right
      clipped
      app
    >
      <v-list dense>
        <v-list-tile @click.stop="right = !right">
          <v-list-tile-action>
            <v-icon>exit_to_app</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Open Temporary Drawer</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar
      color="blue-grey"
      dark
      fixed
      app
      clipped-right
    >
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Obserbird</v-toolbar-title>
      <v-icon small>verified_user</v-icon>
      <v-spacer></v-spacer>
      <v-toolbar-side-icon @click.stop="drawerRight = !drawerRight"></v-toolbar-side-icon>
    </v-toolbar>
    <v-navigation-drawer
      v-model="drawer"
      fixed
      app
    >
      <v-list dense>
        <v-list-tile @click.stop="left = !left">
          <v-list-tile-action>
            <v-icon>exit_to_app</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Open Temporary Drawer</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-navigation-drawer
      v-model="left"
      temporary
      fixed
    >
      <v-icon large>verified_user</v-icon>
    </v-navigation-drawer>
    <v-content>
      <v-container grid-list-md text-xs-center>
        <v-layout row wrap>
          <v-flex v-for="i in 9" :key="`4${i}`" xs4>
            <v-card>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/desert.jpg"
                aspect-ratio="2.75"
              ></v-img>
              

              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">Agent: {{ i }}</h3>
                </div>
              </v-card-title>

              <v-card-actions>
                <v-icon>arrow_left</v-icon>
                <v-icon>arrow_right</v-icon>
                <v-icon>mic_off</v-icon>
                <v-icon>mic</v-icon>
                <v-btn flat color="orange" @click="dialog = true">Open</v-btn>
              </v-card-actions>
            </v-card>
          </v-flex>
          <v-flex md6>
            <v-dialog
              v-model="dialog"
              width="750"
              height="550"
            >
              <v-card>
                <pano title="The Title" width="720" height="480" bundle="assets/imgbox/" format="jpg"></pano>

                <v-card-actions>
                  <h3 class="headline mb-0">Agent: {{ i }}</h3>
                  <v-spacer></v-spacer>
                  <v-icon>arrow_left</v-icon>
                  <v-icon>arrow_right</v-icon>
                  <v-icon>mic_off</v-icon>
                  <v-icon>mic</v-icon>
                  <v-spacer></v-spacer>
                  <v-btn
                    color="primary"
                    flat
                    @click="dialog = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
          </v-flex>
        </v-layout>
      </v-container>
      <!-- <v-container fluid fill-height>
        <v-layout justify-center align-center>
          <v-flex shrink>
            <v-tooltip right>
              <template v-slot:activator="{ on }">
                <v-btn :href="source" icon large target="_blank" v-on="on">
                  <v-icon large>code</v-icon>
                </v-btn>
              </template>
              <span>Source</span>
            </v-tooltip>
            <v-tooltip right>
              <template v-slot:activator="{ on }">
                <v-btn icon large href="https://codepen.io/johnjleider/pen/KQrPKJ" target="_blank" v-on="on">
                  <v-icon large>mdi-codepen</v-icon>
                </v-btn>
              </template>
              <span>Codepen</span>
            </v-tooltip>
          </v-flex>
        </v-layout>
      </v-container> -->
    </v-content>
    <v-navigation-drawer
      v-model="right"
      right
      temporary
      fixed
    >
      <v-icon large>verified_user</v-icon>
    </v-navigation-drawer>
    <v-footer color="blue-grey" class="white--text" app>
      <span>A20</span>
      <v-spacer></v-spacer>
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>
  import Pano from 'vue-pano';

  export default {
    name: 'App',
    components: { Pano },
    data: () => ({
      drawer: false,
      drawerRight: false,
      right: false,
      left: false,
      source: "https://github.com/meesoverdevest/medialab-2-2019",
      dialog: false
    })
  }
</script>