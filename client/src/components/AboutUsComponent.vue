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
                <form method="post" action="">
                    <div class="d-flex ms-4">
                        <div class="mb-3 col-4">
                            <input type="text" class="form-control" placeholder="Your Name" name="name" id="name"
                                minlength="4" maxlength="20" required>
                        </div>
                        <div class="mb-3 ms-4 col-5">
                            <input type="email" class="form-control" placeholder="Your Email" name="email" id="email"
                                minlength="4" maxlength="40" required>
                        </div>
                    </div>
                    <div class="ms-4">
                        <div class="mb-3 col-10">
                            <input type="subject" class="form-control" placeholder="Subject" name="subject" id="subject"
                                minlength="4" maxlength="60" required>
                        </div>
                        <div class="mb-3 col-10">
                            <textarea type="text" class="form-control" placeholder="Message..." name="message" id="message"
                                minlength="4" maxlength="400" rows="8" required></textarea>
                        </div>
                    </div>
                    <button class="btn rounded-pill btn-outline-success">Send Message</button>
                </form>
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