<script setup>
import { contactText } from "@/constants/index"
</script>
<template>
    <section id="contact">
        <div class="contact__inner">
            <h2 class="contact__title">Contact</h2>

            <div class="contact__line" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
            <div class="contact__text">
                <div class="text">
                    <div v-for="(cont, key) in contactText" :key="key">
                        <a :href="cont.link"><em>{{ cont.title[0] }}</em> : {{ cont.title[1] }}</a>
                    </div>
                </div>
            </div>
            <div class="contact__line bottom" aria-hidden="true">
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
                <span class="line"></span>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
#contact {
    height: 100vh;
}

.contact__inner {
    padding: 16px;
}

.contact__title {
    font-family: var(--mainEng-font);
    font-size: 7.8vw;
    text-transform: uppercase;
    font-weight: bold;
    color: var(--mainfont-color);

}

.contact__line {
    display: block;
    width: 100%;
}

.contact__line .line {
    display: block;
    width: 100%;
    height: 1px;
    background-color: var(--subBg300);
    margin-bottom: 0.5vw;
}

.contact__line .line:nth-child(1) {
    height: 1px;
}

.contact__line .line:nth-child(2) {
    height: 2px;
}

.contact__line .line:nth-child(3) {
    height: 3px;
}

.contact__line .line:nth-child(4) {
    height: 4px;
}

.contact__line .line:nth-child(5) {
    height: 5px;
}

.contact__line .line:nth-child(6) {
    height: 6px;
}

.contact__line .line:nth-child(7) {
    height: 7px;
}

.contact__line.bottom {
    display: block;
    width: 100%;
}

.contact__line.bottom .line:nth-child(1) {
    height: 7px;
}

.contact__line.bottom .line:nth-child(2) {
    height: 6px;
}

.contact__line.bottom .line:nth-child(3) {
    height: 5px;
}

.contact__line.bottom .line:nth-child(4) {
    height: 4px;
}

.contact__line.bottom .line:nth-child(5) {
    height: 3px;
}

.contact__line.bottom .line:nth-child(6) {
    height: 2px;
}

.contact__line.bottom .line:nth-child(7) {
    height: 1px;
}

.contact__text {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 50vh;
    background-color: var(--subcolor400);
    text-align: center;
    color: var(--subcolor2_000);
    font-size: 3vw;
    line-height: 1.6;

}

.contact__text em {
    font-weight: bold;
}

.contact__text a {
    transition: all 0.3s;
}

.contact__text a:hover {
    text-decoration: underline;
    font-size: 3.1vw;
}
</style>
