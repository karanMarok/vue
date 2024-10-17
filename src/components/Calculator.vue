<template>
    <div class="flex justify-center">
        <div class="bg-gray-300 w-3/12">
            <input type="text" class="w-[97%] rounded-lg m-2 p-2" placeholder="Calculator" v-model="calcString" />

            <div class="grid grid-rows-4 grid-flow-col gap-4">
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="7">7</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="4">4</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="1">1</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="0">0</button>

                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="8">8</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="5">5</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="2">2</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString(" .")"
                    :value=".">.</button>

                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="9">9</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="6">6</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="3">3</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="=">=</button>

                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="/">/</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="*">*</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="-">-</button>
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200" @click="addToString"
                    :value="+">+</button>

            </div>

            <div class="grid grid-rows-1 grid-flow-col gap-4">
                <button class="m-2 p-2 bg-white rounded shadow hover:bg-blue-200">C</button>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'Calculator',
    data() {
        return {
            total: 0,
            calcString: ''
        }
    },
    methods: {
        addToString(event) {
            this.calcString += event.target.value;
        }
    },
    computed: {

    }
}
</script>