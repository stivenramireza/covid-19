<template>
  <b-card
    title="Card Title"
    img-src="https://picsum.photos/600/300/?image=25"
    img-alt="Image"
    img-top
    tag="article"
    style="max-width: 20rem;"
    class="mb-2"
  >
    <b-card-text>
      {{ text }}
    </b-card-text>

    <b-button to="/specific" variant="primary">See more</b-button>
  </b-card>
</template>

<script>
export default {
    props: {
        text: {
            type: String,
            required: false,
            default: '',
            validator: value => {
                return value.length >= 1
            }
        }
    }
}
</script>