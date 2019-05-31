<template>
    <div class="row">
        <div class="col-xs-12 col-sm-6">
            <ul class="list-group">
                <app-server-item v-for="server in 5" :key="server" :index="server"></app-server-item>
            </ul>
        </div>
        <app-server-item-detail></app-server-item-detail>
    </div>
</template>

<script>
import ServerItem from './ServerItem'
import ServerItemDetail from './ServerItemDetail'

    export default {
        components: {
            'app-server-item': ServerItem,
            'app-server-item-detail': ServerItemDetail
        }
    }
</script>