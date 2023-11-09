<script setup>
import { skillText } from "@/constants/index";
</script>

<template>
    <section id="skill">
        <div class="skill__inner">
            <h2 class="skill__tiltle">
                challenge <em>나의 도전</em>
            </h2>
            <div class="skill__desc">
                <div v-for="(skill, key) in skillText" :key="key">
                    <span>{{ key + 1 }}.</span>
                    <h3>{{ skill.title }}</h3>
                    <p>{{ skill.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;
}

.skill__tiltle {
    position: sticky;
    top: 70px;
    left: 0;
    width: 50%;
    height: 7vw;
    font-size: 5vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mainTit-font);
    border-bottom: 0.4vw solid var(--subBg400);
    color: var(--subBg400);
}

.skill__tiltle em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 500;
    display: inline-block;
    vertical-align: 4px;
}

.skill__desc {
    width: 48%;
}

.skill__desc span {
    font-weight: 700;
    font-size: 5rem;
    color: var(--subBg400);
    margin-bottom: 2vw;
    font-family: var(--mainNum-font);
}

.skill__desc h3 {
    font-size: 2rem, ;
    line-height: 1;
    margin-bottom: 2vw;
    color: var(--subBg400);
    font-weight: 800;
    text-decoration: underline;
    text-underline-position: under;
}

.skill__desc p {
    font-size: 1.2rem;
    font-weight: normal;
    color: var(--subBg400);
    margin-bottom: 30vh;
}

@media (max-width: 800px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__tiltle {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        background-color: var(--mainBg-color);
        font-size: 9vw;
    }

    .skill__desc {
        width: 100%;
    }

    .skill__desc span {
        font-size: 15vw;
    }

    .skill__desc h3 {
        font-size: 5vw;
    }

    .skill__desc p {
        font-size: 4vw;
    }
}
</style>
