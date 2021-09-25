<template>
    <div>
        <h1>Analysis of Completed Tickets</h1>
        <ul>
            urgent | complete | late
            <li v-for="ticket of tickets" :key="ticket.id">
                {{ticket.urgent}} | {{ticket.complete}} | {{ticket.late}}
            </li>
        </ul>
        <!-- TODO: find its counts -->
        <!-- TODO: turn counts into doughnut chart -->
        <p style="color:tomato">[chart complete per total]</p>
        <p style="color:tomato">[chart urgent per total]</p>
        <p style="color:tomato">[chart late per total]</p>
        <p style="color:tomato">[compare manual and database file?]</p>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: "Ongoing",
    data() {
        return {
            tickets: []
        }
    },
    // TODO: use computed to show only completed tickets
    // TODO: use Array.reduce() to count ticket.complete
    async created() {
        const {data} = await axios.get("http://localhost:3000/tickets");
        this.tickets = data;
    }
}
</script>

<style lang="scss" scoped>

</style>