<template>
 <div class="fullscreen bg-landing">
		<div class="row justify-center q-gutter-xl" style="padding-top:100px">
					<div class="col-xs-4 col-md-4">
                        <q-card v-ripple class="bg-resume q-pa-xl" @click="onClickResume">
                            <q-card-section class="resume text-center">
						Resume
                            </q-card-section>
                        </q-card>
					</div>
                    <div class="col-xs-4 col-md-4">
						<q-card v-ripple class="bg-project q-pa-xl">
                            <q-card-section class="project text-center" @click="onClickProject">
						Projects
                            </q-card-section>
                        </q-card>
					</div>
                    <div class="col-xs-4 col-md-4">
						<q-card>
                               <q-img src="~assets/plant-unsplash.jpg" style="height:230px; opacity:0.9;"/>
                        </q-card>
					</div>
                    <div class="col-xs-4 col-md-4">
						<q-card class="bg-about q-px-xl">
                            <q-card-section class="text-center">
						        <p class="about">About</p>
                                    <q-separator />
						        <p class="about-desc">I'm Husna. A frontend developer with 8 months experiences.</p>
                            </q-card-section>
                        </q-card>
					</div>
          
        </div>
 </div>
            
</template>

<script>
import { gsap } from "gsap";

export default {
    data() {
        return{

        }
    },
    mounted: function(){
    gsap.from('.bg-about', {duration:4, scale: 2})
  },
    methods: {
        onClickResume() {
            this.$router.push('/resume')
        },
        onClickProject() {
            this.$router.push('/project')
        }
    }
}

</script>
