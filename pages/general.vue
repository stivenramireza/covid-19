<template>
    <div>
        <b-jumbotron bg-variant="dark" text-variant="white" border-variant="dark">
            <template v-slot:header>COVID-19</template>

            <template v-slot:lead>
            CDC is responding to a pandemic of respiratory disease spreading from person-to-person caused by a novel (new) coronavirus. The disease has been named “coronavirus disease 2019” (abbreviated “COVID-19”). This situation poses a serious public health risk. The federal government is working closely with state, local, tribal, and territorial partners, as well as public health partners, to respond to this situation. COVID-19 can cause mild to severe illness; most severe illness occurs in older adults.
            </template>
        </b-jumbotron>
        <div class="container">
            <div class="row">
                <b-card-group columns>
                    <Card
                        v-for="(item, index) in countries"
                        :key="index"
                        :country="item.countryRegion"
                        :province="item.provinceState"
                        :code="item.iso2"
                        :confirmed-cases="item.confirmed"
                        :recovered-cases="item.recovered"
                        :deaths-cases="item.deaths"
                    />
                </b-card-group>
            </div>
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
        return{
            countriesList: []
        }
    },
    mounted(){
        this.countries.forEach(country => {
            this.countriesList.push(country.countryRegion)
        });
        this.countriesList = this.countriesList.filter((item, index) => this.countriesList.indexOf(item) === index)
        console.log(this.countriesList)
    },
    async asyncData({ params, query, $axios, error, store }) {
        try {
            const url = `https://covid19.mathdro.id/api/confirmed`
            const { data } = await $axios.get(url)
            return {
                countries: data
            }
        } catch (error) {
            return error
        }
    },
    methods: {
        async getCountryInfo(country) {
            try {
                const url = `https://covid19.mathdro.id/api/countries/${country}`
                const { data } = await $axios.get(url)
                return {
                    country: data
                }
            } catch (error) {
                return error
            }
        }
    }
}
</script>