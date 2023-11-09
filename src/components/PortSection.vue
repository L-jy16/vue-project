<script setup>
import { portText } from "@/constants/index"
</script>
<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                portfolio <em>포폴 작업물</em>
            </div>
            <div class="port__wrap">
                <div v-for="(port, key) in portText" :key="key" :class="'port__item p' + (key + 1)">
                    <span class="num">{{ port.num }}.</span>
                    <a :href="port.view">
                        <img :src="port.img" :alt="port.title">
                    </a>
                    <h3 class="title">{{ port.title }}</h3>
                    <p class="desc">
                        {{ port.desc }}
                    </p>
                </div>

            </div>
        </div>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger"
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top 56px",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    // markers: true,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>

<style lang="scss">
#port {
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__title {
    position: sticky;
    left: 0;
    top: 70px;
    height: 5vw;
    background-color: var(--mainBg-color);
    width: 100%;
    height: 7vw;
    font-size: 5vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mainTit-font);
    border-bottom: 0.4vw solid var(--subBg400);
    color: var(--subBg400);
    margin-bottom: 4vh;
}

.port__title em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 500;
    display: inline-block;
    vertical-align: 4px;
}

.port__item {
    margin-top: 40px;
    width: 500px;
    height: 70vh;
    margin-right: 25px;
    padding: 25px;
    box-sizing: border-box;
    background-color: #fff;
    background-color: var(--subcolor400);
}

.port__item:nth-child(even) {
    background-color: var(--subcolor3_500);
}

.port__item .num {
    display: inline;
    font-size: 3vw;
    font-weight: 900;
    font-family: var(--mainNum-font);
    color: var(--subcolor2_600);
}

.port__item a img {
    border-radius: 15px;
    margin-top: -20px;
    filter: saturate(0);
    transition: all 0.3s;
}

.port__item a img:hover {
    margin-top: 0;
    filter: saturate(100%);
}

.port__item h3 {
    text-align: center;
    padding: 1.2rem;
    border-bottom: 2px dashed;
    font-weight: bolder;
    color: var(--subcolor2_500);
    font-size: 1.8rem;
    margin-bottom: 1rem;
    font-family: var(--mainTit-font);
}

.port__item .desc {
    text-align: center;
    font-size: 1.2rem;
    color: var(--subcolor2_500);
    font-family: var(--mainTit-font);
}
</style>
