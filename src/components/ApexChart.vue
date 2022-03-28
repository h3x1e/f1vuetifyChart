<template>
    <v-container>
        <div class="chart">
            <apexchart
                width="500"
                type="bar"
                :options="chartOptions"
                :series="series"
                class="apex-chart"
            ></apexchart>
        </div>
    </v-container>
</template>

<script>
export default {
    data: () => {
        return {
            chartOptions: {
                chart: {
                    id: "F1 2021",
                },
                xaxis: {
                    categories: [
                        "Max Verstappen",
                        "Lewis Hamilton",
                        "Sebastian Vettel",
                        "Charles Leclerc",
                        "Pierre Gasly",
                        "Daniel Ricciardo",
                        "Kimi Räikkönen",
                        "Nico Hulkenberg",
                        "Kevin Magnussen",
                        "Sergio Perez",
                        "Esteban Ocon",
                    ],
                },
            },
            series: [
                {
                    name: "Points",
                    data: [1, 2, 3, 3, 4, 5, 6, 7, 8, 9],
                },
            ],
        };
    },
};
</script>
