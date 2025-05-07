<template>
  <div id="horizontal" class="scrollContainer">
    <div class="loading-page content-section section">
      <div class="text-center align-items-center user-info">
        <div class="image">
          <img class="img-user" src="../assets/user.png" />
        </div>
        <div class="info">
          <h5 class="text-white font-weight-normal small-text">I'm</h5>
          <h1 class="user-name text-uppercase">NGAN NGUYEN</h1>
          <code>UI/UX Design - Frontend Developer</code>ƒ
        </div>

      </div>
      <div class="scroll">
        <div class="m-scroll hozRight1">
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>VUE</large> FRAMEWORK
          </span>
          <span>
            <large>HTML</large> FRONTEND
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>CSS</large> STYLE
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
        </div>
        <div class="m-scroll hozRight">
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>VUE</large> FRAMEWORK
          </span>
          <span>
            <large>HTML</large> FRONTEND
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
          <span>
            <large>CSS</large> STYLE
          </span>
          <span>
            <large>GRAPHIC</large> DESIGN
          </span>
        </div>
        <!-- <div class="m-scroll hozLeft">
          <span>
            <b class="fill">UI / UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill txt-pink">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill txt-pink">UI/UX</b>
            <small>DESIGN</small>
          </span>
          <span>
            <b class="fill">UI/UX</b>
            <small>DESIGN</small>
          </span>
        </div> -->
      </div>
    </div>
    <section id="section01" class="content-section section blue">
      <div class="">
        <div class="section-content">
          <div class="title">
            <!-- <h4>And here</h4> -->
            <h2><span>I work with</span> <br> tools <br>& framworks</h2>
            <h4>Some design tools and frameworks I use in my projects.</h4>
          </div>
          <div class="flex">
            <div class="box-content">
              <div class="row">
                <div class="col-4 box box01">
                  <h3 class="bl">Figma</h3>
                  <img src="../assets/section03/figma.svg" />
                </div>
                <div class="col-4 box box02">
                  <h3 class="white">Adobe</h3>
                  <img src="../assets/section03/adobe.svg" />
                </div>
                <div class="col-4 box box03">
                  <h3 class="bl">Vuejs</h3>
                  <img src="../assets/section03/vuejs.svg" />
                </div>
              </div>
              <div class="row">
                <div class="col-4 box box03">
                  <h3 class="bl">Figma</h3>
                  <img src="../assets/section03/figma.svg" />
                </div>
                <div class="col-4 box box02">
                  <h3 class="white">Adobe</h3>
                  <img src="../assets/section03/adobe.svg" />
                </div>
                <div class="col-4 box box01">
                  <h3 class="bl">Vuejs</h3>
                  <img src="../assets/section03/vuejs.svg" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="section02" class="content-section section">
      <div class="row">

        <div class="col-6">
          <div class="col-lg-12 bg-purple height60 relative">
            <div class="des-content">
              <h2 class="">
                Let's see
                <br />
                <p>What did <span class="cl-green">I do?</span></p>
              </h2>
              <p class="">
                Some projects i have done. Besides using adobe software i can also convert them to front end and work
                with
                coder
              </p>
            </div>
          </div>
        <div class="col-lg-12 bg-yellow height40"></div>
          
        </div>
        <div class="col-lg-6">
            <div class="col-lg-12 bg-yellow height50"></div>
            <div class="col-lg-12 height50">
                <div class="col-lg-6 bg-purple width50"></div>
              <div class="col-lg-6 bg-yellow width50"></div>             
            </div>        
        </div>
      </div>
    </section>
    <section id="section03" class="content-section section">
      <div class="">
        <!-- <h1>content 2</h1> -->
        <div class="content">
          <h1>Thank you !</h1>
          <div class="typed-out">believe with my experience, sensitivity, enthusiasm and responsibility in work. I will
            do a good job and build a truly effective team.</div>
            <div class="contact">
              <div>
                <p>Phone:0981029889</p>
                <p>Email: ngannguyen977@gmail.com</p>
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
export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger);

    const sections = gsap.utils.toArray("#horizontal .content-section");

    gsap.to(sections, {
      xPercent: -100 * (sections.length - 1),
      //   ease: "none",
      scrollTrigger: {
        trigger: "#horizontal",
        pin: true,
        scrub: 1,
        snap: 1 / (sections - 1),
        // base vertical scrolling on how wide the container is so it feels more natural.
        end: "+=3500",
        // end: () => "+=" + (sections.offsetWidth - innerWidth),
        //end: () => horizontalScrollContainer.scrollWidth
      },
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
