<template>

    <div>
        <canvas ref="canvas" id="canvas"></canvas>
    </div>

</template>

<script>
import { Line } from "vue-chartjs";

export default {
    extends: Line,
    methods:{
        callAfterOneMinute(){
            this.renderChart(
                {
                    labels: [
                        "January",
                        "February",
                        "March",
                        "April",
                        "May",
                        "June",
                        "July"
                    ],
                    datasets: [
                        {
                            label: "Data 1",
                            data: [2, 10, 5, 9, 0, 6, 20],
                            backgroundColor: "transparent",
                            borderColor: "rgba(1, 116, 188, 0.50)",
                            pointBackgroundColor: "rgba(171, 71, 188, 1)"
                        }
                    ]
                },
                {
                    responsive: true,
                    maintainAspectRatio: false,
                    title: {
                        display: true,
                        text: "My Data"
                    }
                }
            );
        },
        callIntervalGraph(){
            setInterval(()=>{
                this.callAfterOneMinute();
            },5e3);
        }
    },
    mounted() {
        this.callAfterOneMinute();
        this.callIntervalGraph();
    }
};
</script>
