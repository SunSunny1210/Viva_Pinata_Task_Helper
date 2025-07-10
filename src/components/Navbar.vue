<script setup>
import { ref } from 'vue';

const isOpen = ref(false);
const menuRef = ref(null);

const showMenu = () => {
    isOpen.value = !isOpen.value
}

const menuRefHeight = () => {
    if (menuRef.value) {
        return menuRef.value.scrollHeight;
    } else {
        return 0
    }
}
</script>

<template>
    <nav>
        <div class="blur"></div>
        <div class="nav-info">
            <button @click="showMenu">Let's Start! <span>&#9660;</span></button>
            <Transition name="show-menu">
                <div v-show="isOpen" class="login-menu">
                    <Transition name="show-links">
                        <div v-if="isOpen" class="a-links">
                            <RouterLink to="">&#9825; Log in</RouterLink>
                            <RouterLink to="">&#9825; Register</RouterLink>
                        </div>
                    </Transition>
                </div>
            </Transition>
            <div class="links" ref="menuRef">
                <RouterLink>Home</RouterLink>
                <RouterLink>Piñatas</RouterLink>
                <RouterLink>Villagers</RouterLink>
                <RouterLink>Plants</RouterLink>
                <RouterLink>Objects</RouterLink>
            </div>
            <img src="../assets/images/VivaPinataTIP.png" alt="Viva Piñata TP Logo">
        </div>
    </nav>
</template>

<style scoped>
 nav {
    position: fixed;
    height: 100px;
    width: 100%;
    background-color: transparent;

    .blur {
        position: fixed;
        height: 100px;
        width: 100%;
        background-color: transparent;
        backdrop-filter: blur(3px);
        z-index: -1;
    }

    .nav-info {
        padding: 0 2rem;
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;

        button {
            padding: 1rem;
            font-size: var(--p-normal-size);
            color: white;
            background-color: var(--dark-violet);
            border: none;
            border-radius: var(--radius);
        }

        button:hover {
            color: var(--dark-violet);
            background-color: white;
        }

        .login-menu {
            position: fixed;
            top: 50px;
            left: 33px;
            height: 9rem;
            width: 151px;
            font-size: var(--p-normal-size);
            color:  blueviolet;
            background-color: beige;
            z-index: -1;
            border-radius: 0 0 12px 12px;
            
            .a-links {
                margin-top: 2.5rem;
                display: flex;
                flex-direction: column;
                justify-content: flex-start;
                align-items: center;
                gap: 0.5rem;

                a {
                    padding: 0.5rem;
                    text-decoration: none;
                    border-radius: var(--radius);
                }
                
                a:hover {
                    color: beige;
                    background-color: blueviolet;
                }
            }
        }
        
        .links {
            display: flex;
            justify-content: space-evenly;
            align-items: center;
            gap: 5rem;

            a {
                padding: 1rem;
                color: blueviolet;
                background-color: var(--white-blur);
                text-decoration: none;
                border: 3px solid white;
                border-radius: var(--radius);
            }

            a:hover {
                color: white;
                background-color: blueviolet;
            }
        }

        img {
            height: 70px;
        }
    }
 }

 .show-menu-enter-active, .show-menu-leave-active {
    transition: max-height 0.2s ease;
 }

 .show-menu-enter-from, .show-menu-leave-to {
    max-height: 0;
 }

 .show-menu-enter-to, .show-menu-leave-from {
    max-height: 9rem;
 }

 .show-links-enter-active {
    transition: opacity 0.65s ease, transform 0.2s;
 }

 .show-links-leave-active {
    transition: opacity 0.1s ease, transform 0.2s;
 }

 .show-links-enter-from, .show-links-leave-to {
    opacity: 0;
    transform: translateY(-10px);
}

.show-links-enter-to, .show-links-leave-from {
    opacity: 1;
    transform: translateY(0);
 }
</style>