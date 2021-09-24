<template>
    <div class="Timeline">
        <v-timeline dense>
            <v-timeline-item small color="green">{{begin}} Begin </v-timeline-item>
            <p style="color:tomato">[time elapse]</p>
            <v-timeline-item small color="green">{{PR_issue}} PR Issue </v-timeline-item>
            <p style="color:tomato">[total time used]</p>
            <v-timeline-item small color="green">{{PR_approve}} PR Approve </v-timeline-item>
            <p style="color:tomato">[total time used]</p>
            <v-timeline-item small color="green">{{PO_issue}} PO Issue </v-timeline-item>
            <p style="color:tomato">[total time used]</p>
        </v-timeline>
    </div>
</template>

<script>
    export default {
        name: "Timeline",
        props: {
            'begin': String,
            'PR_issue': String,
            'PR_approve': String,
            'PO_issue': String,
        }    
    }
</script>

<style lang="scss" scoped>

</style>