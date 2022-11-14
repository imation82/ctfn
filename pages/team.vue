<template>
    <section id="team" class="team">
        <b-container>
            <header class="team-header">
                <h1>Our Team</h1>
                <p class="team-header-description">CTFN was born out of the desire to meet the need for quality
                    reporting on major corporate events. We
                    are committed to excellent journalism and strive to meet our readers' unique demand for timely
                    information by employing intrepid and experienced reporters and analysts who share our core values
                    of
                    integrity and a desire to seek the truth.</p>
            </header>

            <b-row>
                <b-col lg="4" v-for="(teams, i) in team" :key="i" class="mt-5">
                    <div class="team-member h-100">
                        <div class="team-member-content">
                            <h3 class="team-name">{{ teams.firstName }} {{ teams.lastName }}</h3>
                            <h4 class="team-title">{{ teams.title }}</h4>
                            <div class="horizontal-line-style"></div>
                            <p class="team-bio">{{ teams.biography }}</p>
                        </div>
                    </div>
                </b-col>
            </b-row>

            <header class="team-header mt-5">
                <h1>Team Members</h1>
                <p class="team-header-description">Our growing team of journalists has decades of investigative
                    reporting experience and is supported by
                    multiple seasoned and well-researched analysts.</p>
            </header>

            <b-row>
                <b-col lg="4" v-for="(members, i) in member" :key="i" class="mt-5">
                    <div class="team-member h-100">
                        <div class="team-member-content">
                            <h3 class="team-name">{{ members.firstName }} {{ members.lastName }}</h3>
                            <h4 class="team-title">{{ members.title }}</h4>
                            <div class="horizontal-line-style"></div>
                            <p class="team-bio">{{ members.biography }}</p>
                        </div>
                    </div>
                </b-col>
            </b-row>
        </b-container>
    </section>
</template>

<script>

