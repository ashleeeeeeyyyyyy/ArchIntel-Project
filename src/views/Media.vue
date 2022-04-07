<template>
  <v-app>
    <v-main>
      <v-container fluid="xs-sm-md-lg">
        <v-row>
          <v-col>
            <v-card class="mx-auto">
              <v-list-item three-line>
                <v-list-item-content>
                  <v-list-item-title class="text-h5 mb-1">
                    Walbro - All Media
                  </v-list-item-title>
                  <v-list-item-subtitle>This table shows recently searched articles for Walbro</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>

              <v-card-actions>
                <v-btn class="ma-2" color="primary">
                  Export
                </v-btn>
              </v-card-actions>

              <v-tabs color="blue darken-1">
                <v-tab v-for="link in links" :key="link">
                  {{ link }}
                </v-tab>
              </v-tabs>
            </v-card>
          </v-col>
        </v-row>

        <div>
          <v-data-table
            :headers="headers"
            :items="list"
            class="elevation-1"
          >
          <template #item.edit="{ item }">
            <v-checkbox
              v-model="item.edit"
              color="primary"
            ></v-checkbox>
          </template>

          <template #item.published="{ item }">
            <v-checkbox
              v-model="item.published"
              color="primary"
            ></v-checkbox>
          </template>

          <template #item.title="{ value }">
            <a target="_blank" :href="value">
              {{ value }}
            </a>
        </template>

        <template v-slot:item.action="{ value }">
          <v-btn class="mx-2" fab dark small color="green">
            <v-icon medium>edit_note</v-icon>
          </v-btn>
          
          <v-btn class="mx-2" fab dark small color="blue">
            <v-icon dark>cloud</v-icon>
          </v-btn>
        </template>
        </v-data-table>
      </div>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        links: [
          'ALL (1000)',
          'CUSTOMERS (221)',
          'COMPETITORS(78)',
          'PRODUCTS (171)',
        ],
        list: [
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 2:07PM',
            edit: true,
            published: false,
            category: 'Customers',
            title: 'Review: 2021 Honda Gold DCT a Good Long-Distance Tourer',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 1:43PM',
            edit: true,
            published: false,
            category: 'Customers',
            title: 'Case IH Unveils Tier 5-Compliant Puma Tractors',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 12:51PM',
            edit: true,
            published: false,
            category: 'Customers',
            title: 'Kawasaki to Expand Production Facilty',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 3:33PM',
            edit: true,
            published: false,
            category: 'Customers',
            title: 'Specialty Equipment Marked Association Names Finalist For 2021 SEMA Awards',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 1:03PM',
            edit: true,
            published: false,
            category: 'Customers',
            title: 'Volvo Launches New Electric Heavy-Duty Equipment',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 4:07PM',
            edit: true,
            published: false,
            category: 'Social Media',
            title: 'VIDEO: Kawasaki Confirms Z650 RS, Z900 RS SE for Canada',
          },
          {
            action: '',
            date: "October 12, 2021",
            created: 'October 08, 2021 3:58PM',
            edit: true,
            published: false,
            category: 'Social Media',
            title: 'VIDEO: 2022 Yamaha WR2 Features & Benefits',
          },
          {
            action: '',
            date: "October 08, 2021",
            created: 'October 08, 2021 3:07PM',
            edit: true,
            published: true,
            category: 'Competitors',
            title: 'Bosch, BorgWarner Support Congress Dritev',
          },
          {
            action: '',
            date: "October 08, 2021",
            created: 'October 08, 2021 2:55PM',
            edit: true,
            published: true,
            category: 'Competitors',
            title: 'CFO Bob Hickson Departs Oregon Tool',
          },
          {
            action: '',
            date: "October 08, 2021",
            created: 'October 08, 2021 3:12PM',
            edit: false,
            published: false,
            category: 'Customers',
            title: 'Deesiide Gold Club bolsters fleet',
          },
        ],
        headers: [
          {
            text: 'Action',
            align: 'start',
            sortable: false,
            value: 'action',
          },
          { text: 'Media Date', value:'date', },
          { text: 'Created Date & Time', value: 'created' },
          { text: 'For Editing', value: 'edit' },
          { text: 'Published', value: 'published' },
          { text: 'Category', value: 'category' },
          { text: 'Title', value: 'title' },
        ],
      }
    },
  }
</script>