<template>
  <div style="margin-top:50px; padding-bottom:40px;padding-top:30px;">
   <h4 style="text-align:center; color:#f6142a;">Photo Gallery</h4>
  </div>
  <div style="width:800px; margin:0 auto;"> 
    <b-carousel
      id="carousel1"
      style="text-shadow: 1px 1px 2px #333;"
      controls
      indicators
      background="#ababab"
      :interval="4000"
      img-width="1024"
      img-height="480"
      v-model="slide"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide
      img-src="https://img1.wsimg.com/isteam/ip/5abd5167-563b-48a9-94e9-5ed58bc0fbf8/964399b6-7d83-43cd-97c9-63a786a1b303.JPG/:/rs=w:400,h:500,cg:true,m/cr=w:800,h:500,a:cc"
      />

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://img1.wsimg.com/isteam/ip/5abd5167-563b-48a9-94e9-5ed58bc0fbf8/2298e732-cb60-4d48-8dcd-6c8a242f2aa2.JPG/:/rs=w:400,h:500,cg:true,m/cr=w:800,h:500,a:cc">
        
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="https://img1.wsimg.com/isteam/ip/5abd5167-563b-48a9-94e9-5ed58bc0fbf8/ba702acd-5193-4f56-a308-0e68a5bfada9.JPG/:/rs=w:400,h:500,cg:true,m/cr=w:800,h:500,a:cc" />

      <b-carousel-slide>
        <img
          slot="img"
          class="d-block img-fluid w-100"
          width="1024"
          height="480"
          src="https://img1.wsimg.com/isteam/ip/5abd5167-563b-48a9-94e9-5ed58bc0fbf8/e1f428fe-1397-4028-b5ff-00dccfdc6a62.JPG/:/rs=w:400,h:500,cg:true,m/cr=w:800,h:500,a:cc"
          alt="image slot"
        />
      </b-carousel-slide>
    </b-carousel>
    </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
      sliding: null
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
    },
    onSlideEnd(slide) {
      this.sliding = false;
    }
  }
};
</script>