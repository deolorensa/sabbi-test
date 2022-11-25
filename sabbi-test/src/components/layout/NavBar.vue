<template>
    <v-container>
        <v-toolbar
        color="rgb(0, 115, 250)">
        <svg xmlns="http://www.w3.org/2000/svg" color="#ffff" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4.8 2.3A.3.3 0 1 0 5 2H4a2 2 0 0 0-2 2v5a6 6 0 0 0 6 6v0a6 6 0 0 0 6-6V4a2 2 0 0 0-2-2h-1a.2.2 0 1 0 .3.3"></path><path d="M8 15v1a6 6 0 0 0 6 6v0a6 6 0 0 0 6-6v-4"></path><circle cx="20" cy="10" r="2"></circle></svg>
            <v-toolbar-title class="text-title">
                Technical Test
            </v-toolbar-title>
            
            <v-toolbar-items class="white">
                
                <v-btn text>
                    <a href="#post" class="white">Post Content</a>
                    
                </v-btn>
                <v-btn text>
                    User
                </v-btn>
                
            </v-toolbar-items>
            
            
        </v-toolbar>
    </v-container>
</template>

<script>
export default {

}
</script>

<style scoped>
.text-title{
    color: rgb(250 250 249);
    font-weight: 600;
}
a{
    text-decoration: none;
}
</style>