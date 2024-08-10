<template>
    <div class="flex flex-col w-100 web-row">
        <div class="logo-section">
            <div>
                <p id="logo">bad taste</p>
            </div>
            <div class="info borderbox">
                <p>web development for a variety of fields. bad taste agency by <a href="https://jordanfurr.com/" target="_">Jordan
                        Furr</a>. based in Brooklyn, New York.
                </p>
                <br>
                <span @click="copyEmail" style="cursor: pointer;">
                    <p class="email-label">jordan@jordanfurr.com</p>
                </span>
                <span v-if="copied" class="copied">copied!</span>
                <a href="" target="_">Instagram</a>
            </div>
        </div>
        <div class="info-col">
            <div class="info-section">
                <p class="subtitle">PROJECTS</p>
                <div class="site-list">
                    <div>
                        <a href="https://spintheupwheel.netlify.app/" target="_">UP Tool Dashboard</a>
                    </div>
                    <a href="https://earnestproject.com/" target="_">Earnest Project</a>
                    <a href="https://www.theupsideofuncertainty.com/" target="_">The Upside of Uncertainty</a>
                    <a href="https://harmonpsychotherapy.com/" target="_">Harmon Psychotherapy & Consulting</a>
                    <a href="https://centerforexpandingcompassion.org/" target="_">Center for Expanding Compassion</a>
                    <a href="https://madewithharmony.com/" target="_">Made with Harmony</a>
                    <a href="https://uncertaintyscience.com/" target="_">Uncertainty Science Initiative</a>
                </div>
            </div>
            <div class="info-section">
                <p class="subtitle">TECHNOLOGIES</p>
                <div class="service-list">
                    <p>Vue & Nuxt.js</p>
                    <p>Wordpress</p>
                    <p>Shopify</p>
                    <p>Figma</p>
                    <p>Squarespace</p>
                </div>
            </div>
        </div>
        <div class="info-col">
            <div class="info-section">
                <p class="subtitle">INFLUENCE</p>
                <div class="influencer">
                    <p class="influence">Diana Vreeland</p>
                    <p>"We all need a splash of bad taste—it’s hearty, it’s healthy, it’s physical. I think we could use
                        more of it. No taste is what I’m against."</p>
                    <br>
                    <p><em>[Interviewer]: Is there someone who personifies your idea of a great sense of
                            style?</em></p>
                    <br>
                    <p>"When you see a racehorse being led out. I think the've got something, hmmm, that no one else has. A
                        racehorse has a little extra pizazz."</p>
                    <!---
                    <br>
                    <p class="influence">Frequencies</p>
                    <p>Invention</p>
                    <p>Humanity</p>
                    <p>Freshness</p>
                    <p>Discernment</p>
                    <p>Beauty</p>
                    --->
                </div>
                <!---
                <div class="influencer">
                    <p class="influence">Diana Vreeland</p>
                    <p>"We all need a splash of bad taste—it’s hearty, it’s healthy, it’s physical. I think we could use
                        more of it. No taste is what I’m against."</p>
                    
                </div>
                --->
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