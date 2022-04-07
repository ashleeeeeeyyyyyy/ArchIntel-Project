<template>
  <v-app>
    <v-main class="grey lighten-3">
      <v-container fluid="xs-sm-md-lg">
        <v-row>
          <v-col cols="12" sm="6">
            <v-sheet min-height="80vh" rounded="xs-sm-md-lg">
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title class="text-h5">Welcome to Walbro Writer Dashboard</v-list-item-title>
                  <v-list-item-subtitle>Data as of Oct 9, 2021 10:00 PM</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-card-actions>
                <v-btn class="ma-2" color="success">
                  Create Article
                </v-btn>
              </v-card-actions>
              
              <v-tabs color="blue darken-1">
                <v-tab v-for="link in links" :key="link">
                  {{ link }}
                </v-tab>
              </v-tabs>

              <div class="primary darken-1 text-center">
                <span class="center white--text font-weight-bold">Customers</span><br>
              </div>
              
              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-container fluid class="pa-0">
                      <v-row align="center">
                        <v-col cols="12" sm="6">
                          <div class>
                            <div class>
                              <v-btn class="mx-2" fab dark small color="green">
                                <v-icon dark>
                                  edit
                                </v-icon>
                              </v-btn>
                            </div><br>
                            
                            <div class>
                              <v-btn class="mx-2" fab dark small color="blue">
                                <v-icon dark>
                                  mdi-account-plus
                                </v-icon>
                              </v-btn>
                            </div><br>

                            <div class>
                              <v-btn class="mx-2" fab dark small color="red">
                                <v-icon dark>
                                  mdi-delete
                                </v-icon>
                              </v-btn>
                            </div>
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-list-item-content>
                </v-list-item>
              </v-card>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-container fluid class="pa-0">
                      <v-row align="center">
                        <v-col cols="12" sm="6">
                          <div class>
                            <div class>
                              <v-btn class="mx-2" fab dark small color="green">
                                <v-icon dark>
                                  edit
                                </v-icon>
                              </v-btn>
                            </div><br>
                            
                            <div class>
                              <v-btn class="mx-2" fab dark small color="blue">
                                <v-icon dark>
                                  mdi-account-plus
                                </v-icon>
                              </v-btn>
                            </div><br>

                            <div class>
                              <v-btn class="mx-2" fab dark small color="red">
                                <v-icon dark>
                                  mdi-delete
                                </v-icon>
                              </v-btn>
                            </div>
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-list-item-content>
                </v-list-item>
              </v-card>

              <div class="primary darken-1 text-center">
                <span class="center white--text font-weight-bold">Competitors</span><br>
              </div>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-subtitle class="text-center">-No Article Available-</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-card>

              <div class="primary darken-1 text-center">
                <span class="center white--text font-weight-bold">Products</span><br>
              </div>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-container fluid class="pa-0">
                      <v-row align="center">
                        <v-col cols="12" sm="6">
                          <div class>
                            <div class>
                              <v-btn class="mx-2" fab dark small color="green">
                                <v-icon dark>
                                  edit
                                </v-icon>
                              </v-btn>
                            </div><br>
                            
                            <div class>
                              <v-btn class="mx-2" fab dark small color="blue">
                                <v-icon dark>
                                  mdi-account-plus
                                </v-icon>
                              </v-btn>
                            </div><br>

                            <div class>
                              <v-btn class="mx-2" fab dark small color="red">
                                <v-icon dark>
                                  mdi-delete
                                </v-icon>
                              </v-btn>
                            </div>
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-list-item-content>
                </v-list-item>
              </v-card>
            </v-sheet>
          </v-col>
          
          <v-col cols="12" sm="6">
            <v-simple-table>
              <template>
                <thead>
                  <v-list-item three-line>
                    <v-list-item-content>
                      <v-list-item-title class="text-h5 mb-1">Writed Production</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  
                  <tr>
                    <th class="text-left">Name</th>
                    <th class="text-left">Assigned</th>
                    <th class="text-left">Submitted</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="item in production_info" :key="item.name">
                    <td>{{ item.name }}</td>
                    <td>{{ item.prod_assigned }}</td>
                    <td>{{ item.prod_submitted }}</td>
                  </tr>
                </tbody>
              </template>
            </v-simple-table><br>

            <v-sheet rounded="xs-sm-md-lg">
               <v-list-item three-line>
                  <v-list-item-title class="text-h5 mb-1">Article List Preview</v-list-item-title>
              </v-list-item>
              <div class="primary darken-1 text-center">
                <span class="white--text font-weight-bold">Customers</span><br>
              </div>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-subtitle class="text-center">-No Article Available-</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>

                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-subtitle class="text-center">-No Article Available-</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-card>
            </v-sheet>

            <v-sheet rounded="xs-sm-md-lg">
              <div class="primary darken-1 text-center">
                <span class="white--text font-weight-bold">Competitors</span><br>
              </div>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-subtitle class="text-center">-No Article Available-</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-card>
            </v-sheet>

            <v-sheet min-height="20vh" rounded="xs-sm-md-lg">
              <div class="primary darken-1 text-center">
                <span class="white--text font-weight-bold">Products</span><br>
              </div>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-subtitle class="text-center">-No Article Available-</v-list-item-subtitle>
                  </v-list-item-content>
                </v-list-item>
              </v-card>
            </v-sheet>

          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
        overlay: true,
        links: [
          'TODAY (18)',
          'ADVANCE (7)',
          'LAST 7 DAYS (46)',
          'SENT BACK (4)',
        ],
        production_info: [
          {
            name: 'Writer User 1',
            prod_assigned: 7,
            prod_submitted: 7,
          },
          {
            name: 'Writer User 2',
            prod_assigned: 3,
            prod_submitted: 2,
          },
        ],
      }
    },
  }
</script>