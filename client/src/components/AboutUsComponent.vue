<template>
    <div class="bg">
        <div class="d-flex justify-content-around">
            <h1 class="why-us mt-4 px-5 mb-4">About Us</h1>
            <h1 class="why-us mt-4 px-5 mb-4">Contact Us</h1>

        </div>

        <div class="col-12 d-flex justify-content-center">
            <div class="col-12 col-md-6 split">
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique rem ex dolorum
                    eveniet quidem!
                    Consequatur molestiae iure illo cumque quasi.</p>
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, in!</p>
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus incidunt
                    voluptas expedita eum non
                    nobis, reiciendis quod facere nostrum in.</p>
            </div>
            <div class="col-12 col-md-6">

            </div>
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
.bg {
    background-color: #e4a960;
}

p {
    font-size: 15px;
    font-family: cursive;
}

.split {
    border-right: thin solid #361112c7;
}
</style>