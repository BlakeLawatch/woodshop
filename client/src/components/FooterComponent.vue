<template>
    <div class="bg-card py-4 text-center">
        <div class="mb-5">
            <a class="socials" href="https://www.instagram.com/knottywoodshopllc/"><i
                    class="mdi mdi-instagram text-light"></i></a>

        </div>
        <div>
            <p class="text-light mb-0"><i class="mdi mdi-copyright"></i> COPYRIGHT <b> KNOTTY WOOD SHOP LLC</b>
                All
                rights
                reserved
            </p>

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
    font-size: 2rem;
    position: absolute;
}

.socials :hover {
    transition: .3s ease-in-out;
    // transform: scale(2);
    font-size: 2.5rem;
}
</style>