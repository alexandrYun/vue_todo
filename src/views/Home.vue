<template>
    <div class="home">
        <h1 class="home__title">
            TODO
        </h1>
        <div class="links-wrapper">
            <router-link to="/todo" class="nav-link"><v-btn class="home__btn">Начать работу с TODO</v-btn></router-link>
            <router-link to="/about" class="nav-link"><v-btn class="home__btn">About</v-btn></router-link>
        </div>
    </div>
</template>

<style>
    .home {
        text-align: center;
        font-family: 'Montserrat Alternates', sans-serif;
        width: 50%;
        margin: 100px auto;
        color: #272727;
    }

    .home__title {
        font-size: 140px;
        border-bottom: 1px solid rgba(39, 39, 39, 0.3);
        display: inline-block;
        margin-bottom: 25px;
    }

    .links-wrapper {
        display: flex;
        gap: 15px;
        justify-content: center;
    }
</style>