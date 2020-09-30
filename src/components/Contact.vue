<template>
    <v-container class="mt-15" id="contact">
        <div class="text-center">
            <h2 class="ma-10" id="heading">Contact Us</h2>
        </div>
        <v-card class="pa-6 text-center" elevation="0" id="form-card">
            <v-card-text>
                <v-form>
                    <v-text-field v-model="name" label="Name" solo></v-text-field>
                    <v-text-field v-model="email" label="Email" solo></v-text-field>
                    <v-textarea v-model="message" label="Message" solo></v-textarea>
                    <v-btn class="primary">Send Message</v-btn>
                </v-form>
            </v-card-text>
        </v-card>
    </v-container>
</template>

<script>
export default {
    name: 'Contact',
    data() {
        return{
            name: '',
            email: '',
            message: ''
        }
    }
}
</script>

<style scoped>
#heading{
    display: inline-block;
    border-bottom: 2px solid lightseagreen;
}
#form-card{
    width: 90%;
}
</style>