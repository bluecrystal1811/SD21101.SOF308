<template>
    <div>
        <h3 class = "text-blue">Count: {{ state.count }}</h3>
        <h3 :class="state.count>5 ? 'text-danger' : 'text-blue'">Count: {{ state.count }}</h3>
        <button @click="increment">Increment</button>
        <h3>Name: {{ state.user.name }}</h3>
        <h3>Age: {{ state.user.age }}</h3>
        <h3>Street: {{ state.user.address.street }}</h3>
        <h3>City: {{ state.user.address.city }}</h3>
        <h3>State: {{ state.user.address.state }}</h3>
        <h3>ZIP: {{ state.user.address.zip }}</h3>
    </div>
</template>

<script>
import { reactive } from 'vue'

export default {
    setup () {
        const state = reactive({
            count: 0,
            user: {
                name: 'Do Minh Khoi',
                age: 19,
                address: {
                    street: '123 Nguyen Van Linh',
                    city: 'Da Nang',
                    state: 'Vietnam',
                    zip : '550000'
                }
            },
        })
        const increment = () => {
            state.count++
        }
        return {state,increment}
    }
}
</script>

<style lang="scss" scoped>
    .text-danger {
        color: red;
    }
    .text-blue {
        color: blue;
    }
</style>