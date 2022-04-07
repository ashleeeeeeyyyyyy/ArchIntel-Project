<template>
  <nav>
      <v-app-bar color="teal darken-4" dark app>
          <v-app-bar-nav-icon @click="drawer = !drawer">

          </v-app-bar-nav-icon>
          
          <v-responsive max-width="1000">
          <v-text-field
            label="Search"
            prepend-inner-icon="mdi-magnify"
            dense
            flat
            hide-details
            solo-inverted
          ></v-text-field>
          </v-responsive>
          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-monitor-dashboard</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon>mdi-bell</v-icon>
          </v-btn>
            
          <v-btn icon>
            <v-icon>settings</v-icon>
          </v-btn>

          <v-btn icon>
            <v-icon right>mdi-clock-outline</v-icon>
          </v-btn>
      </v-app-bar>

      <v-navigation-drawer v-model="drawer" dark app class="teal darken-4">
          <v-list>
            <v-list-item link>
                <v-list-item-content>
                <v-list-item-title class="text-h6">Writer Chassis</v-list-item-title>
            </v-list-item-content></v-list-item>
            </v-list>
            <v-divider></v-divider>

            <v-list>
                <v-list-item link>
                <v-list-item-content>
                    <v-list-item-title class="pt-3">Ashley Pua Phee</v-list-item-title>
                    <v-list-item-subtitle>Writer</v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-action>
                    <v-icon>mdi-menu-down</v-icon>
                </v-list-item-action>
                </v-list-item>
            </v-list>
            <v-divider></v-divider>

            <v-list flat>
                <v-list-item v-for="link in links" :key="link.text" router :to="link.route" active-class="border">
                    <v-list-item-action>
                        <v-icon>{{link.icon}}</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                        <v-list-item-title>{{link.text}}</v-list-item-title>
                    </v-list-item-content>
                </v-list-item>
            </v-list>

          <v-footer bottom fixed dark padless>
            <v-card class="flex teal darken-2" flat tile>
                <v-card-text class="white--text pt-3">
                    <strong><u>Salesforce Home</u></strong><br>
                    <strong>v.4.4.0 | © 2021 Archintel Corp.</strong>
                </v-card-text>
            </v-card>
          </v-footer>
      </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
    data: () => ({
        drawer: true,
        links: [
            { icon: 'dashboard', text:'Dashboard', route:'/' },
            { icon: 'on_device_training', text:'All Media', route:'/media' },
            { icon: 'settings', text:'Account Settings', route:'/settings' },
        ]
    })
}
</script>

<style>

</style>