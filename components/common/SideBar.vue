<template>
<v-card height="100%">
    <v-icon size="200">
        mdi-account
    </v-icon>
    <v-list>
        <v-list-item v-for="item in items" :key='item.title' nuxt :to="item.link" >
            <v-list-item-icon>
                <v-icon>
                    {{item.icon}}
                </v-icon>
            </v-list-item-icon>
            <v-list-item-content>
                <v-list-item-title>
                    {{item.title}}
                </v-list-item-title>
            </v-list-item-content>

        </v-list-item>

    </v-list>
</v-card>
</template>
<script>
export default {
    name: 'SideBar',
    data(){
        return {
            items:[
            {title:'Overview', icon:'mdi-domain', link:'/overview'},
            {title:'Data Analysis', icon:'mdi-image', link:'/analysis'},
            {title:'Sales Forcast', icon: 'mdi-help-box', link:'/forcast'},
            {title:'Profile', icon:'mdi-account', link:'/profile'},
            {title:'Sign Out', icon: 'mdi-logout', link:'/logout'}
        ]
}
    }
}

</script>
<style scoped>
.v-list-item--active{
    border-width: 1px 0px 1px 5px;
    border-style: solid;
    border-color: rgb(0, 153, 255);
    -webkit-text-fill-color: rgb(0, 153, 255);
    
}
</style>