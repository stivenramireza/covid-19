<template>
    <div>
        <b-jumbotron bg-variant="dark" text-variant="white" border-variant="dark">
            <template v-slot:header>COVID-19</template>

            <template v-slot:lead>
            CDC is responding to a pandemic of respiratory disease spreading from person-to-person caused by a novel (new) coronavirus. The disease has been named “coronavirus disease 2019” (abbreviated “COVID-19”). This situation poses a serious public health risk. The federal government is working closely with state, local, tribal, and territorial partners, as well as public health partners, to respond to this situation. COVID-19 can cause mild to severe illness; most severe illness occurs in older adults.
            </template>
        </b-jumbotron>
        <div class="container">
            <Card text="123" />
        </div>
    </div>
</template>

<script>    
import Card from '@/components/Card.vue'

export default {
    components: {
        Card
    },
    data() {
        return {
            
        }
    }
}
</script>