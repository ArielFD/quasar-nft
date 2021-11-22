<template>
  <q-page class="flex flex-center">
    <q-card 
    class="my-card q-pa-lg primary">

      <div class="q-pa-sm">
        <q-img
          class="rounded-borders "
          img-class="my-custom-image"
          src="../assets/image-equilibrium.jpg"
        />
      </div>
      
      <q-card-section>
          <div class="text-h6 text-accent">
              Equilibrium #3429
          </div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        <div class="text-caption text-primary">
          pOur equilibrium collection promotes balance and calm
        </div>
        <div class="fit row justify-between content-start">
          <q-chip
            dense
            text-color="secondary"
            icon="img:data:image/svg+xml,%3Csvg%20width%3D%2211%22%20height%3D%2218%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%3Cpath%20d%3D%22M11%2010.216%205.5%2018%200%2010.216l5.5%203.263%205.5-3.262ZM5.5%200l5.496%209.169L5.5%2012.43%200%209.17%205.5%200Z%22%20fill%3D%22%2300FFF8%22%2F%3E%3C%2Fsvg%3E"
          >
            0.041 ETH
          </q-chip>
          <q-chip
            dense
            text-color="primary"
            icon="img:data:image/svg+xml,%3Csvg%20width%3D%2217%22%20height%3D%2217%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%3Cpath%20d%3D%22M8.305%202.007a6.667%206.667%200%201%200%200%2013.334%206.667%206.667%200%200%200%200-13.334Zm2.667%207.334H8.305a.667.667%200%200%201-.667-.667V6.007a.667.667%200%200%201%201.334%200v2h2a.667.667%200%200%201%200%201.334Z%22%20fill%3D%22%238BACD9%22%2F%3E%3C%2Fsvg%3E"
          >
            3 days left
          </q-chip>
        </div>
      </q-card-section>

      <q-separator color="primary" />

      <q-card-actions row>
        <q-btn flat col >
          <q-avatar size="md">
            <img src="../assets/image-avatar.png" />
          </q-avatar>
        </q-btn>
        <div class="row">
          <q-btn label="Creation of"  flat no-caps text-color="primary">
          </q-btn>
          <q-btn
            :text-color="data.message ? 'secondary' : 'accent' "
            @mouseover="mouseOver"
            @mouseleave="mouseLeave"
            label="ArielFD"
            flat
            no-caps            
          >
          </q-btn>
        </div>
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script>
import { defineComponent, ref, reactive } from "vue";

export default defineComponent({
  name: "PageIndex",
  setup() {
    let data=reactive({
      message:false
    })

    const mouseOver=()=>{
      data.message=true
    }

    const mouseLeave=()=>{
      data.message=false
    }
    
    return {
      mouseOver,
      mouseLeave,
      data
    };
  },
});
</script>


<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 300px
  background-color: hsl(216, 50%, 16%)
  border-radius: 15px

.q-chip
  background-color: hsl(216, 50%, 16%)
  text-decoration-color: secondary

.my-custom-image
  border-radius: 10px
</style>