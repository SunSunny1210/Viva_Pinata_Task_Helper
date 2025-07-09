<script setup>
</script>

<template>
    <nav>
        <div class="blur"></div>
        <div class="nav-info">
            <button>Let's Start! <span>&#9660;</span></button>
            <div class="links">
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
</style>