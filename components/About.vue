<template>
    <section id="about" class="about scroll-mt">
        <div class="visual-top-right">
            <b-img src="../assets/images/top-right.png" alt="Top right"></b-img>
        </div>
        <div class="visual-bottom-left">
            <b-img src="../assets/images/bottom-left.png" alt="Bottom left"></b-img>
        </div>
        <div class="about-content">
            <b-container>
                <b-row>
                    <b-col md="3">
                        <b-img class="bounce d-none d-md-block" src="../assets/images/left.png" alt="Advertisement" fluid></b-img>
                    </b-col>
                    <b-col md="9">
                        <header>
                            <h1>About Us</h1>
                            <p class="product-header-description">CTFN is a market-leading news and data resource for investors and professionals who are serious about following merger-related developments and understanding events that could influence industrial dynamics — including changes in regulatory enforcement across North America, Europe, and the UK.</p>
                            <p class="product-header-description">Our proprietary platform provides financial news, data, and resources for investors, legal and corporate professionals, regulators, and academics seeking granular knowledge around corporate mergers and notable events, potential impacts from changes in regulatory agencies, and insight into the political environment surrounding these situations. To learn more about CTFN, please schedule a complimentary platform overview.</p>
                                <b-btn id="trial" href="/#trialForm" class="mt-5 submitBtn scroll-trial" @click="showTrial = !showTrial">Request a Trial</b-btn>
                        </header>
                    </b-col>
                </b-row>
            </b-container>            
        </div>
        <div v-if="showTrial" id="trialForm" class="request-trial scroll-padding">
            <b-container>
                <header class="text-center">
                    <p class="request-trial-subTitle">Complete the form below and one of our representatives will be in
                        touch with you.</p>
                </header>
                <b-row class="justify-content-center align-items-center pt-4">
                    <b-col lg="10">
                        <b-form>
                            <b-form-input class="mb-3" id="input-default" placeholder="First Name"></b-form-input>
                            <b-form-input class="mb-3" id="input-default" placeholder="Last Name"></b-form-input>
                            <b-form-input class="mb-3" id="input-default" placeholder="Phone Number"></b-form-input>
                            <b-form-input class="mb-3" id="input-default" placeholder="Email Address"></b-form-input>
                            <b-form-input class="mb-3" id="input-default" placeholder="Company/Organization"></b-form-input>
                        </b-form>
                        <b-form-checkbox id="checkbox-1" name="checkbox-1" value="accepted" unchecked-value="not_accepted">
                            I agree to my personal data being stored and used by CTFN for delivery of it's services. Please
                            see <a href="/privacy-policy" style="color:blue">privacy</a> and <a href="/terms"
                                style="color:blue">terms &amp; conditions.</a>
                        </b-form-checkbox>
                        <div class="text-left mt-4">
                            <b-btn class="trialBtn">Submit</b-btn>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </div>        
    </section>
</template>

<script>

export default {
    name: "About",
    data() {
        return {
            showTrial: false
        }
    }
}

</script>

<style>
@import "../assets/styles/about.css";
@import "../assets/styles/trial-form.css";

.scroll-trial {
    scroll-margin-top: 120px;
}
.scroll-padding {
    scroll-margin-top: 240px;
}

</style>