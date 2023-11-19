<template>
  <div>

    <div class="grid-container">
      <!-- Home Section -->

      <section class="homeSection">
        <img :src=imagePath class="mobile-img" alt="">
        <img :src=imagePath2 class="desktop-img" alt="">
        <div class="homeContainer">
          <h1 class="titleHome">The Bright Future of Web 3.0?</h1>
          <div class="smallContainer">
            <p class="text">We dive into the next evolution of the web that claims to put the power of the platforms back
              into the hands of the people.
              But is it really fulfilling its promise?</p>
            <button class="btn">Read More</button>
          </div>
        </div>
      </section>

      <!-- New Comp Section -->
      <section class="newSection">
        <div class="outerBoxNewComp">
          <h1 class="titleNewComp">New</h1>
          <div class="boxNewComp">
            <h3 class="offWhiteTitle">Hydrogen VS Electric Cars</h3>
            <p class="offWhiteText">Will hydrogen-fueled cars ever catch up to EVs?</p>
          </div>
          <hr>
          <div class="boxNewComp">
            <h3 class="offWhiteTitle">The Downsides of AI Artistry</h3>
            <p class="offWhiteText">What are the possible adverse effects of on-demand AI image generation?</p>
          </div>
          <hr>
          <div class="boxNewComp">
            <h3 class="offWhiteTitle">Is VC Funding Drying Up?</h3>
            <p class="offWhiteText">Private funding by VC firms is down 50% YOY. We take a look at what that
              means.</p>
          </div>
        </div>
      </section>
      </div>

      <!-- Bright Comp Section -->

      <section>
        <div class="outerBox">
          <div class="box">
            <img :src="imagePath3" class="box-img" alt="">
            <div class="textBox">
              <h2 class="m-0 number">01</h2>
              <h4 class="m-0 title">Reviving Retro PCs</h4>
              <p class="m-0 newsText">What happens when old PCs are given modern upgrades?</p>
            </div>
          </div>
          <div class="box">
            <img :src="imagePath4" class="box-img" alt="">
            <div class="textBox">
              <h2 class="m-0 number">02</h2>
              <h4 class="m-0 title">Top 10 Laptops of 2022</h4>
              <p class="m-0 newsText">Our best picks for various needs and budgets.</p>
            </div>
          </div>
          <div class="box">
            <img :src="imagePath5" class="box-img" alt="">
            <div class="textBox">
              <h2 class="m-0 number">03</h2>
              <h4 class="m-0 title">The Growth of Gaming</h4>
              <p class="m-0 newsText">How the pandemic has sparked fresh opportunities.</p>
            </div>
          </div>
        </div>
      </section>
    

  </div>
</template>

<script>
export default {
  data() {
    return {
      imagePath: require('@/assets/image-web-3-mobile.jpg'),
      imagePath2: require('@/assets/image-web-3-desktop.jpg'),
      imagePath3: require('@/assets/image-retro-pcs.jpg'),
      imagePath4: require('@/assets/image-top-laptops.jpg'),
      imagePath5: require('@/assets/image-gaming-growth.jpg')
    }
  }
}
</script>

<style scoped>
/*Home Comp Styling Start*/
.mobile-img {
  display: none;
}

.desktop-img {
  width: 100%;
}

.titleHome {
  font-size: 4rem;
  font-weight: 800;
  width: 39%;
  margin: 0;
}

.text {
  line-height: 2rem;
  color: var(--darkGrayishBlue);
  font-size: 1.3rem;
  margin: 0;
}

.btn {
  background-color: var(--softRed);
  color: #fff;
  padding: 1rem 2rem;
  border: none;
  text-transform: uppercase;
  font-weight: 700;
  margin-bottom: 2.5rem;
  width: 50%;
}

/* Grid Styling Start */

.grid-container{
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  grid-template-rows: repeat(2, 40%);
  gap: 2rem;
}

.homeContainer{
  display: flex;
  justify-content: space-between;
  margin-top: 1rem;
}

.smallContainer{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 50%;
}

.homeSection{
  grid-column: 1 / 6;
  grid-row: 1 ;
}

.newSection{
  grid-column: 6 / -1;
  grid-row: 1 / -1;
}

/* Grid Styling End */

/*Home Comp Styling End*/

/* Bright Future Styling Start */

img {
  display: block;
  max-width: 100%;
}

.outerBox{
  display: flex;
}

.box-img {
  object-fit: cover;
  aspect-ratio: 1 / 1;
}

.box {
  display: flex;
  margin-block: 2rem;
}

.textBox {
  padding-left: 1rem;
}

.newsText{
  color: #000;
  width: 80%;
}

.number {
  color: var(--grayishBlue);
}

.title {
  color: var(--veryDarkBlue);
  padding-block: 1rem;
  font-size: 1.5rem;
}

/* Bright Future Styling End */

/* New Comp Styling Start*/

.outerBoxNewComp {
  background-color: var(--veryDarkBlue);
  padding: 2rem 2rem 0 2rem;
}

.titleNewComp {
  color: var(--softOrange);
  margin: 0;
  font-size: 3rem;
}

.boxNewComp {
  padding-block: 1rem;
}

.offWhiteTitle {
  color: var(--offWhite);
  font-size: calc(16px + .4vw);
}

.offWhiteText{
  color: var(--offWhite);
  font-size: calc(16px + 0.1vw);
  font-weight: 400;
  line-height: 2rem;
}

.offWhiteText:last-child{
  margin-bottom: 0;
}

/*New Comp Styling End*/

@media screen and (width <= 76.313rem) {
  .desktop-img {
    display: none;
  }

  .mobile-img {
    display: block;
    width: 100%;
  }

  .btn{
    margin: 1rem 0 1rem 0;
  }

  .homeContainer{
    flex-direction: column;
  }

  .titleHome{
    width: 100%;
    margin-block: 1rem;
  }

  .smallContainer{
    width: 100%;
  }

  .outerBox{
    flex-direction: column;
  }

  .title{
    font-size: 2.5rem;
  }

  .newsText{
    font-size: 2rem;
  }

  .grid-container{
    display: flex;
    flex-direction: column;
  }
}

@media screen and (width <= 38.875rem){
  .box{
    flex-direction: column;
  }

  .box-img{
    aspect-ratio: 1 / 1;
    width: 100%;
    padding-bottom: 1rem;
  }

  .title{
    font-size: 2rem;
  }

  .newsText{
    font-size: 1rem;
  }
}
</style>