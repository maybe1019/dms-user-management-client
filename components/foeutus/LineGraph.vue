<template>

    <div class="mt-[57px] w-full">
        <div>
         <CustomSelect :options="['Order Information', 'python', 'rust', 'javascript']"
      :default="'Order Information'" :cssClass="'w-full max-w-[343px]'"
      class="select" />
        </div>

        <div class="flex justify-between pr-[53px] pt-[39px] pb-[47px]">
            <!-- legend -->
            
              
                <div class="flex space-x-[9px] items-center">
                    <div class="w-[12px] h-[12px] rounded-[1px] bg-blue-dark "></div>
                    <div class="text-gray-dark font-roboto text-[14px] text-center font-[400] leading-[16.41px]">Money ($)</div>

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

        <div class="w-full">
            <LineChartGenerator :chart-options="chartOptions" :chart-data="chartData" :chart-id="chartId"
                :dataset-id-key="datasetIdKey" :plugins="plugins" :css-classes="cssClasses" :styles="styles"
                :width="width" :height="height" />
        </div>


    </div>


</template>

<script>
import CustomSelect from '../embrillons/CustomSelect.vue';
import { Line as LineChartGenerator } from 'vue-chartjs'
import StatSelectFilter from "./../embrillons/StatSelectFilter.vue";

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
    name: 'LineGraph',
    components: {
        LineChartGenerator,
        StatSelectFilter,
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
            default: 0
        },
        height: {
            type: Number,
            default: 0
        },
        cssClasses: {
            default: 'font-roboto w-full',
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
                    'March',
                    'April',
                    'May',
                    'June',
                    'July'
                    
                    
                ],
                datasets: [
                    {
                        label: 'Money($)',
                        borderColor: "#4489FE",
                        pointStyle: 'circle',
                        borderWidth: 2,
                        pointRadius:5 ,
                        pointHoverRadius: 15,
                        backgroundColor: 'white',
                        data: [4000, 3900, 1000, 4000, 3900, 8000, 4000,3900, 1000, 4000, 3900, 8000, 4000]
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
                            color: "#4489FE",
                            boxWidth: 12,
                            boxHeight: 12,
                            backgroundColor: "#4489FE",
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
                        stacked: false,
                        position: "right",
                        grid: {
                            display: true,
                            drawBorder: false,
                        },
                        ticks: {
                            beginAtZero: true,
                            stepSize: 1000,
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


</style>