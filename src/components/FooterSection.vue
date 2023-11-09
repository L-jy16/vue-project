<script setup>
import { footerText } from "@/constants/index";
</script>
<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>Lee Jiyoung</div>
                <div>@L-jy16</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li v-for="(foot, key) in footerText" :key="key">
                            <a :href="foot.link">{{ foot.title }}</a>
                            <em>{{ foot.desc }}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 LeeJiyoung<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
#footer {
    width: 100%;
}

.footer__inner {
    padding: 16px;
}

.footer__text {
    display: flex;
    width: 100%;
    padding: 1vw 0.5vw;
    color: var(--mainfont-color);
    border-bottom: 3px solid var(--mainfont-color);
    justify-content: space-between;
    align-items: end;
    font-family: var(--mainEng-font);
}

.footer__text div:nth-child(1) {
    font-weight: bold;
    font-size: 3vw;
    margin-right: 5px;
}

.footer__text div:nth-child(2) {
    font-size: 1.5vw;
}

.footer__info {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    /* margin-top: 2vw; */
    padding: 10px;
}

.footer__info .left {
    width: 48%;
}

.footer__info .left .title {
    padding-bottom: 10px;
    font-size: 2.2vw;
    text-transform: uppercase;
    font-family: var(--mainTit-font);
    color: var(--subcolor600);
    border-bottom: 2px solid var(--subcolor600);
}

.footer__info .left .title:hover {
    background-color: var(--subcolor2_200);
}

.footer__info .left .desc {
    padding: 10px 0;
    font-size: 1vw;
    font-family: var(--mainKor-font);
    color: var(--subcolor600);
}

.footer__info .right {
    width: 48%;
}

.footer__info .right h3 {
    padding-bottom: 10px;
    font-size: 2.2vw;
    text-transform: uppercase;
    font-family: var(--mainTit-font);
    color: var(--subcolor600);
    border-bottom: 2px solid var(--subcolor600);
}

.footer__info .right li {
    padding: 1vw;
    font-size: 1.5vw;
    width: 100%;
    border-bottom: 1px dashed var(--subcolor600);
}

.footer__info .right li:hover {
    background-color: var(--subcolor2_200);
    text-decoration: underline;
    text-underline-position: under;
}

.footer__info .right li:last-child {
    border: none;
}

.footer__info .right li a {
    font-weight: bold;
    color: var(--subcolor600);
}

.footer__info .right li em {
    display: none;
}

.footer__right {
    text-align: center;
    font-size: 1vw;
    color: var(--mainfont-color);
}
</style>
