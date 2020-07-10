<template>
<div>
<v-container>
  <v-layout row wrap>
    <v-flex v-for="i in 5"
    :key="i" lg4>
  <v-card 
    class="ma-3 "
    width='250'
    
  >
    <v-sheet
      class="v-sheet--offset mx-auto"
      color="cyan"
      elevation="12"
      max-width="calc(100% - 32px)"
      height='100'
    >
      <v-sparkline
        :labels="labels"
        label-size='12'
        :value="value[i-1]"
        color="white"
        line-width="2"
        padding="16"
        height='100'
      ></v-sparkline>
    </v-sheet>

    <v-card-text class="pt-0">
      <v-divider class="my-2"></v-divider>
      <v-icon
        class="mr-2"
        small
      >
        mdi-clock
      </v-icon>
      <span class="caption grey--text font-weight-light">{{namee[i-1]}}</span>
    </v-card-text>
  </v-card>
    </v-flex>
  </v-layout>
</v-container>

</div>
</template>

<script>
export default {
 data: () => ({
        namee:['amazon','google','facebook','microsoft','tiktok'],
        labels: ['12am','3am','6am','9am','12pm','3pm','6pm','9pm',],
        value: [[200,675,410,390,310,460,250,240],[340,234,280,310,100,100,500,300],[340,234,180,110,500,300,200,100],
        [340,134,480,310,300,100,400,300],[340,534,480,110,500,100,200,300]],
     
    }),
}
</script>

<style>
.v-sheet--offset {
    top: -1px;
    position: relative;
    
  }
</style>