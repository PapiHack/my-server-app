<template>
    <div class="row">
        <div class="col-xs-12 col-sm-6">
            <ul class="list-group">
                <app-server-item 
                    v-for="server in servers" 
                    :key="server.id" 
                    :server="server"
                    @showDetails="displayDetails">
                    </app-server-item>
            </ul>
        </div>
        <app-server-item-detail :server="server"></app-server-item-detail>
    </div>
</template>

<script>
import ServerItem from './ServerItem'
import ServerItemDetail from './ServerItemDetail'

    export default {
        data(){
            return {
                server: 'none',
                servers: [
                    {id: 1, status: 'Normal'},
                    {id: 2, status: 'Critical'},
                    {id: 3, status: 'Normal'},
                    {id: 4, status: 'Critical'},
                    {id: 5, status: 'Normal'},
                ]
            }
        },
        components: {
            'app-server-item': ServerItem,
            'app-server-item-detail': ServerItemDetail
        },
        methods: {
            displayDetails(id){
                let server = this.servers[id - 1]
                this.server = server
            }
        }
    }
</script>