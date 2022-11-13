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
                            <p class="product-header-description">Founded by a team of former investment managers, and
                                supported by experienced financial journalists, CTFN understands the questions on the minds
                                of investors and professionals who are impacted by critical activity in mergers and special
                                situations.</p>
                            <p class="product-header-description">Our market-leading reporting and our proprietary data
                                tools seek to address the questions and the information needs of investors and advisors
                                following the nuanced developments in mergers, dynamic industry sectors, and key special
                                situations.</p>
                            <p class="product-header-description mb-5">CTFN provides time-sensitive updates for better
                                decisions.</p>
                                <b-btn class="submitBtn" @click="showTrial = !showTrial">Request a Trial</b-btn>
                        </header>
                    </b-col>
                </b-row>
            </b-container>            
        </div>
        <div v-if="showTrial" id="trialForm" class="request-trial">
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
                            I agree to my personal data being sotred and used by CTFN for delivery of it's services. Please
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
</style>