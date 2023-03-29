<template>
    <div class="user-card">
        <div class="user-card_left">
            <img src="/src/assets/user-card.svg" alt="user" class="user-card_left_photo">
            <div class="user-card_left_info">
                <p class="user-card_name">
                    Абрамова Екатерина
                    <svg width="13" height="27" viewBox="0 0 13 27" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M6.07502 5.39999C7.56675 5.39999 8.77505 4.19176 8.77505 2.69996C8.77499 1.20823 7.56675 0 6.07502 0C4.58323 0 3.375 1.20823 3.375 2.70003C3.375 4.19176 4.58323 5.39999 6.07502 5.39999Z"
                            fill="#FF93DA"/>
                        <path
                            d="M8.71428 8.59948C8.34978 7.4925 7.31703 6.74995 6.15601 6.74995H6.00078C4.83976 6.74995 3.80701 7.49243 3.44251 8.59948L0 18.9H4.05V27H8.10001V18.9H12.15L8.71428 8.59948Z"
                            fill="#FF93DA"/>
                    </svg>
                </p>
                <div class="jc-sb">
                    <div class="user-card_social">
                        <img src="/src/assets/whatsapp.svg" alt="wh">
                        <img src="/src/assets/viber.svg" alt="vb">
                        <img src="/src/assets/telegram.svg" alt="tg">
                        <a href="#" class="user-card_comment">Комментарии</a>
                    </div>
                    <div class="user-card_status">
                        <span class="status">Статус</span>
                        <p class="status_value success">Активен</p>
                    </div>
                </div>
            </div>
        </div>
        <div class="user-card_right"></div>
    </div>
</template>

<script>
export default {
    name: "UserCard"
}
</script>

<style lang="scss" scoped>
.user-card {
    width            : 100%;
    background-color : #ffffff;
    border           : 1px solid #000000;
    box-shadow       : 0 4px 5px rgba(0, 0, 0, 0.1);
    border-radius    : 10px;
    display          : flex;
    justify-content  : space-between;
    padding          : 20px 30px 20px 20px;

    &_left {
        width         : 50%;
        display       : flex;
        align-items   : center;
        padding-right : 40px;

        &_photo {
            width         : 112px;
            height        : 112px;
            margin-right  : 38px;
            border-radius : 50%;
        }

        &_info {
            display         : flex;
            flex-direction  : column;
            justify-content : space-between;
            height          : 100%;
            width           : 100%;
        }
    }

    &_name {
        font-size           : 38px;
        line-height         : 43px;
        font-weight         : 700;
        color               : #458afb;
        -webkit-text-stroke : 1px #000000;
        text-shadow         : 0 4px 4px rgba(0, 0, 0, 0.25);
        display             : flex;
        align-items         : center;

        svg {
            margin-left : 30px;
            min-width   : 13px;
        }
    }

    &_social {
        display     : flex;
        align-items : center;

        img {
            margin-right : 10px;
        }
    }

    &_comment {
        margin-left : 30px;
        color       : #458afb;
        font-size   : 18px;
        line-height : 22px;
        font-weight : 400;
    }

    &_status {
        .status {
            color       : #86939c;
            font-size   : 14px;
            line-height : 17px;

            &_value {
                color        : #0d2839;
                font-size    : 18px;
                line-height  : 22px;
                padding-left : 18px;
                position     : relative;

                &:after {
                    content          : "";
                    position         : absolute;
                    left             : 0;
                    top              : 50%;
                    transform        : translateY(-50%);
                    border-radius: 2px;
                    width            : 9px;
                    height           : 9px;
                    background-color : #9ecb45;
                }
            }
        }
    }
}
</style>