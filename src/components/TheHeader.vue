<template>
    <header class="header">
        <div class="header__burger">
            <burger-menu />
        </div>
        <div class="header__logo">
            <svg width="110" height="117" viewBox="0 0 110 117" fill="none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                <rect width="110" height="117" fill="url(#pattern0)"/>
                <defs>
                <pattern id="pattern0" patternContentUnits="objectBoundingBox" width="1" height="1">
                <use xlink:href="#image0" transform="scale(0.00909091 0.00854701)"/>
                </pattern>
                <image id="image0" width="110" height="117" xlink:href="data:image/png;base64,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"/>
                </defs>
            </svg>
            <svg width="322" height="20" viewBox="0 0 322 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path d="M136.6 19H127.1L108.6 6.1L105.6 18.9H97.3L101.5 1H111L129.5 14.1L132.5 1H140.8L136.6 19Z" fill="#DF1F26"/>
                <path d="M182.8 4.9H154.2C153.5 4.9 152.9 5 152.4 5.2C151.9 5.4 151.6 5.7 151.5 6L151.4 7C151.3 7.3 151.5 7.6 151.9 7.8C152.3 8 152.9 8.1 153.5 8.1H177.3C178.6 8.1 179.7 8.3 180.5 8.7C181.3 9.1 181.7 9.6 181.5 10.2L180 16.7C179.9 17.3 179.3 17.8 178.3 18.2C177.3 18.6 176.1 18.8 174.8 18.8H140.2L141.1 15H169.7C170.4 15 171 14.9 171.5 14.7C172 14.5 172.3 14.2 172.4 13.9L172.7 12.8C172.8 12.5 172.6 12.3 172.2 12C171.8 11.8 171.2 11.7 170.6 11.7H146.8C145.5 11.7 144.4 11.5 143.6 11.1C142.8 10.7 142.4 10.2 142.6 9.6L144.1 3.1C144.2 2.5 144.8 2 145.8 1.6C146.8 1.2 148 1 149.3 1H183.9L182.8 4.9Z" fill="#DF1F26"/>
                <path d="M261.6 8.10001L260.7 11.9H235.7L235.2 14.1C235.1 14.4 235.3 14.6 235.7 14.9C236.1 15.1 236.7 15.2 237.3 15.2H265.9L265 19H230.4C229.1 19 228 18.8 227.2 18.4C226.4 18 226 17.5 226.1 16.9L229.3 3.30001C229.4 2.70001 230 2.20001 231.1 1.80001C232.1 1.40001 233.3 1.20001 234.6 1.20001H269.2L268.3 5.00001H239.7C239 5.00001 238.4 5.10001 237.9 5.30001C237.4 5.50001 237.1 5.80001 237 6.10001L236.5 8.30001H261.6V8.10001Z" fill="#DF1F26"/>
                <path d="M50.6001 19H42.2001L44.5001 9.2L32.2001 19H29.6001L21.8001 9.2L19.5001 19H11.1001L15.2001 1H23.6001L32.3001 12.1L46.4001 1.1H54.8001L50.6001 19Z" fill="#DF1F26"/>
                <path d="M94.3001 16.8C94.2001 17.4 93.6001 17.9 92.6001 18.3C91.6001 18.7 90.4001 18.9 89.1001 18.9H59.2001C57.9001 18.9 56.8001 18.7 56.0001 18.3C55.2001 17.9 54.8001 17.4 54.9001 16.8L58.1001 3.20001C58.2001 2.60001 58.8001 2.10001 59.9001 1.70001C60.9001 1.30001 62.1001 1.10001 63.4001 1.10001H93.2001C94.6001 1.10001 95.6001 1.30001 96.5001 1.70001C97.3001 2.10001 97.7001 2.60001 97.5001 3.20001L94.3001 16.8ZM86.5001 14.1L88.4001 5.90001C88.5001 5.60001 88.3001 5.40001 87.9001 5.10001C87.5001 4.90001 86.9001 4.80001 86.3001 4.80001H68.4001C67.7001 4.80001 67.1001 4.90001 66.6001 5.10001C66.1001 5.30001 65.8001 5.60001 65.7001 5.90001L63.8001 14.1C63.7001 14.4 63.9001 14.6 64.3001 14.9C64.7001 15.1 65.3001 15.2 65.9001 15.2H83.8001C84.5001 15.2 85.1001 15.1 85.6001 14.9C86.2001 14.7 86.5001 14.4 86.5001 14.1Z" fill="#DF1F26"/>
                <path d="M207.2 19H198.9L201.9 5.9C202 5.6 201.8 5.4 201.4 5.1C201 4.9 200.4 4.8 199.8 4.8H186.7L187.6 1H227L226.1 4.8H213C212.3 4.8 211.7 4.9 211.2 5.1C210.7 5.3 210.4 5.6 210.3 5.9L207.2 19Z" fill="#DF1F26"/>
                <path d="M308.2 19H299.8L300.8 14.6C300.8 14.3 300.6 14.1 300.2 13.8C299.8 13.6 299.3 13.5 298.6 13.5H280.8C280.1 13.5 279.5 13.6 279 13.8C278.5 14 278.2 14.3 278.1 14.6L277 18.9H268.6L272.3 3.1C272.4 2.5 273 2 274 1.6C275 1.2 276.2 1 277.5 1H307.3C308.7 1 309.7 1.2 310.6 1.6C311.4 2 311.8 2.5 311.6 3.1L310.2 9.4C310.1 10 309.5 10.5 308.4 10.9C307.4 11.3 306.2 11.5 304.8 11.5C306.3 11.5 307.4 11.8 308.3 12.3C308.6 12.4 308.7 12.7 308.8 12.9C309 13.4 309.1 13.6 309.1 13.7L308.2 19ZM302.2 8.7L302.8 6C302.9 5.7 302.7 5.5 302.3 5.2C301.9 5 301.3 4.9 300.7 4.9H282.8C282.1 4.9 281.5 5 281 5.2C280.5 5.4 280.2 5.7 280.1 6L279.5 8.7C279.4 9 279.6 9.2 280 9.5C280.4 9.7 281 9.8 281.6 9.8H299.5C300.1 9.8 300.7 9.7 301.2 9.5C301.8 9.2 302.1 9 302.2 8.7Z" fill="#DF1F26"/>
            </svg>
        </div>
        <nav class="header__navigation">
            <ul class="header__navigation-list">
                <li><a href="#">NOT MY DESIGN</a></li>
                <li><a href="https://github.com/pylsar/myVueMoto" rel="nofollow" target="_blank">CODE HERE</a></li>
            </ul>
        </nav>
    </header>
</template>
<script>
import BurgerMenu from '@/components/BurgerMenu.vue';
    export default {
        name: 'TheHeader',
        components:{
            BurgerMenu
        } 
    }
</script>  
<style lang="scss">
    .header{
        width: 100%;
        height: 20vh;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        &__burger{
            width: 33%;
            padding-left: 20px;
        }
        &__logo{
            width: 33%;
            max-height: 20vh;
            padding-top: 10px;
            display: flex;
            flex-direction: column;
            align-items: center;
            & svg:first-child{
                padding-bottom: 10px;
            }
        }
        &__navigation{
            width: 33%;
            padding-right: 20px;
        }
        &__navigation-list{
            width: 100%;
            display: flex;
            justify-content: flex-end;
            & li{
                list-style: none;
                margin-left: 20px;
                position: relative;
                &:first-child{
                    margin-left: 0;
                    &::after{
                        content: '';
                        display: block;
                        background: #fff;
                        width: 2px;
                        height: 100%;
                        position: absolute;
                        top: 0;
                        right: -10px;
                    }
                }
                & a {
                    text-transform: uppercase;
                    text-decoration: none;
                    font-size: 14px;
                    color: #fff;
                }
            }
        }
    }
/***ADAPTIVE***/
    @media screen and (max-width: 960px) {
        .header{
            &__logo{
                & svg:first-child{
                    height: 80px;
                }
            }
            &__navigation-list{
                & li{
                    & a {
                        font-size: 12px;
                    }
                }
            }
        }
    }	
    @media screen and (max-width: 768px) {
        .header{
            &__navigation-list{
                flex-direction: column;
                align-items: flex-end;
                & li{
                    &:first-child{
                        &::after{
                            display: none;
                        }
                    }
                }
            }
        }
    }
    @media screen and (max-width: 450px) {
        .header{
            &__logo{
                position: absolute;
                left: 50%;
                transform: translate(-50%);
            }  
            &__logo{
                & svg{
                    &:last-child{
                        width: 200px;
                    }
                }
            } 
        }
    }
    @media screen and (max-width: 375px) {
        .header{
            &__navigation-list{
                & li{
                    & a {
                        font-size: 10px;
                    }
                }
            }
        }
    }
</style>