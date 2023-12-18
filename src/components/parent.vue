<script setup>
import {ref, onMounted} from "vue";

const daily = ref(true);
const monthly = ref(false);
const weekly = ref(false);
const arr = [daily, monthly, weekly];
onMounted(() => {
    let $btns = document.querySelectorAll(".bottom > ul > li > button");
    $btns.forEach(($btn) => {
        $btn.addEventListener("click", (e) => {
            $btns.forEach((el) => el.classList.remove("active"));
            $btn.classList.add("active");
        });
    });
    $btns[0].addEventListener("click", (e) => {
        arr.forEach((state) => (state.value = false));
        daily.value = true;
    });
    $btns[1].addEventListener("click", (e) => {
        arr.forEach((state) => (state.value = false));
        monthly.value = true;
    });
    $btns[2].addEventListener("click", (e) => {
        arr.forEach((state) => (state.value = false));
        weekly.value = true;
    });
});
</script>
<template>
    <section>
        <div class="container">
            <div class="left">
                <div class="top">
                    <div class="image">
                        <img
                            src="../assets/images/image-jeremy.png"
                            alt="jeremy"
                        />
                    </div>
                    <span> <span> Report for </span> Jeremy Robson</span>
                </div>
                <div class="bottom">
                    <ul role="list">
                        <li role="listitem">
                            <button
                                role="button"
                                aria-label="change-time"
                                class="active"
                            >
                                Daily
                            </button>
                        </li>
                        <li role="listitem">
                            <button role="button" aria-label="change-time">
                                weekly
                            </button>
                        </li>
                        <li role="listitem">
                            <button role="button" aria-label="change-time">
                                monthly
                            </button>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="right">
                <div>
                    <div class="header">
                        <span class="task">work</span>
                        <span class="icon"
                            ><svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                /></svg
                        ></span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">5hrs</span>
                        <span class="history">last weak - 7hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">32hrs</span>
                        <span class="history">last weak - 36hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">103hrs</span>
                        <span class="history">last weak - 128hrs</span>
                    </footer>
                </div>
                <div>
                    <div class="header">
                        <span class="task">play</span>
                        <span class="icon">
                            <svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                />
                            </svg>
                        </span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">1hrs</span>
                        <span class="history">last weak - 2hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">10hrs</span>
                        <span class="history">last weak - 8hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">23hrs</span>
                        <span class="history">last weak - 29hrs</span>
                    </footer>
                </div>
                <div>
                    <div class="header">
                        <span class="task">study</span>
                        <span class="icon">
                            <svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                />
                            </svg>
                        </span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">0hrs</span>
                        <span class="history">last weak - 1hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">4hrs</span>
                        <span class="history">last weak - 7hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">13hrs</span>
                        <span class="history">last weak - 19hrs</span>
                    </footer>
                </div>
                <div>
                    <div class="header">
                        <span class="task">exercise</span>
                        <span class="icon">
                            <svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                />
                            </svg>
                        </span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">1hrs</span>
                        <span class="history">last weak - 1hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">4hrs</span>
                        <span class="history">last weak - 5hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">11hrs</span>
                        <span class="history">last weak - 18hrs</span>
                    </footer>
                </div>
                <div>
                    <div class="header">
                        <span class="task">social</span>
                        <span class="icon">
                            <svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                />
                            </svg>
                        </span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">1hrs</span>
                        <span class="history">last weak - 3hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">5hrs</span>
                        <span class="history">last weak - 10hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">21hrs</span>
                        <span class="history">last weak - 23hrs</span>
                    </footer>
                </div>
                <div>
                    <div class="header">
                        <span class="task">self care</span>
                        <span class="icon">
                            <svg
                                width="21"
                                height="5"
                                xmlns="http://www.w3.org/2000/svg"
                            >
                                <path
                                    d="M2.5 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Zm8 0a2.5 2.5 0 1 1 0 5 2.5 2.5 0 0 1 0-5Z"
                                    fill="#BBC0FF"
                                    fill-rule="evenodd"
                                />
                            </svg>
                        </span>
                    </div>
                    <footer v-if="daily">
                        <span class="time">0hrs</span>
                        <span class="history">last weak - 1hrs</span>
                    </footer>
                    <footer v-if="weekly">
                        <span class="time">2hrs</span>
                        <span class="history">last weak - 2hrs</span>
                    </footer>
                    <footer v-if="monthly">
                        <span class="time">7hrs</span>
                        <span class="history">last weak - 11hrs</span>
                    </footer>
                </div>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
