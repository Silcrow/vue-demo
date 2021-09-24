<template>
    <div id="ShowTicket">
        {{tracking_id}} | {{description}} | {{urgent}}
    </div>
</template>

<script>
    export default {
        name: "ShowTicket",
        props: {
            'tracking_id': String,
            'description': String,
            'urgent': Boolean
        }
    }
</script>

<style lang="scss" scoped>

</style>