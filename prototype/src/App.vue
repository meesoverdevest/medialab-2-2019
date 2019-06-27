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
          <v-flex v-for="agent in agents" :key="agent.id" xs4>
            <v-card :color="agent.has_emergency ? 'red' : null">
              <v-img
                :src="agent.avatar"
                aspect-ratio="2"
              ></v-img>
              

              <v-card-title primary-title>
                <div>
                  <h3 class="headline mb-0">Agent: {{ agent.name }}</h3>
                </div>
              </v-card-title>

              <v-card-actions>
                <v-btn color="orange" @click="openDialog(agent)">Open</v-btn>
                <v-icon>arrow_left</v-icon>
                <v-icon>arrow_right</v-icon>
                <v-icon @click="toggle_mic(agent)" v-if="!agent.mic_on">mic_off</v-icon>
                <v-icon @click="toggle_mic(agent)" v-else>mic_on</v-icon>
              </v-card-actions>
            </v-card>
          </v-flex>
          <v-flex md6>
            <v-dialog 
              v-if="dialogAgent !== null"
              v-model="dialog"
              width="720"
            >
              <v-tabs
                color="orange"
                dark
                slider-color="yellow"
              >
                <v-tab
                  key="panorama"
                  ripple
                >
                  Video
                </v-tab>
                <v-tab
                  key="location"
                  ripple
                >
                  Locatie
                </v-tab>
                <v-tab-item
                  key="panorama"
                >
                  <pano :title="`Agent ${dialogAgent.name} in ${dialogAgent.city}, ${dialogAgent.street}`" width="720" height="480" :bundle="`assets/${dialogAgent.id}/`" format="jpg"></pano> 
                </v-tab-item>
                <v-tab-item
                  key="location"
                >
                  <v-card flat>
                    <v-card-text>Locatie: {{ dialogAgent.city }}, {{ dialogAgent.street }}</v-card-text>
                  </v-card>
                </v-tab-item>
              </v-tabs>
              <v-btn color="orange lighten-1" @click="closeDialog">Close {{ dialogAgent.name }}</v-btn>
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
  import faker from 'faker';
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
      dialog: false,
      agents: [],
      dialogAgent: null
    }),
    mounted() {
      this.createAgents();

      let self = this;
      setTimeout(function(){ self.setEmergency() }, 10000);
    },
    methods: {
      openDialog(agent) {
        this.dialogAgent = agent;
        this.dialog = true;
      },
      closeDialog() {
        this.dialogAgent = null;
        this.dialog = false;
      },
      setEmergency() {
        this.agents.find(a => a.id === 4).has_emergency = true;
      },
      createAgents() {
        for (var i = 0; i < 6; i++) {
          this.agents.push({
            id: i+1,
            name: faker.name.findName(),
            city: faker.address.city(),
            street: faker.address.streetName(),
            avatar: faker.image.avatar(300,140,"people"),
            mic_on: false,
            has_emergency: false
          });
        }
      },
      toggle_mic(agent) {
        this.agents.find(a => a.id === agent.id).mic_on = agent.mic_on === false ? true : false;
      }
    }
  }
</script>