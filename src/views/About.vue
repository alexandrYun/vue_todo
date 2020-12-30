<template>
    <div class="about">
        <h1 class="about__title">
            О проекте
        </h1>
        <p class="about__text">
            Привет, меня зовут Александр и я начинающий frontend разработчик.
            Я пишу на JS и Vue.js, примеры моих проектов можно найти на моём <a href="https://github.com/alexandrYun" target="_blank">GitHub</a>.
            Данный проект написан с использованием Vue.js и Vuetify. Также здесь использован роутинг для переходя по страницам.
            На странице <router-link to="/todo" class="nav-link">TODO</router-link> представлен основной фунционал: можно создавать список дел, задавать им приоритет и дедлайн, неактуальные задачи можно удалить.
        </p>
    </div>
</template>

<style>
    .about {
        /* text-align: center; */
        font-family: 'Montserrat Alternates', sans-serif;
        width: 50%;
        margin: 20px auto;
        color: #272727;
    }

    .about__title {
        border-bottom: 1px solid rgba(39, 39, 39, 0.3);
        display: inline-block;
    }

    .about__text {
        margin-top: 20px;
        line-height: 25px;
        letter-spacing: 1px;
        border: 1px solid rgba(39, 39, 39, 0.3);
        padding: 10px;
        font-size: 18px;
    }

    .home-link {
        color: #272727;
    }

    .home-link:hover {
        text-shadow: 0 1px 1px rgba(0, 0, 0, 0.5);
    }
</style>