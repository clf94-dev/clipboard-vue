<template>
<b-container fluid class="features-section">
    <h2 data-aos="fade-right" data-aos-delay="100">Supercharge your workflow</h2>
    <p data-aos="fade-right" data-aos-delay="100">We’ve got the tools to boost your productivity.</p>
    <b-row class="row-feat">
        <b-col xs="12" sm="4" md="4" lg="4" v-for="feat of features" v-bind:key="feat.title">
            <b-col data-aos="fade-up" v-bind:data-aos-delay="feat.delay">
                <img :src="feat.src" :alt="feat.imgAlt">

                <h4>{{feat.title}}</h4>
                <p>{{feat.text}}</p>
            </b-col>
        </b-col>

    </b-row>
</b-container>
</template>

<script>
export default {
    name: 'Features',
    data() {
        return {
            features: [{
                    title: 'Create blacklists',
                    text: 'Ensure sensitive information never makes its way to your clipboard by excluding certain sources.',
                    src: require("@/assets/images/icon-blacklist.svg"),
                    imgAlt: 'Create blacklists',
                    delay: 100
                },
                {
                    title: 'Plain text snippets',
                    text: 'Remove unwanted formatting from copied text for a consistent look.',
                    src: require("@/assets/images/icon-text.svg"),
                    imgAlt: 'Plain text snippets',
                    delay: 300
                },
                {
                    title: 'Sneak preview',
                    text: 'Quick preview of all snippets on your Clipboard for easy access.',
                    src: require("@/assets/images/icon-preview.svg"),
                    imgAlt: 'Sneak preview',
                    delay: 500
                }

            ]
        }
    }
}
</script>

<style>
.features-section {
    text-align: center;
    padding: 5% 7%;
}

.features-section h2 {
    font-size: 30px;
}

img {
    margin-bottom: 20px;
}

.features-section p {
    font-size: 16px;
    color: #9fabb2;
    margin-bottom: 60px;
}

.features-section .row-feat h4 {
    font-size: 20px;
}

.features-section .row-feat p {
    font-size: 16px;
    color: #9fabb2;
    padding: 0 15%;
    margin-bottom: 60px;
}
</style>
