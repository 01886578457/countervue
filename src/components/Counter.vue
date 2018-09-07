<template>
    <div>
        <counter-value :count="count"></counter-value>
        <div>
            <counter-button>+</counter-button>
            <counter-button>-</counter-button>
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
        }
    }
};
</script>