export default {
    name: "Team",
    data() {
        return {
            team: [
                {
                    firstName: "Jonathan",
                    lastName: "Spitzer",
                    title: "CEO",
                    biography: "Jonathan founded CTFN to provide quality news on major corporate actions and regulatory events. CTFN's mission is to provide insights for analysts, portfolio managers, deal professionals, regulators, and corporate executives who seek news and analysis with context and perspective. Jonathan previously was a merger arbitrage analyst at Arnhold and S. Bleichroeder Advisers, as well as co-portfolio manager of the merger arbitrage funds at Arnhold and S. Bleichroeder (First Eagle Investment Management). He earned a BA from Yale College (summa cum laude, Phi Beta Kappa) and an MBA from Columbia Business School (Beta Gamma Sigma)."
                },
                {
                    firstName: "Reuben",
                    lastName: "Miller",
                    title: "Executive Editor",
                    biography: "Reuben Miller is a seasoned reporter and editor with more than a decade of experience advancing coverage in investor-oriented news. Previously he ran the Washington DC bureau for an M&A product of the Financial Times Group, launched and managed ReOrg Research's event-driven coverage, and worked as the research director at a financial services firm. Reuben has also worked on Capitol Hill, at a boutique law firm, and thoroughly enjoyed a stint as a wildland firefighter in the Oregon wilderness. He holds a BA in Political Science from Lewis & Clark College."
                }, 
                {
                    firstName: "Melissa",
                    lastName: "Walker",
                    title: "General Counsel and Director of Compliance",
                    biography: "Melissa is a securities lawyer and compliance professional who has focused her practice on representing clients in securities litigation matters, including insider trading, market timing, the Investment Company Act of 1940, earnings management, and corporate governance. Previously, Melissa worked at Ropes & Gray, LLP in Washington, D.C., and New York. She holds a J.D. from George Washington University Law School, where she was a member of The George Washington Law Review, and a B.A. from the University of North Carolina at Chapel Hill, in Journalism and Political Science."
                },
                {
                    firstName: "Nils",
                    lastName: "Tracy",
                    title: "Senior Product Manager and Deputy Editor",
                    biography: "Nils is CTFN's senior regulatory and legal reporter covering special situations arising at the federal, state, and local level. Prior to joining CTFN, Nils founded Isogriv, an artificial intelligence platform for event driven investors and attorneys. He has also held positions as an event driven analyst at FiscalNote and Height Capital Markets. Nils previously ran the M&A and Event Driven products at Reorg, Inc. He holds an MA from Duke University with a concentration in Economics, a JD from Suffolk University Law School, and a BA from Miami University (OH)."
                }, 
                {
                    firstName: "Kara",
                    lastName: "Sullivan",
                    title: "Director of Engagement",
                    biography: "Kara joined CTFN to support sales and marketing initiatives. She spent seven years in distribution sales and marketing for A&E Television Networks, and more than five years in account management, at several advertising and branding agencies in NYC and CT. Kara seeks to forge a partnership with CTFN readers so that understanding their evolving needs remains a top priority. She is a graduate of Smith College."
                }, 
                {
                    firstName: "Stephen",
                    lastName: "Velgot",
                    title: "Director of Research",
                    biography: "Stephen has more than 20 years of experience as a research analyst. He started an event driven research product at Renaissance Macro Research, after covering risk arbitrage at ICAP and event driven situations at Susquehanna and Cathay Financial. Stephen has an MBA in Finance from New York University and a BS in Operations Research from Cornell University."
                }, 
                {
                    firstName: "Greg",
                    lastName: "Falkowski",
                    title: "Director of Operations",
                    biography: "Greg has 15 years experience working in financial news and data at the Mergermarket Group (Acuris) in New York, where he built and managed large structured and unstructured data sets and designed customized products that identified trading opportunities. Greg has experience collaborating with commercial teams to provide consultative account support, hiring and supervising remote research teams, and improving data management processes and systems. He earned a BA in Finance from Wake Forest University. Greg will move into a role at CTFN as a reader advocate, working to ensure the best user experience for our valued subscribers."
                }, 
                {
                    firstName: "Esther",
                    lastName: "D'Amico",
                    title: "Deputy Editor",
                    biography: "Esther will initially focus on antitrust coverage, serve as a writing coach resource for reporters, and help to further develop CTFN's in-house style. Prior to joining CTFN, Esther led US antitrust, CFIUS, and congressional coverage at Acuris's Dealreporter and PaRR. She has covered such crises as the September 11 attacks and Superstorm Sandy, and has led coverage on several industrial beats including chemicals and transportation. Originally from Long Island, she has a bachelor's degree in journalism and English from Texas Christian University."
                },                                                                                                                    
            ],
            member: [
                {
                    firstName: "Michael",
                    lastName: "Bow",
                    title: "European Commission and UK Competition and Markets Authority Reporter",
                    biography: "Michael is based in Brussels and previously spent 10 years in London writing about the City. He was City Correspondent at the Evening Standard between 2015 and 2020 covering insurance, fund management, and the M&A beat. Before that he wrote for daily free sheet City A.M. covering private equity and hedge funds and began his financial reporting career in the trade press writing about institutional pensions for Incisive Media. He holds a BA from the University of Birmingham and an Msc from the University of Oxford."
                },
                {
                    firstName: "Robert W.",
                    lastName: "Welkos",
                    title: "Senior Public Utilities, FCC and Special Coverage Reporter",
                    biography: "Bob covers utility, cable, and banking deals, and has a great skill for understanding the nuances of state regulatory processes. Bob was a 20-year veteran reporter for the Los Angeles Times and shared in two Pulitzer Prizes awarded to the newspaper's metro staff. He has reported on numerous state and federal trials and served as the Times entertainment industry legal affairs writer covering Hollywood and the law. Bob was also a correspondent for the Associated Press. He is based in Los Angeles."
                }, 
                {
                    firstName: "Victoria",
                    lastName: "Turner",
                    title: "DC Regulatory Reporter",
                    biography: "Victoria's background brings together an array of work experience from the private to public sectors. Prior to joining CTFN, Victoria briefly wrote for The Well News where she focused on telecommunications, technology, and business. Before TWN, she worked as an antitrust reporter covering policy developments and market-moving news for Acuris, where she led the Telecommunications, Media and Technology beat. A native Venezuelan, she leveraged her bilingual fluency to expand the Latin America coverage by reporting on cross-border M&A. She holds a BA in Journalism from Baylor University and a postgraduate certificate from St. Mary's University at Twickenham, UK."
                },
                {
                    firstName: "Saniya",
                    lastName: "Rao",
                    title: "M&A and Telecom Policy Reporter",
                    biography: "Saniya Rao is a graduate of the Master of Professional Studies in Journalism program at Georgetown University, prior to which she did her undergraduate studies in communications, literature, and psychology. Her work experience includes interning in social media for Agence France-Presse, working as a breaking news copywriter for Republic World in Mumbai, and as reporting intern with The Economic Times in Bengaluru. Saniya covers key aspects of telecom policy for CTFN from Washington, DC."
                }, 
                {
                    firstName: "Lucas",
                    lastName: "Savoie",
                    title: "Research Analyst",
                    biography: "Luke joined CTFN as a research analyst after completing his degree in Economics at Occidental College in Los Angeles. During his tenure there, Luke played college football and basketball and spent his summers interning in New York as an analyst in foreign exchange operations."
                }, 
                {
                    firstName: "Travis",
                    lastName: "Morrow",
                    title: "Product Development Manager & M&A Correspondent",
                    biography: "Travis has several years experience in M&A and antitrust research. Travis previously worked at Reorg M&A where he covered a wide range of M&A transactions and regulatory events. He also worked at Isogriv, continuing his research and analysis of M&A and event-driven financial coverage, as well as helping to launch Isogriv's data platform. He holds a BA in Government from Harvard University."
                }, 
                {
                    firstName: "Collin",
                    lastName: "Harvel",
                    title: "Policy Risk Correspondent & Product Team Member",
                    biography: "Collin covers political, regulatory, and litigation risks at the state and federal levels. Prior to joining CTFN, he worked as an investment analyst covering the financial services, payments, and tobacco and cannabis industries. Collin's strong understanding of parliamentary processes, legislative drivers, and market-based policy impacts enables him to effectively synthesize crucial information and communicate it to readers in an actionable way. Collin received a BA in International Relations from American University and studied Russian Language and Culture at Middlebury College."
                }, 
                {
                    firstName: "Natasha",
                    lastName: "Snyder",
                    title: "Senior Healthcare Markets Correspondent",
                    biography: "Natasha's role at CTFN is a senior healthcare correspondent, covering relevant legislative, regulatory, and political catalysts at the federal and state level across a variety of healthcare sub-sectors. Prior to joining CTFN, Natasha was a policy analyst at FiscalNote where she covered an array of issues for investors including provider and payer payment systems, drug pricing, and digital health. Previously, she held a senior healthcare analyst position at the Marwood Group in Washington, DC. Natasha received her BA from Vanderbilt University."
                }, 
                {
                    firstName: "Alex",
                    lastName: "Wilts",
                    title: "Senior Regulatory Reporter & DC Bureau Chief",
                    biography: "Based in Washington, DC, Alex covers merger enforcement developments at the DOJ's antitrust division, the FTC, and national security reviews conducted by CFIUS. Prior to joining CTFN, she oversaw coverage of US antitrust news for Global Competition Review. Alex has also written for several different outlets, including Reuters, Reorg, and The Independent. She graduated from The University of Texas at Austin in 2015 with degrees in marketing and journalism."
                }, 
                {
                    firstName: "Deane",
                    lastName: "McRobie",
                    title: "Senior UK/Europe Pre-Event and Special Situations Reporter",
                    biography: "Deane came to CTFN from Mergermarket and its affiliated publications Dealreporter, Activistmonitor, and PaRR. He has served as editor of Activistmonitor, and his reporting has focused on the consumer, retail and leisure sectors, including scoops on such megadeals as AB InBev's acquisition of SABMiller, British American Tobacco's purchase of Reynolds American, and EssilorLuxottica's bid for Grandvision. Originally from Canada, he graduated from McGill University with a degree in political science and East Asian language studies."
                }, 
                {
                    firstName: "Lucia",
                    lastName: "Molina",
                    title: "Legal Associate",
                    biography: "Lucia is a legal associate with a diverse background in technology, entrepreneurship, IP law, and social justice. She holds a Juris Doctor from Loyola College of Law New Orleans with a focus on IP law. Throughout her time at Loyola, she interned at the Orleans Parish Criminal District Court House as a judicial intern and at the Gillis Long Poverty Law Center as a legal intern. In her last year of law school, Lucia was inducted by the Supreme Court of Louisiana to work as a student practitioner in the nationally ranked Stuart H. Smith Law Clinic & Center for Social Justice and participated in the Workplace Litigation Clinic. She also worked at Isogriv, continuing patent research and leading compliance initiatives. Before attending Loyola, she graduated from Baylor University with a BBA in Management Information Systems from the Hankamer School of Business."
                }, 
                {
                    firstName: "Graham",
                    lastName: "Riss",
                    title: "Research Analyst",
                    biography: "Graham Riss is a research analyst with a broad interest and understanding of the financial markets, and enjoys analyzing various industries. He has been training with CTFN's Director of Research and editors since August of 2021. Graham currently has an associates degree from NCC and is working towards receiving a bachelors in finance."
                },                                                                                                                                   
            ]                            
        }
    }
}

</script>

<style scoped>
@import "../assets/styles/team.css";
</style>