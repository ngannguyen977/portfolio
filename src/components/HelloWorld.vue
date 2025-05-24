<template>
  <div id="horizontal" class="scrollContainer">
    <div class="loading-page content-section section">
      <div class="text-center align-items-center user-info">
        <div class="image">
          <img class="img-user" :src="userImg" />
        </div>
        <div class="info">
          <h5 class="text-white font-weight-normal small-text">I'm</h5>
          <h1 class="user-name text-uppercase">NGAN NGUYEN</h1>
          <code>UI/UX Design - Frontend Developer</code><br><br>
          <span>Please scroll to the next page </span>
          <span><img class="right-arrow" :src="rightArrowImg" /></span>
        </div>
      </div>
      <div class="scroll">
        <!-- Your scroll content remains the same -->
      </div>
    </div>

    <section id="section01" class="content-section section blue">
      <div class="">
        <div class="section-content">
          <div class="title">
            <h2><span>I work with</span> <br> tools <br>& framworks</h2>
            <h4>Some design tools and frameworks I use in my projects.</h4>
          </div>
          <div class="flex">
            <div class="box-content">
              <div class="ds-flex">
                <div class="col-4 box box01">
                  <h3 class="bl">Figma</h3>
                  <img :src="figmaIcon" />
                </div>
                <div class="col-4 box box02 white">
                  <h3 class="">Adobe</h3>
                  <img :src="adobeIcon" />
                </div>
                <div class="col-4 box box03">
                  <h3 class="bl">Vuejs</h3>
                  <img :src="vuejsIcon" />
                </div>
              </div>
              <div class="ds-flex">
                <div class="col-4 box box02">
                  <h3 class="bl white">HTML</h3>
                  <img :src="htmlIcon" />
                </div>
                <div class="col-4 box box01">
                  <h3 class="">Boostrap</h3>
                  <img :src="bootstrapIcon" />
                </div>
                <div class="col-4 box box02">
                  <h3 class="bl white">CSS</h3>
                  <img :src="cssIcon" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Other sections remain the same until contact section -->

    <section id="section03" class="content-section section">
      <div class="">
        <div class="content">
          <h1>Thank you !</h1>
          <div class="typed-out">I believe with my experience, sensitivity, enthusiasm and responsibility in work. I will
            do a good job and build a truly effective team.</div>
          <div class="contact">
            <div class="display-flex">
              <p><img :src="phoneIcon" alt="" class="">Phone: <b>0981029889</b><span> </span></p>
              <p><img :src="mailIcon" alt="" class="">Email:<b> ngannguyen977@gmail.com</b><span></span></p>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import "./style.scss";

// Import all images
import userImg from '@/assets/user.png'
import rightArrowImg from '@/assets/right-arrow.png'
import figmaIcon from '@/assets/section03/figma.svg'
import adobeIcon from '@/assets/section03/adobe.svg'
import vuejsIcon from '@/assets/section03/vuejs.svg'
import htmlIcon from '@/assets/section03/html.svg'
import bootstrapIcon from '@/assets/section03/b.svg'
import cssIcon from '@/assets/section03/css3.svg'
import phoneIcon from '@/assets/phones.png'
import mailIcon from '@/assets/mail.png'

export default {
  data() {
    return {
      // Assign imported images to data properties
      userImg,
      rightArrowImg,
      figmaIcon,
      adobeIcon,
      vuejsIcon,
      htmlIcon,
      bootstrapIcon,
      cssIcon,
      phoneIcon,
      mailIcon
    }
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    const sections = gsap.utils.toArray("#horizontal .content-section");
    gsap.to(sections, {
      xPercent: -100 * (sections.length - 1),
      scrollTrigger: {
        trigger: "#horizontal",
        pin: true,
        scrub: 1,
        snap: 1 / (sections - 1),
        end: "+=3500",
      },
    });
  },
};
</script>

<style scoped lang="scss">
/* Your existing styles remain the same */
</style>