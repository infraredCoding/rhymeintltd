<template>
    <div>
        <v-app-bar
        app
        color="light"
        light mobile-breakpoint=700
        >
        <div class="d-flex align-center ml-10">
            <v-img
            alt="Vuetify Logo"
            class="shrink mr-2"
            contain
            src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
            transition="scale-transition"
            width="40"
            />

            <v-appbar-title>
            Rhyme Int Ltd.
            </v-appbar-title>
        </div>

        <v-spacer></v-spacer>
        <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
        <div class="hidden-sm-and-down">
            <v-btn href="#about" text>
            <span class="px-4">About</span>
            </v-btn>
            <v-btn href="#contact" text>
            <span class="px-4">Contact</span>
            </v-btn>
        </div>
        </v-app-bar>

        <v-navigation-drawer
            v-model="drawer"
            app
            >
            <v-icon @click="drawer = false" large id="close-nav">mdi-close</v-icon>
            <v-list>
                <v-list-item
                v-for="item in items"
                :key="item.title"
                link
                >

                <v-list-item-content class="text-center my-15">
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </div>    
</template>

<script>
export default {
    name: "Navbar",
    data(){
        return { 
            drawer: false,
            items: [
                {
                    'title': 'Contact'
                },
                {
                    'title': 'About'
                }
            ]
        }
    }
}
</script>

<style scoped>
#close-nav{
    margin-left: 40%;
    margin-top: 20px;
}
</style>