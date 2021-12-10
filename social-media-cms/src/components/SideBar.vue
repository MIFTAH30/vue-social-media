<template>
    <nav>
        <v-app-bar color="#23262D" dark app class="line" height="70px">
            <v-chip class="ma-2" color="grey darken-1" pill>
                DASHBOARD
                <v-icon right small color="cyan">
                    fas fa-chevron-circle-down
                </v-icon>
            </v-chip>
            <v-chip class="ma-2" color="grey darken-1" pill>
                REPORTS
                <v-icon right small color="cyan">
                    fas fa-chevron-circle-down
                </v-icon>
            </v-chip>
            <v-chip class="ma-2" color="grey darken-1" pill>
                ORDERS
                <v-icon right small color="cyan">
                    fas fa-chevron-circle-down
                </v-icon>
            </v-chip>
            <v-spacer></v-spacer>
            <v-text-field filled dense rounded label="Search" prepend-inner-icon="fas fa-search" class="mt-7 mr-2" sm="1"></v-text-field>
            <v-btn fab color="cyan" elevation="0" class="mr-2">
                <v-icon color="white">fas fa-user-check</v-icon>
            </v-btn>
            <v-btn fab color="orange" elevation="0">
                <v-icon color="white">fas fa-bars</v-icon>
            </v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" dark app mini-variant mini-variant-width="125" color="#23262D">
            <v-list>
                <v-list-item-group color="cyan">
                    <v-list-item class="mb-4">
                        <v-list-item-content align="center">
                            <v-icon align="center" x-large>fa fa-tv</v-icon>
                        </v-list-item-content>
                    </v-list-item>
                </v-list-item-group>
                <v-list-item-group color="cyan" v-model="selectedItem">
                    <v-list-item class="mb-4" v-for="(item, i) in items" :key="i">
                        <v-list-item-content align="center">
                            <v-icon v-text="item.icon" align="center"></v-icon>
                            <v-list-item-subtitle v-text="item.text" align="center" class="caption"></v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
    // data() {
    //     return {
    //         api: '',
    //         items: []
    //     },
    // },
    data: () => ({
        drawer: null,
        seletedItem: 0,
        items: [
            {text: 'DASHBOARD', icon: 'fas fa-tachometer-alt'},
            {text: 'REPORTS', icon: 'fas fa-file-alt'},
            {text: 'STOCK AGEING', icon: 'fas fa-chart-line'},
            {text: 'DEVICE SALES', icon: 'fas fa-tablet'},
            {text: 'USER REPORT', icon: 'fas fa-user-tag'},
            {text: 'SETTINGS', icon: 'fas fa-cogs'},
        ]
    })
}
</script>