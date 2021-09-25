<template>
    <div>
        <h1>Ongoing Tickets</h1>
        <p style="color:tomato">[filter panel]</p>
        <ul>
            ID | Description | Urgent
            <li v-for="ticket of tickets" :key="ticket.id">
                {{ticket.tracking_id}}
            </li>
        </ul>
                <Timeline :begin=ticket.timestamp.begin
                            :PR_issue=ticket.timestamp.PR_issue
                            :PR_approve=ticket.timestamp.PR_approve
                            :PO_issue=ticket.timestamp.PO_issue
                />
                <!-- TODO: wrap timeline in scrollable table with pagination -->
    </div>
</template>

<script>
import axios from 'axios';
import Timeline from '../components/Timeline.vue';

export default {
    name: "Ongoing",
    data() {
        return {
            tickets: []
        }
    },
    components: {
        Timeline
    },
    async created() {
        const {data} = await axios.get("http://localhost:3000/tickets");
        this.tickets = data;
    }
}
</script>

<style lang="scss" scoped>

</style>