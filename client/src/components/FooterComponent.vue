<template>
    <div class="bg-card py-4 text-center">
        <div>
            <p class="text-light mb-0"><i class="mdi mdi-copyright"></i> COPYRIGHT <b> KNOTTY WOOD SHOP LLC</b>
                All
                rights
                reserved
            </p>

        </div>
        <div>
            <a class="socials" href="https://www.instagram.com/knottywoodshopllc/"><i
                    class="mdi mdi-instagram text-light"></i></a>

        </div>



    </div>
</template>


<script>
export default {
    setup() {
        return {}
    }
};
</script>


<style lang="scss" scoped>
.socials {
    text-decoration: none;
    max-height: 10vh;
    max-width: 10vw;
}

.socials :hover {
    transform: scale(2);
    transition: 2s ease-in-out;
    // font-size: 2rem;
    // position: fixed;
    // z-index: 999;
}
</style>