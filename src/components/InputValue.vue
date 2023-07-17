<template>
    <div id="test-container"> 
        <label for="num-input">
            <input type="number" id="num-input" v-model="num" />
            <p id="formatted-input">{{ formatted_num }}</p>
        </label>
    </div>
</template>

<script>
import { defineComponent, ref, watch } from "vue";

export default defineComponent({
    name:"JesusInput1",

    setup(){

        const num = ref(0);
        const formatted_num = ref('0');

        watch(num, () => {
            formatted_num.value = '$' + formatCurrency(num.value);
        });

        const formatCurrency = (value)=> {
            value = Intl.NumberFormat('es-CO', { 
                // style: 'none', 
                currency: 'COP', 
                minimumFractionDigits: 0, 
                maximumFractionDigits: 0 
            }).format(Number(value));
            value = value.replace(/\$\s/g,"");
            return value;
        };


        return {
            num,
            formatted_num
        }
    }
})
</script>

<style scoped>
    #test-container {
        align-content: center;
        justify-content: center;
        text-align: center;
    }
    #num-input {
        opacity: 0;
        cursor: default;
       
    }
    #formatted-input{
       text-align: start;
       cursor: text;
       max-width: max-content;
       min-width: 300px;
       margin: auto;
       padding: 5px 10px;
       color: #f8f8f8;
       border-bottom: 1px solid rgb(255, 255, 255);
    }
    #formatted-input:hover{
       color: rgb(119, 119, 119);
       background-color: rgb(193, 225, 253);
       border-top-right-radius: 10px;
    }

</style>