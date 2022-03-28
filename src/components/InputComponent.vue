<template>
    <v-container fluid>
        <div>
            <v-row align="center">
                <v-col>
                    <v-text-field
                        v-model="drivers.name"
                        label="Enter Driver"
                    ></v-text-field>
                </v-col>
                <v-col
                    ><v-text-field
                        v-model="drivers.points"
                        label="Enter Points"
                    ></v-text-field
                ></v-col>
                <v-btn @click="addDriver" class="mx-1" fab dark color="green">
                    <v-icon dark> mdi-plus </v-icon>
                </v-btn>
            </v-row>
        </div>

        <div class="driver-table">
            <v-simple-table>
                <template v-slot:default>
                    <thead>
                        <tr>
                            <th align="left">Driver</th>
                            <th class="text-left">Points</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="driver in drivers" :key="driver.id">
                            <td align="left">{{ driver.name }}</td>
                            <td align="center">{{ driver.points }}</td>
                        </tr>
                    </tbody>
                </template>
            </v-simple-table>
        </div>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            drivers: [
                {
                    id: "1",
                    name: "",
                    points: "",
                },
            ],
        };
    },
    methods: {
        addDriver() {
            let newDriver = {
                id: this.drivers.id++,
                name: this.drivers.name,
                points: this.drivers.points,
            };

            this.drivers.push(newDriver);
            this.drivers.name = "";
            this.drivers.points = "";
        },
    },
};
</script>
