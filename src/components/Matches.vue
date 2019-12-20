<template>
    <div class="c-match">
        <div class="c-match__header">
            <div>14:55</div>
            <div>EPICENTER 2019</div>
        </div>
        <div class="c-match__content">
            <div class="c-match__team c-match__team_first">
                <div class="c-match__team-name">{{ match.team1.name }}</div>
                <img class="c-match__team-logo" :src="match.team1.logo" @click="openImage($event)">
            </div>
            <div class="c-match__score">{{ match.team1.score }} : {{ match.team2.score }}</div>
            <div class="c-match__team c-match__team_second">
                <div class="c-match__team-name">{{ match.team2.name }}</div>
                <img class="c-match__team-logo" v-bind:src="match.team2.logo">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Matches",
        props: {
            match: Object
        },
        data () {
            return {

            }
        },
        methods: {
            openImage(event) {
                console.log(event.target);
            }
        }
    };
</script>

<style scoped>
    * {
        box-sizing: border-box;
    }

    .c-match {
        background-color: #232d38;
        border-radius: 6px;
        color: #b9bdbf;
        display: flex;
        flex-direction: column;
        width: 100%;
        padding: 10px;
        font-size: 14px;
    }

    .c-match__header {
        display: flex;
        justify-content: space-between;
        font-weight: 800;
    }

    .c-match__content {
        display: flex;
        align-items: center;
        justify-content: center;
        min-height: 80px;
    }

    .c-match__team {
        display: flex;
        align-items: center;
        width: 100%;
        font-size: 18px;
        font-weight: 800;
    }

    .c-match__team_first {
        padding-right: 35px;
        justify-content: flex-end;
    }

    .c-match__team_second {
        padding-left: 35px;
        justify-content: flex-start;
    }

    .c-match__team-logo {
        width: 48px;
        height: 48px;
    }

    .c-match__team_first > .c-match__team-logo {
        margin-left: 8px;
    }

    .c-match__team_second > .c-match__team-logo {
        margin-right: 8px;
        order: 0;
    }

    .c-match__team_second > .c-match__team-name {
        order: 1;
    }

    .c-match__score {
        position: absolute;
        margin: 0 auto;
        width: 70px;
        font-size: 22px;
        font-weight: 900;
    }
</style>