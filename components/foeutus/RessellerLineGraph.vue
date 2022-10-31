<template>

    <div class="mt-[57px] w-full">
        <div>
          <CustomSelect :options="['Order Information', 'python', 'rust', 'javascript']"
      :default="'Order Information'" :cssClass="'max-w-[343px]'"
      class="select" />
        </div>

        <div class="flex justify-between pr-[53px] pt-[39px] pb-[47px]">
            <!-- legend -->
            <div class="flex space-x-[14px] items-center">
                <div class="flex space-x-[9px] items-center">
                    <div class="w-[12px] h-[12px] rounded-[1px] bg-[#4489FE]"></div>
                    <div class="text-gray-dark w-[35px] rounded-[2px] font-roboto  text-[14px] text-center font-[400] leading-[16.41px]">Profit</div>

                </div>
                <div class="flex space-x-[9px] items-center">
                    <div class="w-[12px] h-[12px] rounded-[1px] bg-[#FF9F00]"></div>
                    <div class="text-gray-dark font-roboto text-[14px] text-center font-[400] leading-[16.41px]">Order Volume</div>

                </div>

            </div>
            <!-- peroid -->
            <div class="flex">
                <button type="button"
                    class="text-gray-dark w-[35px] rounded-[2px] font-roboto text-[12px]  font-[400] leading-[14.06px] hover:cursor-pointer ">
                    <span class=" font-roboto"> 1D </span>
                </button>
                <button type="button"
                    class="text-gray-dark w-[35px] rounded-[2px] font-roboto text-[12px]  font-[400] leading-[14.06px] hover:cursor-pointer ">
                    <span class=" font-roboto"> 7D </span>
                </button>
                <button type="button"
                    class="text-gray-dark w-[35px] rounded-[2px] font-roboto text-[12px]  font-[400] leading-[14.06px] hover:cursor-pointer ">
                    <span class=" font-roboto"> 1M </span>
                </button>
                <button type="button"
                    class="text-gray-dark w-[35px] rounded-[2px] font-roboto text-[12px]  font-[400] leading-[14.06px] bg-blue-dark hover:cursor-pointer">
                    <span class=" text-white "> 1Y </span>
                </button>
                <button type="button"
                    class="text-gray-dark w-[59px] rounded-[2px] font-roboto text-[12px]  font-[400] leading-[14.06px] hover:cursor-pointer  ">
                    <span class=" font-roboto"> Custum </span>
                </button>
            </div>
        </div>


        <div>
            <LineChartGenerator :chart-options="chartOptions" :chart-data="chartData" :chart-id="chartId"
                :dataset-id-key="datasetIdKey" :plugins="plugins" :css-classes="cssClasses" :styles="styles"
                :width="width" :height="height" />
        </div>


    </div>


</template>

<script>
import { Line as LineChartGenerator } from 'vue-chartjs'
import CustomSelect from '../embrillons/CustomSelect.vue';

import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    LineElement,
    LinearScale,
    CategoryScale,
    PointElement
} from 'chart.js'

ChartJS.register(
    Title,
    Tooltip,
    Legend,
    LineElement,
    LinearScale,
    CategoryScale,
    PointElement
)

export default {
    name: 'RessellerLineGraph',
    components: {
        LineChartGenerator,
        
        CustomSelect
    },
    props: {
        chartId: {
            type: String,
            default: 'line-chart'
        },
        datasetIdKey: {
            type: String,
            default: 'label'
        },
        width: {
            type: Number,
            default: 800
        },
        height: {
            type: Number,
            default: 400
        },
        cssClasses: {
            default: 'font-roboto',
            type: String
        },
        styles: {
            type: Object,
            default: () => { }
        },
        plugins: {
            type: Array,
            default: () => []
        }
    },
    data() {
        return {
            chartData: {

                labels: [
                    'January',
                    'February',
                    'March',
                    'April',
                    'May',
                    'June',
                    'July',
                    'junly'
                ],
                datasets: [
                    {
                        label: 'Profit',
                        borderColor: "#4489FE",
                        pointStyle: 'circle',
                        borderWidth: 2,
                        pointRadius: 7,
                        pointHoverRadius: 15,
                        backgroundColor: 'white',
                        data: [0, 400, 390, 100, 400, 390, 800, 400]
                    },
                     {
                        label: 'Order Volume',
                        borderColor: "#FF9F00",
                        pointStyle: 'circle',
                        borderWidth: 2,
                        pointRadius: 7,
                        pointHoverRadius: 15,
                        backgroundColor: 'white',
                        data: [0,200, 140, 300, 760, 420, 110, 500]
                    }
                ]
            },


            chartOptions: {
                aspectRatio: 3,
                
                responsive: true,
                inflateAmount: "1",
                plugins: {
                    legend: {
                        display: false,
                        align: "start",
                        labels: {
                            padding: 20,
                            color: "#757575",
                            boxWidth: 12,
                            boxHeight: 12,
                            backgroundColor: ["#4489FE","#FF9F00"],
                            font: {
                                size: 14,
                                family: "Roboto"
                        
                    }
                        },
                    },
                },

                layout: {},

                scales: {
                    x: {
                        stacked: true,
                        ticks: {
                            font: {
                                size: 12,
                            },
                        },
                        grid: {
                            display: false,
                        },
                    },
                    y: {
                        
                        position: "right",
                        grid: {
                            display: true,
                            drawBorder: false,
                        },
                        ticks: {
                            beginAtZero: true,
                            stepSize: 100,
                            min: 0,
                            padding:19

                        },
                    },
                },
            },
        }
    }
}
</script>
<style scoped>
.period-content {
    font-weight: 400;
    font-size: 12px;
    line-height: 14px;
    color: #757575;
}

button {
    margin-right: 10px;
}

.active-text {
    color: white;
}

.active-button-bg {
    background: #4489fe;
}

</style>