
<template>
    <div class="bg-white bg">
      <!-- <div class="button-area d-flex justify-content-evenly">
        <Button class="run-btn bg-red run" text="一鍵跑路🏃" fontSize="35px" padding="10px"></Button>
      </div> -->
      <div class="suggest px-5 d-flex flex-row">
        <div class="step1 d-flex flex-row" v-if="suggestInfo.currentStep >= 1">
            <div class="d-flex align-items-center">
                <Textspan text="學歷は" :fontSize="45" class="run-span bg-red"/>
            </div>
            <div class="d-flex flex-column ms-4">
                <Checkbox 
                    :options="['碩士之上', '碩士', '本科', '專科', '高中', '高中之下']" 
                    textDirection="row" 
                    layoutDirection="col"
                    :exlusive="true"
                    @click="nextStep()"
                />  
            </div>
        </div>
        <div class="step2 d-flex flex-row" v-if="suggestInfo.currentStep >= 2">
            <div class="d-flex align-items-center">
                <Textspan text="金幣は" :fontSize="45" class="run-span bg-red"/>
            </div>
            
                <Checkbox 
                    :options="['<1', '[1,5]', '[5,10]', '>10']" 
                    textDirection="row" 
                    layoutDirection="col"
                    :exlusive="true"
                    @click="nextStep()"
                    class="d-flex align-items-center ms-4"
                /> 
            
        </div>
      </div>
    </div> 
</template>
    
<script lang="ts">
import Button from '@/components/general/Button.vue';
import Checkbox from '@/components/general/Checkbox.vue'
import Textspan from '@/components/general/TextSpan.vue'

export default {
    components: {
    Button,
    Checkbox,
    Textspan
    },
    data: () => {
    return {
        suggestInfo: {
            currentStep: 1
        }
    }
    },
    methods: {
    nextStep() {
        this.suggestInfo.currentStep++;
    },
    prevStep() {

    }
    }
}
</script>

<style scoped>
div.bg {
    width: 100%;
    height: 1000px;
}

div[class~='step'] {
    transition: 0.1s all;
}


</style>