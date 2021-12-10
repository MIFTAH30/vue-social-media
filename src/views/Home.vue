<template>
    <div class="home">
        <v-container fluid class="mt-4">
            <v-row>
                <v-col cols="12" sm="4">
                    <v-card color="#23262D" elevation="5">
                        <v-row>
                            <v-col cols="12" sm="6">
                                <v-list-item three-line>
                                    <v-list-item-content>
                                        <div>
                                            <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">
                                                FAMILY
                                            </v-list-item-subtitle>
                                            <v-icon color="grey" x-large>fa fa-users</v-icon>
                                        </div>
                                    </v-list-item-content>
                                </v-list-item>
                            </v-col>
                            <v-col cols="12" sm="6">
                                <v-list-item three-line>
                                    <v-list-item-content class="text-right">
                                        <div>
                                            <v-list-item-subtitle class="subtitle-1 mb-14 grey--text">742,824</v-list-item-subtitle>
                                            <v-list-item-subtitle class="grrey--text" style="font=size: 11px">CHANGE TO</v-list-item-subtitle>
                                            <v-list-item-subtitle class="grrey--text mb-5" style="font=size: 11px">PREVIOS MONTH</v-list-item-subtitle>
                                            <v-icon color="green" class="mt-2 mr-2">fa fa-sort-up</v-icon>
                                            <span class="green--text">+20,597</span>
                                            <span class="green--text">(2.16%)</span>
                                        </div>
                                    </v-list-item-content>
                                </v-list-item>
                            </v-col>
                        </v-row>
                    </v-card>
                </v-col>
                <v-col cols="12" sm="3"></v-col>
                <v-col cols="12" sm="3"></v-col>
                <v-col cols="12" sm="3"></v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>

  export default {
    name: 'Home',

    data() {
        return {
            desserts: [
                {
                    glutenfree: false,
                    name    : 'Jeremi',
                    email   : 'Jeremi@gmail.com',
                    contact : '088844465142',
                    status  : 'Open'
                },
                {
                    glutenfree: false,
                    name    : 'Alex',
                    email   : 'Alex@gmail.com',
                    contact : '088844465142',
                    status  : 'Close'
                },
                {
                    glutenfree: false,
                    name    : 'Jhon Doe',
                    email   : 'jhon.doe@gmail.com',
                    contact : '088833365142',
                    status  : 'Open'
                },
            ],
            headers: [
                { text : '', value : 'glutenfree' },
                {
                    text    : 'Name',
                    align   : 'start',
                    sortable: false,
                    value   : 'name',
                },
                { text : 'Email', value : 'email' },
                { text : 'Contact', value : 'contact' },
                { text : 'Status', value : 'status', sortable: false },
                { text : 'Actions', value : 'actions', sortable: false },
            ],
            files: [
                {
                    avatar: '',
                    action: 'Open',
                    headline: 'Birthday gift',
                    subtitle: 'Have any ideas about what we shoukd get Heidi for her birthday?',
                    title: '<strong>Trevor Hansen</strong>'
                }
            ]
        }
    }
  }
</script>

<style scoped>
    .datatab {
        background: #23262D !important;
    }
</style>