<script setup>

</script>

<template>
    <div class="header__catalog">
            <div class="header__catalog-menu ">
            <div class="header__catalog-menu-side">
                <ul class="header__catalog-menu-list">
                <li class="header__catalog-menu-list-item " v-for="_ in 10">
                    <NuxtImg src="https://s3-alpha-sig.figma.com/img/dd0a/2591/8d22c237f9fbe72d5f285936427f8a90?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=psHHXlNFJfO2n6~KXNgozs7CYsns3SlH9vRIvpP5x9Z-~0GBSYEVJbG2~ArcbYhfzGohTVbdMRf8Ch9avrK-oYnXQl4wNWLqR9thXLgrKJRMsaU7DSmx12mOzFmIUmijy7V-mLod~88WU4779jk49k0rcDbWbDGfq7NsT2bZokLpPN0N2adC3-b8P3bZLa~6ELU~Qj7WgMYa-ohDPIzyNQniNGz8DlhMuVu~8Hn5lqVFrOeXQcyXpoM222uKh6wtIKQf7qsemEv40O-WnULUwQGnot73G~BS5MmLxW4UGRt4teN5WY69HiVTzAcrEYOpbK-ptec-eO0l2H~i2Ndkmw__"></NuxtImg>
                    <span>DIN 2353</span>
                </li>
                <li class="header__catalog-menu-list-item active ">
                    <NuxtImg src="https://s3-alpha-sig.figma.com/img/dd0a/2591/8d22c237f9fbe72d5f285936427f8a90?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=psHHXlNFJfO2n6~KXNgozs7CYsns3SlH9vRIvpP5x9Z-~0GBSYEVJbG2~ArcbYhfzGohTVbdMRf8Ch9avrK-oYnXQl4wNWLqR9thXLgrKJRMsaU7DSmx12mOzFmIUmijy7V-mLod~88WU4779jk49k0rcDbWbDGfq7NsT2bZokLpPN0N2adC3-b8P3bZLa~6ELU~Qj7WgMYa-ohDPIzyNQniNGz8DlhMuVu~8Hn5lqVFrOeXQcyXpoM222uKh6wtIKQf7qsemEv40O-WnULUwQGnot73G~BS5MmLxW4UGRt4teN5WY69HiVTzAcrEYOpbK-ptec-eO0l2H~i2Ndkmw__"></NuxtImg>
                    <span>DIN 2353</span>
                </li>
            </ul>
            <ul class="header__catalog-menu-list">
                <li class="header__catalog-menu-list-item" v-for="_ in 2">
                    <NuxtImg src="https://s3-alpha-sig.figma.com/img/f0dd/a76d/adccf4a4992131ae0481b22ae469f914?Expires=1731283200&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4&Signature=kqYaP2CZcty3vPb0rNXBIVgJ0UPYDWLSNpPwb84PstODxMs3z4ZXW4~hITUIrCfIaVT3LmGq7TR3hEA0Gk8hitEu2anlZsPrSmzTSxu54Y9plXEMKsqFkriqxnEymVpXmPUMx2Z~RKiD5dCK7QI9N6N~QdCwV1OgjQB6CWV~qvVMHYxzz~a8ymaf89sQbhIwnxCVrs4OmZF5jR~XxgGOb0QJhYpev1tNNWfz7gy-YvbBU4Hmajxmq-3TcRCPkIyUOa1ppxKs3n255iizB9VwFj~mNmaUJ1oYR8mMc-OVsq75K7AWb68CaTsf2u9sh03NW7ijAnFg2ZR3PDqvOo7HFA__"></NuxtImg>
                    <span>Игольчатые клапаны</span>
                </li>
            </ul>
            </div>

        </div>
        <div class="header__catalog-overlay">
        </div>
    </div>
</template>


<style lang="scss" scoped>
.header__catalog {
    color: black;
    position: relative;
    width: 100%;
    height: 100%;

    &-menu {
        position: absolute;
        z-index: 10006;

        &-side {
            display: flex;
        }

        &-list {
            padding: 20px;
            align-items: center;
            background-color: white;
            height: max-content;

            &-item {
                display: flex;
                padding: 10px 211px 10px 10px;
                align-items: center;
                gap: 20px;
                border-bottom: 1px solid #d9d9d9;
                cursor: pointer;
                transition: 0.3s;

                &.active {  // изменено на &.active для применения к li
                    background: #3064C7;
                    
                    & span {
                        color: white;
                    }
                }

                &:hover {
                    background: #3064C7;

                    & span {
                        color: white;
                    }
                }
            }

            & img {
                max-width: 60px;
                height: auto;
            }

            & span {
                color: #000;
                font-family: "Myriad Pro";
                font-size: 18px;
                font-style: normal;
                font-weight: 600;
                line-height: 90%; /* 16.2px */
            }
        }
    }

    &-overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: #00000060;
        z-index: 10004;
    }
}

@media screen and (max-width: 1199.99px) {
    .header__catalog-menu-list-item {
        padding: 10px 130px 10px 10px;
    }
}
@media screen and (max-width: 767.99px) {
    .header__catalog {
        display: none;
    }
}
</style>