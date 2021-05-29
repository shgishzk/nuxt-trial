<template>
    <div>
        <v-row>
            <v-col cols="12" sm="12" md="12" lg="12">
                <chartCard />
            </v-col>
        </v-row>
    </div>
</template>

<script>
import chartCard from '~/components/ChartCard.vue';
export default {
    components: {
        chartCard,
    }
}
</script>