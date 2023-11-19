<template>
    <div>

        <!-- Home Section -->

        <section>
            <img :src=imagePath class="mobile-img" alt="">
            <img :src=imagePath2 class="desktop-img" alt="">
            <h1 class="title">The Bright Future of Web 3.0?</h1>
            <p class="text">We dive into the next evolution of the web that claims to put the power of the platforms back
                into the hands of the people.
                But is it really fulfilling its promise?</p>
            <button class="btn">Read More</button>
        </section>

        <!-- New Comp Section -->
        <section>
            <div class="outerBoxNewComp">
                <h1 class="titleNewComp">New</h1>
                <div class="boxNewComp">
                    <h3 class="offWhiteNewComp">Hydrogen VS Electric Cars</h3>
                    <p class="offWhiteNewComp">Will hydrogen-fueled cars ever catch up to EVs?</p>
                </div>
                <hr>
                <div class="boxNewComp">
                    <h3 class="offWhiteNewComp">The Downsides of AI Artistry</h3>
                    <p class="offWhiteNewComp">What are the possible adverse effects of on-demand AI image generation?</p>
                </div>
                <hr>
                <div class="boxNewComp">
                    <h3 class="offWhiteNewComp">Is VC Funding Drying Up?</h3>
                    <p class="offWhiteNewComp">Private funding by VC firms is down 50% YOY. We take a look at what that
                        means.</p>
                </div>
                <hr>
            </div>
        </section>

        <!-- Bright Comp Section -->

        <section>
            <div class="outerBox">
                <div class="box">
                    <img :src="imagePath" class="box-img" alt="">
                    <div class="textBox">
                        <h2 class="m-0 number">01</h2>
                        <h4 class="m-0 title">Reviving Retro PCs</h4>
                        <p class="m-0">What happens when old PCs are given modern upgrades?</p>
                    </div>
                </div>
                <div class="box">
                    <img :src="imagePath2" class="box-img" alt="">
                    <div class="textBox">
                        <h2 class="m-0 number">02</h2>
                        <h4 class="m-0 title">Top 10 Laptops of 2022</h4>
                        <p class="m-0">Our best picks for various needs and budgets.</p>
                    </div>
                </div>
                <div class="box">
                    <img :src="imagePath3" class="box-img" alt="">
                    <div class="textBox">
                        <h2 class="m-0 number">03</h2>
                        <h4 class="m-0 title">The Growth of Gaming</h4>
                        <p class="m-0">How the pandemic has sparked fresh opportunities.</p>
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
            imagePath: require('@/assets/image-retro-pcs.jpg'),
            imagePath2: require('@/assets/image-top-laptops.jpg'),
            imagePath3: require('@/assets/image-gaming-growth.jpg')
        }
    }
}
</script>

<style scoped>

/*Home Comp Styling Start*/
.mobile-img{
  display: none;
}

.desktop-img{
  width: 100%;
}

.title{
  font-size: 3rem;
}

.text{
  line-height: 1.5rem;
  color: var(--darkGrayishBlue);
  font-size: 1.1rem;
}

.btn{
  background-color: var(--softRed);
  color: #fff;
  padding: 1rem 2rem;
  border: none;
  text-transform: uppercase;
  font-weight: 700;
  margin-bottom: 2.5rem;
}

@media screen and (width <= 48rem){ 
  .desktop-img{
    display: none;
  }

  .mobile-img{
    display: block;
    width: 100%;
  }
}
/*Home Comp Styling End*/
/* Bright Future Styling Start */

img {
    display: block;
    max-width: 100%;
}

.box-img {
    width: 40%;
}

.box {
    display: flex;
    margin-block: 2rem;
}

.textBox {
    padding-left: 1rem;
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
    padding: 2rem 2rem 1rem 2rem;
}

.titleNewComp {
    color: var(--softOrange);
    margin: 0;
}

.boxNewComp {
    padding-block: 1rem;
}

.offWhiteNewComp {
    color: var(--offWhite);
}

/*New Comp Styling End*/


</style>