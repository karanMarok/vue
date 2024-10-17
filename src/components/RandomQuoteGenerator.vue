<template>
    <div class="flex justify-center">
        <div class="bg-gray-300 w-5/12 text-center rounded-lg">
            <h1 class="text-2xl mb-4">Random Quote Generator</h1>

            <div>
                <p class="mb-4">{{ selectedQuote.quoteText }}</p>
                <h3 class="mb-4"> - {{ selectedQuote.author }}</h3>
            </div>

            <button type="button" @click.prevent="getQuote" class="p-2 bg-black text-white rounded-md">Get
                Quote</button>

        </div>
    </div>
</template>

<script>
export default {
    name: 'RandomQuoteGenerator',
    data() {
        return {
            quotes: [
                { id: 1, quoteText: "Be the Change you want to see in the World!", author: "Mahatma Gandhi" },
                { id: 2, quoteText: "Together, We Can!", author: "Barack Obama" },
                { id: 3, quoteText: "We must know where we come from, otherwise how would we know where we are going!", author: "Shashi Tharoor" },
                { id: 4, quoteText: "Life must be great rather than long!", author: "BR Ambedkar" },
                { id: 5, quoteText: "Work on yourself!", author: "Swami Vivekanada" },
            ],
            selectedQuote: { id: 0, quoteText: "Welcome to the Random Quote Generator!", author: "Team Random Quotes" },
        }
    },
    methods: {
        getQuote() {
            let randomIndex = Math.floor(Math.random() * this.quotes.length);

            this.selectedQuote = this.quotes[randomIndex];
        }
    }
}
</script>