<template>
  <b-card
    :img-src="`https://www.countryflags.io/${code}/flat/64.png`"
    img-alt="Country image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <template v-slot:header>
      <h4 v-if="province !== null" class="mb-0">{{ country }}  - {{ province }}</h4>
      <h4 v-else class="mb-0">{{ country }}</h4>
    </template>

    <b-list-group flush>
      <b-list-group-item>Confirmed cases: <strong>{{ confirmedCases | thousands }}</strong></b-list-group-item>
      <b-list-group-item>Recovered cases: <strong>{{ recoveredCases | thousands }}</strong></b-list-group-item>
      <b-list-group-item>Deaths cases: <strong>{{ deathsCases | thousands}}</strong></b-list-group-item>
    </b-list-group>

    <b-button to="/specific" variant="primary" class="mt-2">See more</b-button>
  </b-card>
</template>

<script>
export default {
    filters: {
        thousands: value => {
            return `${('' + value).replace(/\B(?=(\d{3})+(?!\d))/g, ',')}`
        }
    },
    props: {
        country: {
            type: String,
            required: false,
            default: 'China'
        },
        province: {
            type: String,
            required: false,
            default: 'Hubei'
        },
        code: {
            type: String,
            required: false,
            default: 'CN'
        },
        confirmedCases: {
            type: Number,
            required: false,
            default: 0
        },
        recoveredCases: {
            type: Number,
            required: false,
            default: 0
        },
        deathsCases: {
            type: Number,
            required: false,
            default: 0
        }
    }
}
</script>