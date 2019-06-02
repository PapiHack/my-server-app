<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="server == 'none'">Server Details are currently not updated</p>
        <p v-else>Server n°{{ server.id }} - Status : <b>{{ server.status }}</b>
            <br><button class="btn btn-success" @click="changeStatus">Change status</button> 
        </p>
    </div>
</template>

<script>
    export default {
        props: ['server'],
        methods: {
            changeStatus(){
                this.server.status  = this.server.status == 'Normal' ? 'Critical' : 'Normal'
            }
        }
    }
</script>