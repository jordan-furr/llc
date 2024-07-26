<template>
    <div class="flex flex-col w-100 web-row">
        <div class="info-section">
            <div>
                <p id="logo">bad taste</p>
            </div>
            <div class="info borderbox">
                <p>bad taste is the web design & development practice of <a href="https://jordanfurr.com/" target="_">Jordan Furr</a>. bad taste is based in Brooklyn, NY.
                </p>
                <br>
                <span @click="copyEmail" style="cursor: pointer;">
                    <p class="email-label">jordan@jordanfurr.com</p>
                </span>
                <span v-if="copied" class="copied">copied!</span>
                <a href="" target="_">Instagram</a>
            </div>
        </div>
        <div class="featured">
            <p class="subtitle">SERVICES</p>
            <div class="service-list">
                <p>Vue/Nuxt</p>
                <p>Wordpress</p>
                <p>Shopify</p>
                <p>Figma</p>
                <p>Squarespace</p>
            </div>
        </div>
        <div class="featured">
            <p class="subtitle">FEATURED WORK</p>
            <div class="site-list">
                <a href="https://spintheupwheel.netlify.app/" target="_">Uncertainty Tool Dashboard</a>
                <a href="https://earnestproject.com/" target="_">Earnest Project</a>
                <a href="https://www.theupsideofuncertainty.com/" target="_">The Upside of Uncertainty</a>
                <a href="https://harmonpsychotherapy.com/" target="_">Harmon Psychotherapy & Consulting</a>
                <a href="https://centerforexpandingcompassion.org/" target="_">Center for Expanding Compassion</a>
                <a href="https://madewithharmony.com/" target="_">Made with Harmony</a>
                <a href="https://uncertaintyscience.com/" target="_">Uncertainty Science Initiative</a>
            </div>
            
        </div>
    </div>
</template>


<script>
export default {
    methods: {
        copyEmail() {
            const email = 'jordan@jordanfurr.com';
            navigator.clipboard.writeText(email)
                .then(() => {
                    this.copied = true;
                    setTimeout(() => {
                        this.copied = false;
                    }, 1500);
                })
                .catch(error => {
                    console.error('Failed to copy:', error);
                });
        }
    }
};
</script>