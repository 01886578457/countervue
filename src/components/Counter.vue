<template>
    <div>
        <counter-value :count="count"></counter-value>
        <div>
            <counter-button @clicked="increment">+</counter-button>
            <counter-button @clicked="decrement">-</counter-button>
            <counter-button @clicked="multiplication">*2</counter-button>
            <counter-button @clicked="division">/2</counter-button>
        </div>
    </div>
</template>

<script>
import CounterButton from './CounterButton';
import CounterValue from './CounterValue';
export default {
    name: 'Counter',
    components: {
        CounterButton,
        CounterValue
    },
    data(){
        return {
            count:999
        };
    },
    methods:{
        increment(){
            this.count++;
        },
        decrement(){
            this.count--;
        },
        multiplication(){
            this.count = this.count * 2;
        },
        division(){
            this.count = this.count / 2;
        }
    }
};
</script>