.container {
    display: flex;
    flex-direction: column;
    @media (min-width: 768px) {
        flex-direction: row;
    }
    gap: 50px;
    @media (min-width: 768px) {
        gap: 20px;
    }
    --padding: 30px;
    .left {
        @media (min-width: 768px) {
            flex-basis: 250px;
        }
        > div {
            border-radius: var(--main-rounded);
        }
        .top {
            padding: var(--padding) var(--padding) 5px;
            background-color: var(--Primary-Blue);
            position: relative;
            transform: translateY(10px);
            display: flex;
            column-gap: 20px;
            @media (min-width: 768px) {
                display: block;
                padding: var(--padding) var(--padding) 118px;
            }
            .image {
                width: 70px;
                margin-bottom: 20px;
                img {
                    width: 100%;
                    border: 3px solid white;
                    border-radius: 50%;
                }
            }
            > span {
                color: #fff;
                font-weight: 300;
                font-size: 20px;
                @media (min-width: 768px) {
                    font-size: 38px;
                }
                span {
                    font-size: 16px;
                    color: var(--Neutral-PaleBlue);
                    display: block;
                    margin-top: 10px;
                    @media (min-width: 768px) {
                        margin-top: 0px;
                    }
                }
            }
        }
        .bottom {
            background-color: var(--Neutral-Darkblue);
            border-top-right-radius: 0px;
            border-top-left-radius: 0px;

            @media (min-width: 768px) {
                padding: var(--padding);
            }

            ul {
                display: flex;
                justify-content: space-evenly;
                > li {
                    width: calc(100% / 3);
                    padding: 10px 0px;
                    text-align: center;
                }
                @media (min-width: 768px) {
                    display: block;
                    > li {
                        padding: 0;
                        text-align: left;
                    }
                }
                li {
                    button {
                        background: none;
                        border: none;
                        cursor: pointer;
                        padding: 8px 0px;
                        font-size: 18px;
                        color: var(--Neutral-Desaturatedblue);
                        transition: 0.4s;
                        text-transform: capitalize;
                        &:hover {
                            color: #fff;
                        }
                        &.active {
                            color: #fff;
                        }
                    }
                }
            }
        }
    }
    .right {
        flex: 1;
        display: grid;
        grid-template-columns: 1fr;
        @media (min-width: 576px) {
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
        }
        gap: 50px calc(var(--main-gap) + 15px);
        @media (min-width: 768px) {
            gap: calc(var(--main-gap) + 90px) calc(var(--main-gap) + 15px);
        }
        > div {
            position: relative;
            z-index: 5;
            padding: var(--padding);
            padding-top: 50px;
            background-color: var(--Neutral-Darkblue);
            border-radius: var(--main-rounded);
            &:hover {
                background-color: #34397b;
            }

            @media (min-width: 768px) {
                &:nth-child(1),
                &:nth-child(2),
                &:nth-child(3) {
                    transform: translateY(45px);
                }
            }
            &::after {
                content: "";
                position: absolute;
                width: 100%;
                left: 0;
                height: 60px;
                top: -30px;
                z-index: 1;
                border-radius: var(--main-rounded);
                background-repeat: no-repeat;
                background-size: 70px 70px;
                background-position: 92%;
            }
            &:hover::before {
                background-color: #34397b;
            }
            &::before {
                content: "";
                position: absolute;
                width: 100%;
                background-color: var(--Neutral-Darkblue);
                z-index: 45;
                top: 17px;
                height: 20px;
                left: 0;
                border-radius: va;
                border-radius: var(--main-rounded);
            }
            &:nth-child(1) {
                &::after {
                    background-color: var(--Primary-lightOrange);
                    background-image: url(/src/assets/images/icon-work.svg);
                }
            }
            &:nth-child(2) {
                &::after {
                    background-color: var(--Primary-Softblue);
                    background-image: url("../assets/images/icon-play.svg");
                }
            }
            &:nth-child(2) {
                &::after {
                    background-color: var(--Primary-Softblue);
                    background-image: url("../assets/images/icon-play.svg");
                }
            }
            &:nth-child(3) {
                &::after {
                    background-color: var(--Primary-Lightred);
                    background-image: url("../assets/images/icon-study.svg");
                }
            }
            &:nth-child(4) {
                &::after {
                    background-color: var(--Primary-Limegreen);
                    background-image: url("../assets/images/icon-exercise.svg");
                }
            }
            &:nth-child(5) {
                &::after {
                    background-color: var(--Primary-Violetsocial);
                    background-image: url("../assets/images/icon-social.svg");
                }
            }
            &:nth-child(6) {
                &::after {
                    background-color: var(--Primary-Softorangeselfcare);
                    background-image: url("../assets/images/icon-self-care.svg");
                }
            }
        }
    }
    .right {
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            span {
                color: #fff;
                font-size: 18px;
                font-weight: 500;
                & + span {
                    cursor: pointer;
                }
            }
        }
        footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 20px;
            @media (min-width: 768px) {
                display: block;
            }
        }
        .time {
            display: block;

            color: #fff;
            font-size: 30px;
            font-weight: 300;
            @media (min-width: 768px) {
                font-size: 50px;
            }
        }
        .history {
            display: block;

            font-size: 14px;
            @media (min-width: 768px) {
                margin-top: 10px;
            }

            color: var(--Neutral-PaleBlue);
            text-transform: capitalize;
        }
    }
}
</style>
