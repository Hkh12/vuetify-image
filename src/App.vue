<template>
    <v-app>
        <v-toolbar app color="primary" dark>
            <v-toolbar-title>VImage Component Test</v-toolbar-title>
        </v-toolbar>
        <v-content>
            <v-container class="pt-3">
                <v-flex xs12 md8>                  
                    <h1 class="display-1 mb-3 mt-1">A regular image</h1>
                    <v-image :src='url' />
                    <div class="headline my-3">With an error</div>
                    <v-image :src="url + 'x'"></v-image>
                    <h1 class="display-1 mb-3 mt-1">Custom aspect ratio (X:Y)</h1>
                    Aspect ratios are used for indicators, not image itself.
                    <br>
                    This one has a custom ratio (8:3):
                    <v-image :src="url + 'x'" aspect-ratio='8:3'></v-image>
                </v-flex>
            </v-container>
        </v-content>              
    </v-app>
</template>

<script>
export default {
    name: 'app',
    computed: {
        url(){
            return 'https://pre00.deviantart.net/dc34/th/pre/f/2015/030/6/f/_minflat__dark_material_design_wallpaper__4k__by_dakoder-d8fjqzu.jpg'
        }
    }
}
</script>

<style>
#app{
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
</style>
