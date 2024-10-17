<template>
    <div class="flex justify-center">
        <div class="w-6/12 bg-white border-2 border-gray-300 rounded-lg">
            <div v-for="(accordion, index) in accordionContent" :key="accordion.id">
                <h1 class="bg-blue-300 p-4 rounded-lg cursor-pointer flex justify-between"
                    @click="toggleAccordion(index)">
                    {{ accordion.heading }}
                    <h3>{{ isVisible[index] ? '-' : '+' }}</h3>
                </h1>
                <p v-if="isVisible[index]" class="p-4">
                    {{ accordion.description }}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Accordion',
    data() {
        return {
            isVisible: [false, false],
            accordionContent: [
                { id: 1, heading: "First Accordion", description: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe quibusdam corporis inventore fuga aperiam odio eveniet voluptas, reiciendis eos perspiciatis." },
                { id: 2, heading: "Second Accordion", description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Temporibus, nobis. Unde, pariatur, velit totam quasi voluptate explicabo corporis illum consequatur at, sunt eligendi est dolor!" }
            ]
        }
    },
    methods: {
        toggleAccordion(index) {
            this.isVisible.splice(index, 1, !this.isVisible[index]);
        }
    }
}
</script>
