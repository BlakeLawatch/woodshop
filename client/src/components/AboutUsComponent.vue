<template>
    <div class="bg">
        <section class="row">
            <div class=" col-12 col-md-6 mb-3">
                <h1 class="why-us mt-4 px-5 mb-4 text-center">About Us</h1>
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique rem ex dolorum
                    eveniet quidem!
                    Consequatur molestiae iure illo cumque quasi.</p>
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quisquam, in!</p>
                <p class="text-center">Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus incidunt
                    voluptas expedita eum non
                    nobis, reiciendis quod facere nostrum in.</p>
            </div>
            <div class="col-12 col-md-6 mb-3">
                <h1 class="why-us mt-4 px-5 mb-4 text-center">Contact Us</h1>
                <form method="post" action="https://formspree.io/f/xpzvrzdp">
                    <div class="d-flex ms-4">
                        <div class="mb-3 col-4">
                            <input v-model="editable.name" type="text" class="form-control" placeholder="Your Name"
                                name="name" id="name" minlength="4" maxlength="20" required>
                        </div>
                        <div class="mb-3 ms-5 col-5">
                            <input v-model="editable.email" type="email" class="form-control" placeholder="Your Email"
                                name="email" id="email" minlength="4" maxlength="40" required>
                        </div>
                    </div>
                    <div class="ms-4">
                        <div class="mb-3 col-10">
                            <input v-model="editable.subject" type="subject" class="form-control" placeholder="Subject"
                                name="subject" id="subject" minlength="4" maxlength="60" required>
                        </div>
                        <div class="mb-3 col-10">
                            <textarea v-model="editable.message" type="text" class="form-control" placeholder="Message..."
                                name="message" id="message" minlength="4" maxlength="400" rows="8" required></textarea>
                        </div>
                        <button type="submit" class="btn rounded-pill btn-outline-main">Send Message</button>
                    </div>
                </form>
            </div>

        </section>


    </div>
</template>


<script>
import { ref } from 'vue';
import Pop from '../utils/Pop';

export default {
    setup() {
        const editable = ref({})
        return {
            editable,
            async sendEmail() {
                try {
                    editable.value = {}
                    Pop.success('Email Sent!')
                } catch (error) {
                    Pop.error("email didn't work")
                }
            }

        }
    }
}
    ;
</script>


<style lang="scss" scoped>
.bg {
    background-color: #e4a960;
}

p {
    font-size: 15px;
    font-family: cursive;
}
</style>