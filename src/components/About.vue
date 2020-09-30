<template>
    <v-container class="mt-15" id="about">
        <div class="text-center">
            <h2 class="ma-10" id="heading">About Us</h2>
        </div>
        <v-layout row wrap>
            <v-flex xs12 sm12 md4 lg4 v-for="feature in features" :key="feature.title">
                <v-card class="pa-6" elevation="0">
                    <v-responsive>
                        <v-img :src="feature.images" width="110" class="images"></v-img>
                    </v-responsive>
                    <v-card-text>
                        <div class="subheading text-center"><h2>{{ feature.title }}</h2></div>
                        <div class="mt-4">{{ feature.description }}</div>
                    </v-card-text>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
export default {
    name: 'About',
    data() {
        return {
            features: [
                {
                    images: '/images/Waiting.png', title: 'Over 20 Years of Experience', description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. At eaque sequi odit alias sed? Provident ducimus suscipit enim, recusandae eum assumenda quod a ipsa numquam, aliquid iste excepturi quam in?'
                },
                {
                    images: '/images/Term of Use.png', title: 'Quality Garment Products', description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. At eaque sequi odit alias sed? Provident ducimus suscipit enim, recusandae eum assumenda quod a ipsa numquam, aliquid iste excepturi quam in?'
                },
                {
                    images: '/images/Reviews.png', title: 'Another Title', description: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. At eaque sequi odit alias sed? Provident ducimus suscipit enim, recusandae eum assumenda quod a ipsa numquam, aliquid iste excepturi quam in?'
                }
            ]
        }
    }
}
</script>

<style scoped>
.images{
    margin: auto;
}
#heading{
    display: inline-block;
    border-bottom: 2px solid lightseagreen;
}
</style>