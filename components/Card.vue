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
        text: {
            type: String,
            required: false,
            default: '',
            validator: value => {
                return value.length >= 1
            }
        },
        country: {
            type: String,
            required: false,
            default: 'China',
            validator: value => {
                return value.length >= 1
            }
        },
        province: {
            type: String,
            required: false,
            default: 'Hubei',
            validator: value => {
                return value.length >= 1
            }
        },
        code: {
            type: String,
            required: false,
            default: 'CN',
            validator: value => {
                return value.length >= 1
            }
        },
        confirmedCases: {
            type: String,
            required: false,
            default: 0,
            validator: value => {
                return value.length >= 0
            }
        },
        recoveredCases: {
            type: String,
            required: false,
            default: 0,
            validator: value => {
                return value.length >= 0
            }
        },
        deathsCases: {
            type: String,
            required: false,
            default: 0,
            validator: value => {
                return value.length >= 0
            }
        }
    }
}
</script>