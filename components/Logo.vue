<template>
  <div class="logo">
    <span
      v-if="reloaded && $vuetify.breakpoint.mdAndUp"
      class="logo__letter logo__letter-white"
      >EN</span
    >
    <svg id="compas" viewBox="0 0 161.484 324.423">
      <g>
        <path
          fill="#0E0E0E"
          d="M73.491,0h17.541c-0.044,13.073-0.088,26.146-0.132,39.219c3.502,0.796,10.263,2.829,16.75,8.403
		c8.693,7.469,11.56,16.713,12.528,20.875c0.884,3.803,2.658,11.942-0.987,21.132c-2.502,6.307-6.469,10.368-8.843,12.454
		c-0.54-2.25-1.08-4.5-1.621-6.75c1.5-1.996,3.159-4.684,4.424-8.076c0.505-1.353,1.697-5.175,2.009-10.325
		c0.114-1.878,0.098-4.623-0.618-7.809c-1.825-8.12-6.88-13.168-9.55-15.813c-2.199-2.178-5.392-5.275-10.613-7.283
		c-5.592-2.15-10.415-1.86-13.498-1.641c-5.894,0.418-10.606,2.196-13.778,3.757c-2.034,1.297-4.742,3.266-7.515,6.106
		c-1.771,1.814-3.922,4.016-5.793,7.515c-2.377,4.445-2.902,8.389-3.288,11.273c-0.285,2.126,0.308,10.907,1.358,13.713
		c0.642,1.714,1.289,2.949,1.987,4.257c0.721,1.352,1.726,3.091,3.074,5.046c-0.62,2.2-1.24,4.401-1.86,6.601
		c-1.68-1.712-3.782-4.199-5.655-7.54c-0.685-1.222-2.315-4.299-3.444-8.611c-0.292-1.116-1.569-6.203-1.077-13.062
		c0.217-3.027,0.514-7.157,2.642-11.989c1.819-4.13,4.095-6.744,6.471-9.508c2.09-2.431,4.454-5.185,8.403-7.714
		c4.145-2.655,8.077-3.825,10.646-4.384L73.491,0z"
        />
        <path
          fill="#0E0E0E"
          d="M60.997,78.517l22.007,6.419L35.32,292.228l-14.717,19.101l-3.131-0.783l-3.914,12.056
		c-0.773,1.413-2.331,2.089-3.601,1.722c-1.609-0.464-2.673-2.575-1.819-4.54c1.024-3.705,2.048-7.411,3.072-11.116l-5.167-1.253
		L60.997,78.517z"
        />
        <path
          fill="#0E0E0E"
          d="M104.69,78.517l-22.007,6.419l47.684,207.292l14.717,19.101l3.131-0.783l3.914,12.056
		c0.773,1.413,2.331,2.089,3.601,1.722c1.609-0.464,2.673-2.575,1.819-4.54c-1.024-3.705-2.048-7.411-3.072-11.116l5.167-1.253
		L104.69,78.517z"
        />
        <path
          fill="#0E0E0E"
          d="M0.016,146.148c0.048-0.738,0.359-4.265,3.277-6.772c2.792-2.399,7.549-3.507,11.005-1.1
		c2.759,1.921,3.341,5.069,3.459,5.817l59.586,0.157v-13.678c1.039-2.384,3.275-4.021,5.817-4.245
		c2.803-0.246,5.522,1.265,6.855,3.822c0,4.667,0,9.333,0,14c17.682-0.019,35.364-0.037,53.045-0.056
		c0.198-0.909,0.846-3.252,2.987-4.874c2.106-1.596,4.454-1.582,6.132-1.572c1.16,0.007,2.598,0.015,4.245,0.786
		c2.609,1.222,3.776,3.468,4.088,4.088c1.678,3.333,0.732,6.552,0.452,7.45c-0.256,0.823-0.812,2.534-2.384,4.044
		c-2.076,1.994-4.553,2.318-5.929,2.499c-1.452,0.19-3.272,0.417-5.188-0.472c-3.336-1.547-4.292-5.248-4.448-5.893
		c-17.667,0-35.333,0-53,0c0,4.333,0,8.667,0,13c-0.353,0.731-1.317,2.471-3.356,3.593c-0.603,0.332-1.976,1.059-3.629,0.923
		c-2.584-0.213-4.729-2.145-5.215-4.705c0-4.297,0-8.595,0-12.892l-60.372-0.472c-0.198,0.88-0.859,3.24-3.023,4.759
		c-1.59,1.116-3.217,1.234-5.153,1.373c-1.594,0.115-2.901,0.204-4.402-0.472c-1.627-0.733-2.503-1.96-3.049-2.738
		C-0.168,149.688-0.016,146.646,0.016,146.148z"
        />
      </g>
    </svg>
    <span
      v-if="reloaded && $vuetify.breakpoint.mdAndUp"
      class="logo__letter logo__letter-black"
    >
      LBIS
    </span>
  </div>
</template>

<script>
export default {
  name: 'Logo',
  data: () => ({
    reloaded: false,
  }),
  created() {
    this.$nextTick(function () {
      this.reloaded = true
    })
  },
}
</script>

<style lang="scss" scoped>
#compas {
  width: 8rem;
  @include respond(xs) {
    width: 10rem;
  }
}
.logo {
  display: flex;
  align-items: flex-end;
  @include respond(xs) {
    justify-content: center;
  }
  &__letter {
    font-family: 'Adam';
    font-size: 12rem;
    display: block;
    height: 70%;
    @include respond(xs) {
      font-size: 3rem;
    }
    &-white {
      margin-right: 1.5rem;
      color: white;
      @include respond(xs) {
        margin-right: 1rem;
      }
    }
    &-black {
      color: black;
      margin-left: 1.5rem;
      @include respond(xs) {
        margin-left: 1rem;
      }
    }
  }
}
</style>
