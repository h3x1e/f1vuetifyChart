<template>
    <v-container>
        <v-app>
            <ApexChart></ApexChart>
            <InputComponent></InputComponent>
        </v-app>
    </v-container>
</template>

<script>
import ApexChart from "./components/ApexChart.vue";
import InputComponent from "./components/InputComponent.vue";

export default {
    data: () => ({}),
    components: { ApexChart, InputComponent },
};
</script>
