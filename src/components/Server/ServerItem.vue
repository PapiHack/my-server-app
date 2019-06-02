<template>
    <li class="list-group-item">Server #{{ server.id }} - Status : {{ server.status }}
        &nbsp;&nbsp;&nbsp;<button class="btn btn-info" @click="$emit('showDetails', server.id)">Details</button>
    </li>
</template>

<script>

    export default {
        props: ['server']
    }
</script>