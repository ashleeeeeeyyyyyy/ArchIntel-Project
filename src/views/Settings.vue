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
                  <v-list-item-subtitle>Manage account settings for Walbro</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item><br>

              <v-card class="mx-auto" outlined>
                <v-list-item three-line>
                  <v-list-item-content>
                    <v-list-item-title class="text-h5">General</v-list-item-title>
                    <v-container fluid class="pa-0">
                      <v-row align="center">
                        <v-col cols="12" sm="6">
                          <v-checkbox value>
                            <template v-slot:label>Require Image Caption</template>
                          </v-checkbox>
                          
                          <v-checkbox value>
                            <template v-slot:label>Require Meta Description</template>
                          </v-checkbox>

                          <v-checkbox value>
                            <template v-slot:label>Show Video Text field</template>
                          </v-checkbox>

                          <v-checkbox value>
                            <template v-slot:label>Enable Video Process</template>
                            
                          </v-checkbox>
                        </v-col>
                      </v-row>
                    </v-container>

                    <v-form>
                    <v-container>
                      <v-row>
                        <v-col cols="12" sm="6">
                          <div>Summary Word Count</div><br>
                          <v-text-field
                            label="Minimum"
                            value="10"
                            outlined
                          ></v-text-field>
                          <v-text-field-subtitle></v-text-field-subtitle>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <div>Content Word Count</div><br>
                          <v-text-field
                            label="Minimum"
                            value="10"
                            outlined
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <v-text-field
                            label="Standard"
                            value="80"
                            outlined
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <v-text-field
                            label="Standard"
                            value="80"
                            outlined
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <v-text-field
                            label="Maximum"
                            value="100"
                            outlined
                          ></v-text-field>
                        </v-col>

                        <v-col cols="12" sm="6">
                          <v-text-field
                            label="Maximum"
                            value="100"
                            outlined
                          ></v-text-field>
                        </v-col>

                        <v-card-actions>
                          <v-btn class="ma-2" max-width="500" color="success">Save</v-btn>
                        </v-card-actions>
                      </v-row>
                    </v-container>
                  </v-form>
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
    data: () => ({
    }),
  }
</script>