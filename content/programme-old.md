---
title: "CHR2024 Programme"
layouttype: "single" 
draft: true
---

<style>
/* CSS TABS */
/* modified from https://codepen.io/markcaron/pen/MvGRYV */
/* - NOTE THAT THEY REQUIRE A LITTLE JAVA TO FUNCTION PROPERLY, which is written at the END of programme.md*/

/* interaction part of CSS */
.tabset > input[type="radio"] {
  position: absolute;
  left: -200vw;
}

.tabset .tab-panel {
  display: none;
}

.tabset > input:first-child:checked ~ .tab-panels > .tab-panel:first-child,
.tabset > input:nth-child(3):checked ~ .tab-panels > .tab-panel:nth-child(2),
.tabset > input:nth-child(5):checked ~ .tab-panels > .tab-panel:nth-child(3),
.tabset > input:nth-child(7):checked ~ .tab-panels > .tab-panel:nth-child(4),
.tabset > input:nth-child(9):checked ~ .tab-panels > .tab-panel:nth-child(5),
.tabset > input:nth-child(11):checked ~ .tab-panels > .tab-panel:nth-child(6) {
  display: block;
}

/* Styling*/
.tabset > label { /* label */
  position: relative;
  display: inline-block;
  padding: 15px 15px 25px;
  border: 1px solid transparent;
  border-bottom: 0;
  cursor: pointer;
  font-weight: 600;
  font-size: 1.2em !important;
}

.tabset > label::after {
  content: "";
  position: absolute;
  left: 15px;
  bottom: 10px;
  width: 22px;
  height: 4px;
  background: #8d8d8d; /* inactive tab: color of line underneath tab*/
}

input:focus-visible + label {
  outline: 2px solid rgba(0,102,204,1);
  border-radius: 3px;
}

.tabset > label:hover,
.tabset > input:focus + label,
.tabset > input:checked + label {
  color: #0B25DA; /* active tab: color of label*/
}

.tabset > label:hover::after,
.tabset > input:focus + label::after,
.tabset > input:checked + label::after {
  background: #0B25DA; /* active tab: color of line underneath tab */
}

.tabset > input:checked + label {
  border-color: #ccc;
  border-bottom: 1px solid #fff;
  margin-bottom: -1px;
}

.tab-panel {
  padding: 30px 0;
  border-top: 1px solid #ccc;
}
/* PROGRAMME STYLING in 'DETAILED VIEW' */
    .paper-entry {
        font-size: 1.15em;
        margin: 0;
        padding: 1rem 1.5rem;
        border-left: 1px solid rgba(0,0,0,0.1);
        border-right: 1px solid rgba(0,0,0,0.1);
    }
    .paper-entry:last-child {
        border-bottom: 1px solid rgba(0,0,0,0.1);
        border-radius: 0 0 8px 8px;
    }
    .paper-title {
        font-weight: 500;
    }

    .paper-authors {
        margin-left: 0;
        margin-top: 0em;
        display: block;
        font-style: italic;
        font-size: 0.9em;
    }
    .paper-type {
        font-size: 0.9em;
        vertical-align: super;
        margin-left: 0.25em;
    }
    .session-block {
        margin-bottom: 1.5rem;
        background: #fff;
        box-shadow: 0 2px 4px rgba(0,0,0,0.05);
    }
    .session-a h3 {
        background-color: #601843;
        font-weight: 600;
        margin: 0;
        padding: 1rem 1.5rem;
        color: #fff;
        border-radius: 8px 8px 0 0;
        font-size: 1.25rem;
        line-height: 1.4;
    }
    .session-b h3 {
        background-color: #132344;
        font-weight: 600;
        margin: 0;
        padding: 1rem 1.5rem;
        color: #fff;
        border-radius: 8px 8px 0 0;
        font-size: 1.25rem;
        line-height: 1.4;
    }
    .session-a .paper-entry {
        background-color: rgba(96,24,67,0.03);
    }
    .session-b .paper-entry {
        background-color: rgba(19,35,68,0.03);
    }
    .session-a .paper-entry:nth-child(even) {
        background-color: rgba(96,24,67,0.06);
    }
    .session-b .paper-entry:nth-child(even) {
        background-color: rgba(19,35,68,0.06);
    }
    .alt-session h3 {
        background: linear-gradient(45deg, #601843, #132344);
        font-weight: 600;
        margin: 0;
        padding: 1rem 1.5rem;
        color: #fff;
        border-radius: 8px 8px 0 0;
        font-size: 1.25rem;
        line-height: 1.4;
    }
    .alt-session .paper-entry {
        background-color: rgba(19,35,68,0.02);
    }

    .meta-data { /* What is written underneath session A/B title e.g., zoom link, building number, chair */
        display: block;
        font-size: 1em;
        color: #fff;
        text-align: left;
        margin: 0;
        padding: 0rem 1rem 1rem; /* match the h3 padding */
        font-weight: 650;
    }

    /* Session A meta-data style */
    .session-a .meta-data {
        background-color: #601843;
    }

    /* Session B meta-data style */
    .session-b .meta-data {
        background-color: #132344;
    }

    /* Alt session meta-data style */
    .alt-session .meta-data {
        background: linear-gradient(45deg, #601843, #132344);
    }

    .meta-data .separator {
    margin: 0 0.5rem;
    color: rgba(255,255,255,0.8);
    }

    .meta-item {
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    /* bordered style */
    .bordered-layout {
        display: flex;
    }

    .meta-section {
        padding: 0 0.5rem;
        border-right: 2px solid rgba(255,255,255,0.7);
    }

    .meta-section:last-child {
        border-right: none;
}

    @media screen and (max-width: 768px) {
        .meta-data {
            font-size: 0.7em !important;
        }
    }
/* table made for the programme at the tob of the tabs */
.schedule-table {
    width: 100%;
    max-width: 1000px;
    border-collapse: separate;
    border-spacing: 0;
    text-align: left; 
    padding-left: 0;
    margin: 3rem 0;
}

.schedule-table tr {
    border-bottom: 100px solid #eee;
}

.schedule-table td {
    padding: 1rem;
    vertical-align: top;
}

.schedule-table .time {
    position: relative; /* Make this a relative container */
    width: 140px;
    font-family: monospace;
    color: #555;
    white-space: nowrap;
}

.schedule-table tr:first-of-type .time::before {
    content: "Time in CET";
    position: absolute;
    top: -0.4rem; 
    left: 1rem;
    right: 0;
    font-size: 0.8rem;
    color: #999;
    text-align: left;
}

.schedule-table .highlight {
    font-weight: bold;
}

.schedule-table .location {
    font-size: 0.875rem;
    color: #383D43;
}

.schedule-table .location a {
    color: #383D43;
}

/* ZOOM CARDS - They are supposed to resemble the banners in venue.md, but with a twist to signal that they don't do exactly the same */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  padding: 1rem 0 0 0;
  max-width: 1200px;
  margin: 0 auto;
}

.card {
  border-radius: 10px;
  transition: all 0.3s ease;
  overflow: hidden;
  background: white;
  border: 2px solid;
}

.session-a { border-color: #601843; }
.session-b { border-color: #132344; }

.card a {
  color: #333;
  text-decoration: none !important;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 15px;
  height: 100%;
}

.text-content {
  flex-grow: 1;
}

.zoom-indicator {
  font-weight: 600;
  font-size: 1.1rem;
  margin-bottom: 0.25rem;
  color: inherit;
}

.card span {
  display: block;
  font-size: 0.9rem;
  color: #666;
  margin-top: 0.25rem;
}

.arrow-circle {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-left: 10px;
  transition: all 0.3s ease;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.session-a .arrow-circle {
  background-color: #601843;
  color: white;
}

.session-b .arrow-circle {
  background-color: #132344;
  color: white;
}

.card:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  transform: translateY(-3px);
  border-color: rgba(96, 24, 67, 0.8); /* Slightly intensify the border colour */
}

@media (max-width: 768px) {
  .cards-grid {
    grid-template-columns: 1fr;
    gap: 0rem;
  }
  
  .arrow-circle {
    width: 28px;
    height: 28px;
  }
  
  .zoom-indicator {
    font-size: 1rem;
  }

  .card:hover {
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.1);
    transform: translateY(-1px);
  }
}

</style>
<!-- HTML FOR PROGRAMME -->
Programme for the [pre-conference workshops](#parallel-workshops) on [Tuesday](#tuesday), 3rd December 2024, and the main conference days on [Wednesday](#wednesday), [Thursday](#thursday), and [Friday](#friday), 4th-6th December 2024. See all [accepted papers](/papers).

The main venue address of CHR2024 is *Bartholins Allé 8, 8000 Aarhus C*. See [*Finding the Venue*](/venue/finding-the-venue). 

*Note: Changes may occur in the programme. Please check regularly for the latest information.*

<!-- DAYS -->
<div class="tabset">

  <!-- button creation -->
  <!-- TUE -->
  <input type="radio" name="tabset" id="tuesday" aria-controls="tuesday">
  <label for="tuesday">Tuesday</label>
  <!-- WED -->
  <input type="radio" name="tabset" id="wednesday" aria-controls="wednesday" checked>
  <label for="wednesday">Wednesday</label>
  <!-- THUR -->
  <input type="radio" name="tabset" id="thursday" aria-controls="thursday">
  <label for="thursday">Thursday</label>
  <!-- FRI -->
  <input type="radio" name="tabset" id="friday" aria-controls="friday">
  <label for="friday">Friday</label>
  
  <!-- content -->
  <div class="tab-panels">
  <section id="tuesday" class="tab-panel" alt="tab showing the schedule for tuesday">
   <h2 id="overview-tue" alt="Overview of Tuesday" style="font-weight:bold;">Tuesday, December 3, 2024 (Pre-conference workshops)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">09:00 - 12:30</td>
            <td>
                <a href="#parallel-workshops"><span class="highlight">Workshop sessions</span></a>
                <div class="location">
                    Workshop A: <a href="https://international.au.dk/about/contact/?b=1325#c556911">Building 1325,</a> Room 028 <br>
                    Workshop B: <a href="https://maps.app.goo.gl/6NTA9rnaJ2U39SGF6">Heimdal Conference Center</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:30 - 13:30</td>
            <td>
                Lunch
            </td>
        </tr>
        <tr>
            <td class="time">13:30 - 17:00</td>
            <td>
                <a href="#parallel-workshops"><span class="highlight">Workshop sessions</span></a>
                <div class="location">
                    Workshop A: <a href="https://international.au.dk/about/contact/?b=1325#c556911">Building 1325,</a> Room 028 <br>
                    Workshop B: <a href="https://maps.app.goo.gl/6NTA9rnaJ2U39SGF6">Heimdal Conference Center</a>
                </div>
            </td>
        </tr>
    </table>
   <h3 id="parallel-workshops" style="font-weight:bold; font-size:2em;">Parallel Workshops<h3>
   <h3> Workshop A: Digital Methods for Mythological Research </h3>
   <p style="font-size:1em">
    dm4myth aims to bring together researchers from various disciplines who are interested in studying myths with digital tools and methods.
    We welcome contributions from various disciplines, such as (but not limited to) Ancient Near Eastern Studies, Religious Studies, Classical Studies/Classical Philology, Art History.
    The primary focus of this workshop is to explore the narrative material of mythological stories, underlying belief systems, and the multifaceted representation of characters in mythological contexts using digital methods.
    The full-day workshop is targeted at scholars who work on interdisciplinary research questions, which involve mythological (and derivative) topics and the application or development of computer science methods and algorithms.
    We welcome participants from all stages of their academic career, from (under-)graduate students to early career researchers and senior researchers. (<a href="https://dm4myth.github.io">https://dm4myth.github.io</a>)
   </p>
   <p>
   <h3> Workshop B: Analysing the Reception of Fiction Novels Across Languages</h3>
    <p style="font-size:1em">
    This workshop delves into the intersection of cultural practices and the digital sphere through a hands-on exploration of multilingual fiction book reviewing. 
    It offers participants an immersive experience, guiding them through the full research workflow of computational reader response studies, using book reviews and online comments as proxies for reception.
    Scheduled as four sessions, the workshop provides data and addresses key theoretical, methodological, and interpretive challenges to give participants a comprehensive understanding of the process. It is particularly suited for early career researchers, while senior researchers are also encouraged to attend and engage in discussions on theory and methodology. 
    Participants will gain practical experience with advanced NLP methods, statistical modeling, and computational approaches to reader response studies. Basic familiarity with Python is recommended.
    (<a href="https://igelsociety.github.io/CHR2024-book-reviews-workshop/">https://igelsociety.github.io/CHR2024-book-reviews-workshop/</a>)
    <br>
    <br>
    <i> Note: A maximum of 30 people can attend this workshop, and registered participants of the conference who indicated an interest in this workshop are selected on a first-come-first-serve basis.</i>
   </p>
   </p>
  </section>
  <!-- WED -->
    <section id="wednesday" class="tab-panel" alt="tab showing the schedule for wednesday">
    <h2 id="overview-wed" alt="Overview of Wednesday" style="font-weight:bold;">Wednesday, December 4, 2024 (Day 1)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">09:00 - 11:00</td>
            <td>
                Registration, breakfast and coffee
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1321#c556911">Building 1321</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">11:00 - 11:30</td>
            <td>
                CHR opening words
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1343#c556911">Building 1343,</a> Room 275
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">11:30 - 12:30</td>
            <td>
                <span class="highlight">Keynote by <a href="#keynote-leon-derczynski">Leon Derczynski</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1343#c556911">Building 1343,</a> Room 275
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:30 - 13:30</td>
            <td>
                Lunch
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1422#c556911">Building 1422,</a> Rooms 122, 125, and 132
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:45 - 15:15</td>
            <td>
                <span class="highlight"><a href="#session1A">Session 1A</a> / <a href="#session1B">Session 1B</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>, Rooms 011 / 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:15 - 15:30</td>
            <td>
                Coffee Break
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:30 - 17:00</td>
            <td>
                <span class="highlight"><a href="#session2A">Session 2A</a> / <a href="#session2B">Session 2B</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a>  Rooms 011 / 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">17:00</td>
            <td>
                Opening reception
                <div class="location">
                <a href="https://www.google.com/maps/place/Museum+of+Ancient+Art,+Aarhus/@56.1699487,10.2046871,17z/data=!4m6!3m5!1s0x464c3fc7a1945547:0xfe0ce45f63d0bd34!8m2!3d56.1704672!4d10.2004485!16s%2Fg%2F122l34s_?entry=tts&g_ep=EgoyMDI0MTExOS4yIPu8ASoASAFQAw%3D%3D">Museum of Ancient Art</a></div>
            </td>
        </tr>
    </table>
<!-- zoom overview -->
<h3 style="font-weight:bold; font-size:1.8em;">ZOOM/WIFI</h3>
<span>
For online participants, please navigate to the correct Zoom link:
</span>
<div class="cards-grid">
  <div class="card session-a">
    <a href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link A</div>
        <span>For Session A, Keynotes, and Lightning Talks</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
  <div class="card session-b">
    <a href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link B</div>
        <span>For Session B only</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
</div>
<br>
<span>
<strong>WIFI</strong><br>
For in-person participants, WiFi is available via <a href="https://eduroam.au.dk/en/">Eduroam</a>.
</span>
<!-- detailed overview -->
<h3 style="font-weight:bold; font-size:2.3em;">Detailed View</h3>
<div class="session-block alt-session">
<h3 id="keynote-leon-derczynski" alt="Keynote Leon Derczynski (11:30-12:30)">Keynote (11:30-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1343#c556911">Building: 1343</a>, Room: 275</span><span class="meta-section">Chair: Laure Thompson</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div>
<p class="paper-entry"><a href="/announcements/leon-derczynski#the-keynote" class="paper-title">What Computer Science Can’t Fix About LLM Security</a><span class="paper-authors">Leon Derczynski</span></p>
</div>
<!-- session heading -->
<h2 id="session1" style="font-weight:bold; font-size:1.8em;">Session 1</h2>
<!-- Session 1A -->
<div class="session-block session-a">
<h3 id="session1A" alt="Session 1A: Visual Arts and Art History (13:30-15:00)">Session 1A: Visual Arts and Art History (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 011</span><span class="meta-section">Chair: Lauren Tilton</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper20" class="paper-title">Viability of Zero-shot Classification and Search of Historical Photos</a><span class="paper-type">(long)</span><span class="paper-authors">Erika Maksimova, Mari-Anna Meimer, Mari Piirsalu and Priit Järv</span></p>
<p class="paper-entry"><a href="/papers/paper71" class="paper-title">Transformation of Composition and Gaze Interaction in Noli Me Tangere Depictions from 1300–1600</a><span class="paper-type">(short)</span><span class="paper-authors">Pepe Ballesteros Zapata, Nina Arnold, Vappu Lukander, Ludovica Schaerf and Dario Negueruela del Castillo</span></p>
<p class="paper-entry"><a href="/papers/paper123" class="paper-title">Deciphering Still Life Artworks with Linked Open Data</a><span class="paper-type">(short)</span><span class="paper-authors">Bruno Sartini</span></p>
<p class="paper-entry"><a href="/papers/paper141" class="paper-title">Computational segmentation of Wayang Kulit video recordings using a Cross-Attention Temporal Model</a><span class="paper-type">(short)</span><span class="paper-authors">Hong Wei Shawn Liew and Miguel Escobar Varela</span></p>
<p class="paper-entry"><a href="/papers/paper82" class="paper-title">Assessing Burial Mound Intervisibility and Prominence at Regional Scale</a><span class="paper-type">(short)</span><span class="paper-authors">Adela Sobotkova</span></p>
</div>
      <!-- Session 1B -->
<div class="session-block session-b">
<h3 id="session1B" alt="Session 1B: Classification & Information Extraction (13:30-15:00)">Session 1B: Classification & Information Extraction (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Thibault Clérice</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper73" class="paper-title">Page Embeddings: Extracting and Classifying Historical Documents with Generic Vector Representations</a><span class="paper-type">(short)</span><span class="paper-authors">Carsten Schnober, Renate Smit, Manjusha Kuruppath, Kay Pepping, Leon van Wissen and Lodewijk Petram</span></p>
<p class="paper-entry"><a href="/papers/paper79" class="paper-title">Exploration of Event Extraction Techniques in Late Medieval and Early Modern Administrative Records</a><span class="paper-type">(short)</span><span class="paper-authors">Ismail Prada Ziegler</span></p>
<p class="paper-entry"><a href="/papers/paper130" class="paper-title">Subversive Characters and Stereotyping Readers: Characterizing Queer Relationalities with Dialogue-Based Relation Extraction</a><span class="paper-type">(long)</span><span class="paper-authors">Kent K. Chang, Anna Ho and David Bamman</span></p>
<p class="paper-entry"><a href="/papers/paper52" class="paper-title">Extracting Social Connections from Finnish Karelian Refugee Interviews Using LLMs</a><span class="paper-type">(long)</span><span class="paper-authors">Joonatan Laato, Jenna Kanerva, John Loehr, Virpi Lummaa and Filip Ginter</span></p>
</div>
<!-- session heading -->
<h2 id="session2" style="font-weight:bold; font-size:1.8em;">Session 2</h2>
<!-- Session 2A -->
<div class="session-block session-a">
<h3 id="session2A" alt="Session 2A: Literature (15:30-17:00)">Session 2A: Literature (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 011</span><span class="meta-section">Chair: Federico Pianzola</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper19" class="paper-title">Literary Time Travel: Distinguishing Past and Contemporary Worlds in Danish and Norwegian Fiction</a><span class="paper-type">(long)</span><span class="paper-authors">Jens Bjerring-Hansen, Ali Al-Laith, Daniel Hershcovich, Alexander Conroy and Sebastian Ørtoft Rasmussen</span></p>
<p class="paper-entry"><a href="/papers/paper59" class="paper-title">Recognising non-named spatial entities in literary texts: a novel spatial entities classifier</a><span class="paper-type">(short)</span><span class="paper-authors">Daniel Kababgi, Giulia Grisot, Federico Pennino and Berenike Herrmann</span></p>
<p class="paper-entry"><a href="/papers/paper97" class="paper-title">Latent Structures of Intertextuality in French Fiction</a><span class="paper-type">(short)</span><span class="paper-authors">Jean Barré</span></p>
<p class="paper-entry"><a href="/papers/paper36" class="paper-title">Global Coherence, Local Uncertainty - Towards a Theoretical Framework for Assessing Literary Quality</a><span class="paper-type">(short)</span><span class="paper-authors">Yuri Bizzoni, Pascale Feldkamp and Kristoffer Nielbo</span></p>
<p class="paper-entry"><a href="/papers/paper90" class="paper-title">Animacy in German Folktales</a><span class="paper-type">(short)</span><span class="paper-authors">Julian Häußler, Janis von Keitz and Evelyn Gius</span></p>
</div>
      <!-- Session 2B -->
<div class="session-block session-b">
<h3 id="session2B" alt="Session 2B: Semantic Analysis (15:30-17:00)">Session 2B: Semantic Analysis (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Barbara McGillivray</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper6" class="paper-title">Quantitative Framework for Word-Color Association and Application to 20th Century Anglo-American Poetry</a><span class="paper-type">(long)</span><span class="paper-authors">Sungpil Wang and Juyong Park</span></p>
<p class="paper-entry"><a href="/papers/paper92" class="paper-title">Domain Adaptation with Linked Encyclopedic Data: A Case Study for Historical German</a><span class="paper-type">(long)</span><span class="paper-authors">Thora Hagen</span></p>
<p class="paper-entry"><a href="/papers/paper95" class="paper-title">Tracing the Development of the Virtual Particle Concept Using Semantic Change Detection</a><span class="paper-type">(long)</span><span class="paper-authors">Michael Zichert and Adrian Wüthrich</span></p>
</div>
    </section>
  <!-- THUR -->
    <section id="thursday" class="tab-panel" alt="tab showing the schedule for thursday">
    <h2 id="overview-thu" alt="Overview of Thursday" style="font-weight:bold;">Thursday, December 5, 2024 (Day 2) </h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:30 - 09:00</td>
            <td>
                Breakfast
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:00 - 10:30</td>
            <td>
                <span class=highlight><a href="#lightningtalks">Lightning Talks</a> (<a href="https://cryptpad.fr/form/#/2/form/view/SF-ncSM0p9+HfFW-sg2NOwdB5mfWm052jMXCTMtJPb4/embed/">Feedback Platform</a>)</span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1343#c556911">Building 1343,</a> Room 275
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:30 - 11:00</td>
            <td>
                Coffee break
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">11:00 - 12:30</td>
            <td>
                <span class="highlight"><a href="#session3A">Session 3A</a> / <a href="#session3B">Session 3B</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> Rooms 011 / 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:30 - 13:30</td>
            <td>
                Lunch
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1422#c556911">Building 1422,</a> Rooms 122, 125, and 132
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:30 - 15:00</td>
            <td>
                <span class="highlight"><a href="#session4A">Session 4A</a> / <a href="#session4B">Session 4B</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> Rooms 011 / 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:00 - 15:30</td>
            <td>
                Coffee break
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:30 - 17:00</td>
            <td>
                <span class="highlight"><a href="#session5A">Session 5A</a> / <a href="#session5B">Session 5B</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> Rooms 011 / 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">17:00</td>
            <td>
                <span class="highlight"><a href="#postersession">Poster walk-around</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1422#c556911">Building 1422, </a> Room 122
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">20:00</td>
            <td>
                Conference dinner
                <div class="location">
                    <a href="/venue/conference-dinner#conference-dinner-transport">Restaurant Havnær</a>
                </div>
            </td>
        </tr>
    </table>
<!-- zoom overview -->
<h3 style="font-weight:bold; font-size:1.8em;">ZOOM/WIFI</h3>
<span>
For online participants, please navigate to the correct Zoom link:
</span>
<div class="cards-grid">
  <div class="card session-a">
    <a href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link A</div>
        <span>For Session A, Keynotes, and Lightning Talks</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
  <div class="card session-b">
    <a href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link B</div>
        <span>For Session B only</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
</div>
<br>
<span>
<strong>WIFI</strong><br>
For in-person participants, WiFi is available via <a href="https://eduroam.au.dk/en/">Eduroam</a>.
</span>
<!-- sessions overview -->
<h3 style="font-weight:bold; font-size:2.3em;">Detailed View</h3>
<!-- session heading -->
      <h2 id="session3" style="font-weight:bold; font-size:1.8em;">Session 3</h2>
<!-- Session 3A -->
<div class="session-block session-a">
<h3 id="session3A" alt="Session 3A: Literary Canon & Reception (11:00-12:30)">Session 3A: Literary Canon & Reception (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 011</span><span class="meta-section">Chair: Fotis Jannidis</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper76" class="paper-title">Literary Canonicity and Algorithmic Fairness: The Effect of Author Gender on Classification Models</a><span class="paper-type">(long)</span><span class="paper-authors">Ida Marie S. Lassen, Pascale Feldkamp Moreira and Yuri Bizzoni and Kristoffer Nielbo</span></p>
<p class="paper-entry"><a href="/papers/paper106" class="paper-title">Patterns of Quality: Comparing Reader Reception Across Fanfiction and Commercially Published Literature </a><span class="paper-type">(long)</span><span class="paper-authors">Mia Jacobsen, Yuri Bizzoni, Pascale Feldkamp Moreira and Kristoffer L. Nielbo</span></p>
<p class="paper-entry"><a href="/papers/paper86" class="paper-title">Univariate Statistical Analysis of a Non-Canonical Literary Genre. Quantifying German-Language One-Act Plays (1740–1850)</a><span class="paper-type">(long)</span><span class="paper-authors">Viktor J. Illmer, Dîlan Canan Çakir, Frank Fischer, Lilly Welz and Carsten Milling</span></p>
</div>
      <!-- Session 3B -->
<div class="session-block session-b">
<h3 id="session3B" alt="Session 3B: Stylometry (11:00-12:30)">Session 3B: Stylometry (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Petr Plecháč</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper15" class="paper-title">Abbreviation Application: A Stylochronometric Study of Abbreviations in the Oeuvre of Herne’s Speculum Scribe</a><span class="paper-type">(short)</span><span class="paper-authors">Caroline Vandyck and Mike Kestemont</span></p>
<p class="paper-entry"><a href="/papers/paper61" class="paper-title">Bootstrap Distance Imposters: High precision authorship verification with improved interpretability</a><span class="paper-type">(long)</span><span class="paper-authors">Ben Nagy</span></p>
<p class="paper-entry"><a href="/papers/paper121" class="paper-title">Promises from an Inferential Approach in Classical Latin Authorship Attribution</a><span class="paper-type">(short)</span><span class="paper-authors">Giulio Tani Raffaelli</span></p>
<p class="paper-entry"><a href="/papers/paper9" class="paper-title">Multilingual Stylometry: The influence of language on the performance of authorship attribution using corpora from the European Literary Text Collection (ELTeC)</a><span class="paper-type">(long)</span><span class="paper-authors">Christof Schöch, Julia Dudar, Evgeniia Fileva and Artjoms Šeļa</span></p>
</div>
<!-- session heading -->
<h2 id="session4" style="font-weight:bold; font-size:1.8em;">Session 4</h2>
      <!-- Session 4A -->
<div class="session-block session-a">
<h3 id="session4A" alt="Session 4A: Large Language Models (13:30-15:00)">Session 4A: Large Language Models (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 011</span><span class="meta-section">Chair: Ted Underwood</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper96" class="paper-title">Remember to Forget: A Study on Verbatim Memorization of Literature in Large Language Models</a><span class="paper-type">(long)</span><span class="paper-authors">Xinhao Zhang, Olga Seminck and Pascal Amsili</span></p>
<p class="paper-entry"><a href="/papers/paper122" class="paper-title">Does ChatGPT Have a Poetic Style?</a><span class="paper-type">(long)</span><span class="paper-authors">Melanie Walsh, Anna Preus and Elizabeth Gronski</span></p>
<p class="paper-entry"><a href="/papers/paper119" class="paper-title">On Classification with Large Language Models in Cultural Analytics</a><span class="paper-type">(long)</span><span class="paper-authors">David Bamman, Kent K. Chang and Li Lucy and Naitian Zhou</span></p>
</div>
      <!-- Session 4B -->
<div class="session-block session-b">
<h3 id="session4B" alt="Session 4B: Automatic Text Recognition (13:30-15:00)">Session 4B: Automatic Text Recognition (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Margherita Fantoli</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper30" class="paper-title">Does Context Matter ? Enhancing Handwritten Text Recognition with Metadata in Historical Manuscripts</a><span class="paper-type">(long)</span><span class="paper-authors">Benjamin Kiessling and Thibault Clérice</span></p>
<p class="paper-entry"><a href="/papers/paper35" class="paper-title">Enhancing Arabic Maghribi Handwritten Text Recognition with RASAM 2: A Comprehensive Dataset and Benchmarking</a><span class="paper-type">(long)</span><span class="paper-authors">Chahan Vidal-Gorène, Clément Salah, Noëmie Lucas, Aliénor Decours-Perez and Antoine Perrier</span></p>
<p class="paper-entry"><a href="/papers/paper110" class="paper-title">Steps Towards Mining Manuscript Images for Untranscribed Texts: A Case Study From the Syriac Collection at the Vatican Library</a><span class="paper-type">(long)</span><span class="paper-authors">Luigi Bambaci, George Kiraz, Christine Roughan, Matthieu Freyder and Daniel Stökl Ben Ezra</span></p>
</div>
<!-- session heading -->
<h2 id="session5" style="font-weight:bold; font-size:1.8em;">Session 5</h2>
<!-- Session 5A -->
<div class="session-block session-a">
<h3 id="session5A" alt="Session 5A: Linguistic Change (15:30-17:00)">Session 5A: Linguistic Change (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 011</span><span class="meta-section">Chair: Manex Agirrezabal</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper18" class="paper-title">A Methodology for Studying Linguistic and Cultural Change in China, 1900-1950</a><span class="paper-type">(long)</span><span class="paper-authors">Spencer Dean Stewart</span></p>
<p class="paper-entry"><a href="/papers/paper21" class="paper-title">The birth of French orthography. A computational analysis of French spelling systems in diachrony</a><span class="paper-type">(long)</span><span class="paper-authors">Simon Gabay and Thibault Clérice</span></p>
<p class="paper-entry"><a href="/papers/paper60" class="paper-title">SCIENCE IS EXPLORATION: Computational Frontiers for Conceptual Metaphor Theory</a><span class="paper-type">(short)</span><span class="paper-authors">Rebecca M. M. Hicke and Ross Deans Kristensen-McLachlan</span></p>
</div>
<!-- Session 5B -->
<div class="session-block session-b">
<h3 id="session5B" alt="Session 5B: Search & Discovery (15:30-17:00)">Session 5B: Search & Discovery (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Melanie Walsh</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper1" class="paper-title">Explainable Search and Discovery of Visual Cultural Heritage Collections with Multimodal Large Language Models</a><span class="paper-type">(long)</span><span class="paper-authors">Taylor Arnold and Lauren Tilton</span></p>
<p class="paper-entry"><a href="/papers/paper17" class="paper-title">Integrating Visual and Textual Inputs for Searching Large-Scale Map Collections with CLIP</a><span class="paper-type">(long)</span><span class="paper-authors">Jamie Mahowald and Benjamin Charles Germain Lee</span></p>
<p class="paper-entry"><a href="/papers/paper55" class="paper-title">Visual Navigation of Digital Libraries: Retrieval and Classification of Images in the National Library of Norway’s Digitised Book Collection</a><span class="paper-type">(short)</span><span class="paper-authors">Marie Roald, Magnus Breder Birkenes and Lars Gunnarsønn Bagøien Johnsen</span></p>
</div>
      <!-- Poster Session -->
<h2 style="font-weight:bold; font-size:1.8em;">Poster Session & Lightning Talks</h2>
<div class="session-block alt-session">
<h3 id="postersession" alt="Poster Session (17:00)">Poster Session (17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href=https://international.au.dk/about/contact/?b=1422#c556911>Building: 1422</a>, Room: 122</span></div><p class="paper-entry"><a href="/papers/paper4" class="paper-title">FAIR Turn in Epigraphy: Low Barrier Pathways to Quantitative and Reproducible Research in Latin Epigraphy</a><span class="paper-type">(short)</span><span class="paper-authors">Petra Heřmánková, Brian Ballsun-Stanton and Ray Laurence</span></p>
<p class="paper-entry"><a href="/papers/paper5" class="paper-title">Sub-optimal Recall in Visual Cluster Retrieval: When Clusters Look Like Bridges</a><span class="paper-type">(short)</span><span class="paper-authors">Mathieu Jacomy, Matilde Ficozzi and Anders K. Munk</span></p>
<p class="paper-entry"><a href="/papers/paper12" class="paper-title">Who Advertises in Newspapers? Data Criticism in Mining Historical Job Ads</a><span class="paper-type">(short)</span><span class="paper-authors">Klara Venglarova, Raven Adam, Wiltrud Mölzer, Saranya Balasubramanian, Jörn Kleinert, Manfred Füllsack and Georg Vogeler</span></p>
<p class="paper-entry"><a href="/papers/paper23" class="paper-title">Catching Feelings: Aspect-Based Sentiment Analysis for Fanfiction Comments about Greek Myth</a><span class="paper-type">(short)</span><span class="paper-authors">Julia Neugarten, Tess Dejaeghere, Pranaydeep Singh, Amanda Robin Hemmons and Julie M. Birkholz</span></p>
<p class="paper-entry"><a href="/papers/paper24" class="paper-title">Rediscovering the 1890s: A Norwegian Poetry Corpus</a><span class="paper-type">(short)</span><span class="paper-authors">Ranveig Kvinnsland, Ingerid Løyning Dale and Lars Magne Tungland</span></p>
<p class="paper-entry"><a href="/papers/paper27" class="paper-title">Exploring the Evolution of Gender Power Difference through the Omegaverse Trope on AO3 Fanfiction</a><span class="paper-type">(short)</span><span class="paper-authors">Xiaoyan Yang and Federico Pianzola</span></p>
<p class="paper-entry"><a href="/papers/paper28" class="paper-title">Automated Image Color Mapping for a Historic Photographic Collection</a><span class="paper-type">(short)</span><span class="paper-authors">Taylor Arnold and Lauren Tilton</span></p>
<p class="paper-entry"><a href="/papers/paper29" class="paper-title">Getting to grippe with influenza: an investigation of why the disease is called that</a><span class="paper-type">(short)</span><span class="paper-authors">Maria Bekker-Nielsen Dunbar, Manex Agirrezabal and Tønnes Bekker-Nielsen</span></p>
<p class="paper-entry"><a href="/papers/paper32" class="paper-title">Treebanks for the ordinary working grammarian</a><span class="paper-type">(short)</span><span class="paper-authors">Joel Priestley, Anders Nøklestad, Kristin Hagen, Anu Laanemets and Dag Trygve Truslew Haug</span></p>
<p class="paper-entry"><a href="/papers/paper41" class="paper-title">A quantitative study of gender representation and authors' gender in a large-market print medium</a><span class="paper-type">(short)</span><span class="paper-authors">Christoph Bartl, Sharwin Rezagholi and Mareike Schumacher</span></p>
<p class="paper-entry"><a href="/papers/paper43" class="paper-title">Clustering Tasks and Decision Trees with Augustan Love Poets: Cohesion and Separation in Feature Importance Extraction</a><span class="paper-type">(short)</span><span class="paper-authors">Carlos Javier Nusch, Gimena Del Río Riande, Leticia Cagnina, Marcelo Luis Errecalde and Leandro Antonelli</span></p>
<p class="paper-entry"><a href="/papers/paper56" class="paper-title">The discourse of the French method: making old knowledge on market gardening accessible to machines and humans.</a><span class="paper-type">(short)</span><span class="paper-authors">David Colliaux and Remi van Trijp</span></p>
<p class="paper-entry"><a href="/papers/paper58" class="paper-title">Bringing Rome to Life: Evaluating Historical Image Generation</a><span class="paper-type">(short)</span><span class="paper-authors">Phillip B. Ströbel, Zejie Guo, Ülkü Karagöz, Eva Maria Willi and Felix K. Maier</span></p>
<p class="paper-entry"><a href="/papers/paper63" class="paper-title">Across the Pages: A Comparative Study of Reader Response to Web Novels in Chinese and English on Qidian and WebNovel</a><span class="paper-type">(short)</span><span class="paper-authors">Ze Yu and Federico Pianzola</span></p>
<p class="paper-entry"><a href="/papers/paper78" class="paper-title">Discoverability in a Digital Library: A Study of “Rabbit Holes” within Gallica’s corpus</a><span class="paper-type">(short)</span><span class="paper-authors">Anne-Laure Tettoni and Simon Dumas Primbault</span></p>
<p class="paper-entry"><a href="/papers/paper80" class="paper-title">The GOLEM-Knowledge Graph and Search Interface: Perspectives into Narrative and Fiction</a><span class="paper-type">(short)</span><span class="paper-authors">Franziska Pannach, Luotong Cheng and Federico Pianzola</span></p>
<p class="paper-entry"><a href="/papers/paper99" class="paper-title">Text Mining to unveil Prehistoric Pastness in Museums</a><span class="paper-type">(short)</span><span class="paper-authors">Haley Anne Schwartz, Paula Jardón Giner and Xavier Rubio Campillo</span></p>
<p class="paper-entry"><a href="/papers/paper133" class="paper-title">Modeling the Evolution of Harmony in Popular Music from Different Cultural Contexts</a><span class="paper-type">(short)</span><span class="paper-authors">Fabian C. Moss and Eita Nakamura</span></p>
<p class="paper-entry"><a href="/papers/paper139" class="paper-title">Fine-Tuning Pre-Trained Language Models for Authorship Attribution of the Pseudo-Dionysian Ars Rhetorica</a><span class="paper-type">(short)</span><span class="paper-authors">Gleb Schmidt, Veronica Vybornaya and Ivan P. Yamshchikov</span></p>
</div>
      <!-- Lightning Session -->
<div class="session-block alt-session">
<h3 id="lightningtalks" alt="Lightning Talks (9:00-10:30)">Lightning Talks (9:00-10:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1343#c556911">Building: 1343</a>, Room: 275</span><span class="meta-section">Chair: Wouter Haverals</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span><span class="meta-section"><a style="color:white;" href="https://cryptpad.fr/form/#/2/form/view/SF-ncSM0p9+HfFW-sg2NOwdB5mfWm052jMXCTMtJPb4/embed/">Feedback Platform</a></span></div><p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Beauty, mediated: A media archeology of archived moving images for understanding local representations of human beauty</span><span class="paper-authors">Dana Kaplan and Vered Silber-Varod</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Well-Documented Terror: Navigating the Digital Records of the September 11th Attacks</span><span class="paper-authors">Ian Milligan</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Investigating Individual Composers' Style Evolution Using Deep Audio Features</span><span class="paper-authors">Benjamin Henzel and Christof Weiß</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">PoeTree: Poetry Treebanks in Ten Languages</span><span class="paper-authors">Petr Plecháč and Artjoms Šeļa</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Exploring Ecological Bias in Depictions of NYC Rivers in The New York Times</span><span class="paper-authors">Dez Miller</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Enhancing access to Danish radio and television archives through advanced speech-to-text technologies</span><span class="paper-authors">Lasse Rogers Nielsen, Lars Flemming Mydtskov and Ditte Laursen</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Metaphors of Artificial Intelligence in Contemporary Philosophy: A Computational Text Analysis of the PhilPapers Database</span><span class="paper-authors">Vojtech Kase, Jana Švadlenková and Jan Tvrz</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Towards Operationalizing Linguistic Creativity in Literary and Non-literary Text</span><span class="paper-authors">Emilie Sitter, Yaru Wu, Sina Zarrieß and J. Berenike Herrmann</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">A quest to build phylogenetic networks of literary fiction</span><span class="paper-authors">Oleg Sobchuk, Mason Youngblood, Artjoms Šeļa, Angela Chira, Olivier Morin and Ted Underwood</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Predictably Unpredictable? Characterizing Collective Cultural Consumption Shifts in Nation-Level Library Data</span><span class="paper-authors">Anders Weile and Vedran Sekara</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Leveraging ChatGPT for Multilingual Philosophical Logic Education: A Case Study with Hebrew and Arabic Translations</span><span class="paper-authors">Stav Klein and Ofra Rechter</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Finding pointers of discursively constructed news values in Danish journalism using computer-assisted methods</span><span class="paper-authors">Elisabeth Muth Andersen, Edward Abel and Kamilla Jensen Husen</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">From Kyiv to Paris, from Moscow to Siberia: mapping the ‘outward turn’ of Russian Literature in the 19th century</span><span class="paper-authors">Daniil Skorinkin and Orekhov Boris</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Second-order observation through AI: Towards a humanistic approach of augmenting human intellect</span><span class="paper-authors">Christian Wachter</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Modelling Book Auctions</span><span class="paper-authors">Marika Fox</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">What’s the Issue? Overcoming Copyright and Cataloguing Challenges for Computational Periodicals in the HathiTrust Collections</span><span class="paper-authors">Zoe LeBlanc and Daniel Evans</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Can Computationally Derived Metadata Help in the Bibliographic Recognition of “New” Nations? A Case for Learning-based Prediction</span><span class="paper-authors">Sayan Bhattacharyya</span></p>
<p class="paper-entry"><span class="paper-title" style="font-weight:bold;">Friendships, emotions and data driven literary studies</span><span class="paper-authors">Kirstine Nielsen Degn</span></p>
</div>
    </section>
    <!-- FRI -->
    <section id="friday" class="tab-panel" alt="tab showing the schedule for friday">
      <h2 id="overview-fri" alt="Overview of Friday" style="font-weight:bold;">Friday, December 6, 2024 (DAY 3)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:30 - 09:00</td>
            <td>
                Breakfast
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:00 - 10:00</td>
            <td>
                <span class="highlight">Keynote by <a href="#keynote-lauren-klein">Lauren Klein</a></span>
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1343#c556911">Building 1343,</a> Room 275 
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:00 - 10:30</td>
            <td>
                Coffee break
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1342#c556911">Building 1342</a> / <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:30 - 12:00</td>
            <td>
                <span class="highlight"><a href="#session6A">Session 6A</a>* / <a href="#session6B">Session 6B</a></span>
                <div class="location">
                  <a href="https://international.au.dk/about/contact/?b=1342#c556911">Building 1342,</a> 455 / <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:00 - 13:00</td>
            <td>
                Lunch
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1422#c556911">Building 1422,</a> Rooms 122, 125, and 132
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:00 - 14:30</td>
            <td>
                <span class="highlight"><a href="#session7A">Session 7A</a>* / <a href="#session7B">Session 7B</a></span>
                <div class="location">
                  <a href="https://international.au.dk/about/contact/?b=1342#c556911">Building 1342,</a> 455 / <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">14:30 - 15:00</td>
            <td>
                Coffee break
                <div class="location">
                     <a href="https://international.au.dk/about/contact/?b=1342#c556911">Building 1342</a> / <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324</a>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:00 - 16:15</td>
            <td>
                <span class="highlight"><a href="#session8A">Session 8A</a>* / <a href="#session8B">Session 8B</a></span>
                <div class="location">
                  <a href="https://international.au.dk/about/contact/?b=1342#c556911">Building 1342,</a> 455 / <a href="https://international.au.dk/about/contact/?b=1324#c556911">Building 1324,</a> 025
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">16:15 - 16:45</td>
            <td>
                Award ceremony, concluding remarks
                <div class="location">
                    <a href="https://international.au.dk/about/contact/?b=1343#c556911">Building 1343,</a> Room 275
                </div>
            </td>
        </tr>
    </table>
      <p style="color:darkred;">*NB: Session A has changed location today!</p>
<!-- zoom overview -->
<h3 style="font-weight:bold; font-size:1.8em;">ZOOM/WIFI</h3>
<span>
For online participants, please navigate to the correct Zoom link:
</span>
<div class="cards-grid">
  <div class="card session-a">
    <a href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link A</div>
        <span>For Session A, Keynotes, and Lightning Talks</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
  <div class="card session-b">
    <a href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">
      <div class="text-content">
        <div class="zoom-indicator">Zoom Link B</div>
        <span>For Session B only</span>
      </div>
      <div class="arrow-circle">→</div>
    </a>
  </div>
</div>
<br>
<span>
<strong>WIFI</strong><br>
For in-person participants, WiFi is available via <a href="https://eduroam.au.dk/en/">Eduroam</a>.
</span>
<!-- sessions overview -->
<h3 style="font-weight:bold; font-size:2.3em;">Detailed View</h3>
<div class="session-block alt-session">
<h3 id="keynote-lauren-klein" alt="Keynote Lauren Klein (11:30-12:30)">Keynote (09:00-10:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1343#c556911">Building: 1343</a>, Room: 275</span><span class="meta-section">Chair: Laure Thompson</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div>
<p class="paper-entry"><a href="/announcements/lauren-klein#the-keynote" class="paper-title">When Theory Leads: Towards a Humanities-Forward Model of Computational Research</a><span class="paper-authors">Lauren Klein</span></p>
</div>
<!-- session heading -->
<h2 id="session6" style="font-weight:bold; font-size:1.8em;">Session 6</h2>
<!-- Session 6A -->
<div class="session-block session-a">
<h3 id="session6A" alt="Session 6A: Annotation (10:30-12:00)">Session 6A: Annotation (10:30-12:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1342#c556911">Building: 1342</a>, Room: 455</span><span class="meta-section">Chair: Evelyn Gius</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper75" class="paper-title">Combining Automatic Annotation with Human Validation for the Semantic Enrichment of Cultural Heritage Metadata</a><span class="paper-type">(long)</span><span class="paper-authors">Eirini Kaldeli, Alexandros Chortaras, Vassilis Lyberatos, Jason Liartis, Spyridon Kantarelis and Giorgos Stamou</span></p>
<p class="paper-entry"><a href="/papers/paper46" class="paper-title">Models of Literary Evaluation and Web 2.0. An Annotation Experiment with Goodreads Reviews</a><span class="paper-type">(long)</span><span class="paper-authors">Simone Rebora and Gabriele Vezzani</span></p>
<p class="paper-entry"><a href="/papers/paper62" class="paper-title">Addressing Uncertainty according to the Annotator's Expertise in Archaeological Data Collections: an Approach from Fuzzy Logic</a><span class="paper-type">(short)</span><span class="paper-authors">Patricia Martin-Rodilla and Leticia Tobalina-Pulido</span></p>
<p class="paper-entry"><a href="/papers/paper74" class="paper-title">Direct and Indirect Annotation with Generative AI: A Case Study into Finding Animals and Plants in Historical Text</a><span class="paper-type">(short)</span><span class="paper-authors">Arjan van Dalfsen, Folgert Karsdorp, Ayoub Bagheri, Dieuwertje Mentink, Thirza van Engelen and Els Stronks</span></p>
</div>
<!-- Session 6B -->
<div class="session-block session-b">
<h3 id="session6B" alt="Session 6B: Multilingualism & Translation Studies (10:30-12:00)">Session 6B: Multilingualism & Translation Studies (10:30-12:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Christof Schöch</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper104" class="paper-title"> Textual Transmission without Borders: Multiple Multilingual Alignment and Stemmatology of the ``Lancelot en prose'' (Medieval French, Castilian, Italian)</a><span class="paper-type">(long)</span><span class="paper-authors">Matthias Gille Levenson, Lucence Ing and Jean-Baptiste Camps</span></p>
<p class="paper-entry"><a href="/papers/paper128" class="paper-title">Automatic Translation Alignment Pipeline for Multilingual Digital Editions of Literary Works</a><span class="paper-type">(short)</span><span class="paper-authors">Maria Levchenko</span></p>
<p class="paper-entry"><a href="/papers/paper135" class="paper-title">Early Modern Book Catalogues and Multilingualism: Identifying Multilingual Texts and Translations using Titles</a><span class="paper-type">(long)</span><span class="paper-authors">Yann Ryan and Margherita Fantoli</span></p>
<p class="paper-entry"><a href="/papers/paper42" class="paper-title">Computational Paleography of Medieval Hebrew Scripts</a><span class="paper-type">(short)</span><span class="paper-authors">Berat Kurar-Barakat, Daria Vasyutinsky-Shapira, Sharva Gogawale and Mohammad Suliman and Nachum Dershowitz</span></p>
</div>
<!-- session heading -->
<h2 id="session7" style="font-weight:bold; font-size:1.8em;">Session 7</h2>
<!-- Session 7A -->
<div class="session-block session-a">
<h3 id="session7A" alt="Session 7A: Social Patterns (13:00-14:30)">Session 7A: Social Patterns (13:00-14:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1342#c556911">Building: 1342</a>, Room: 455</span><span class="meta-section">Chair: Taylor Arnold</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper93" class="paper-title">And then I saw it: Testing Hypotheses on Turning Points in a Corpus of UFO Sighting Reports</a><span class="paper-type">(short)</span><span class="paper-authors">Jan Langenhorst, Robert C. Schuppe and Yannick Frommherz</span></p>
<p class="paper-entry"><a href="/papers/paper13" class="paper-title">Beyond the Register: Demographic Modeling of Arrest Patterns in 1879-1880 Brussels</a><span class="paper-type">(long)</span><span class="paper-authors">Folgert Karsdorp, Mike Kestemont and Margo de Koster</span></p>
<p class="paper-entry"><a href="/papers/paper39" class="paper-title">Epistemic Capture through Specialization in Post-World War II Parliamentary Debate</a><span class="paper-type">(long)</span><span class="paper-authors">Ruben Ros and Melvin Wevers</span></p>
<p class="paper-entry"><a href="/papers/paper94" class="paper-title">Revolution + Love: Measuring the Entanglements of State Violence and Emotions in Early PRC</a><span class="paper-type">(short)</span><span class="paper-authors">Maciej Kurzynski and Aaron Gilkison</span></p>
</div>
<!-- Session 7B -->
<div class="session-block session-b">
<h3 id="session7B" alt="Session 7B: Measuring Emotion & Sentiment (13:00-14:30)">Session 7B: Measuring Emotion & Sentiment (13:00-14:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Berenike Herrmann</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper67" class="paper-title">In the Context of Narrative, we Never Properly Defined the Concept of Valence</a><span class="paper-type">(long)</span><span class="paper-authors">Peter Boot, Angel Daza, Carsten Schnober and Willem van Hage</span></p>
<p class="paper-entry"><a href="/papers/paper98" class="paper-title">Sentiment Below the Surface: Omissive and Evocative Strategies in Literature and Beyond</a><span class="paper-type">(long)</span><span class="paper-authors">Pascale Feldkamp, Ea Overgaard Lindhardt, Kristoffer L. Nielbo and Yuri Bizzoni</span></p>
<p class="paper-entry"><a href="/papers/paper124" class="paper-title">Once More, With Feeling: Measuring Emotion of Acting Performances in Contemporary American Film</a><span class="paper-type">(long)</span><span class="paper-authors">Naitian Zhou and David Bamman</span></p>
</div>
<!-- session heading -->
<h2 id="session8" style="font-weight:bold; font-size:1.8em;">Session 8</h2>
<!-- Session 8A -->
<div class="session-block session-a">
<h3 id="session8A" alt="Session 8A: Cultural Dynamics (15:00-16:15)">Session 8A: Cultural Dynamics (15:00-16:15)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1342#c556911">Building: 1342</a>, Room: 455</span><span class="meta-section">Chair: Maria Antoniak</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/67695165152?pwd=6qMHyGDRznz3ai5QAr0CGlOY581tV8.1">Zoom Link A</a></span></div><p class="paper-entry"><a href="/papers/paper137" class="paper-title">On the Unity of Literary Change. The Development of Emotions in German Poetry, Prose, and Drama between 1850 and 1920 as a Test Case</a><span class="paper-type">(long)</span><span class="paper-authors">Leonard Konle, Merten Kröncke, Fotis Jannidis and Simone Winko</span></p>
<p class="paper-entry"><a href="/papers/paper49" class="paper-title">Context is Key(NMF): Modelling Topical Information Dynamics in Chinese Diaspora Media</a><span class="paper-type">(long)</span><span class="paper-authors">Ross Deans Kristensen-McLachlan, Rebecca M.M. Hicke, Márton Kardos and Mette Thunø</span></p>
<p class="paper-entry"><a href="/papers/paper70" class="paper-title">Locating the Leading Edge of Cultural Change</a><span class="paper-type">(short)</span><span class="paper-authors">Sarah Griebel, Becca Cohen, Lucian Li, Jiayu Liu, Jaihyun Park, Jana Perkins and Ted Underwood</span></p>
</div>
      <!-- Session 8B -->

<div class="session-block session-b">
<h3 id="session8B" alt="Session 8B: Popular Media (15:00-16:15)">Session 8B: Popular Media (15:00-16:15)</h3>
<div class="meta-data bordered-layout"><span class="meta-section"><a style="color:white;" href="https://international.au.dk/about/contact/?b=1324#c556911">Building: 1324</a>, Room: 025</span><span class="meta-section">Chair: Miguel Escobar Varela</span><span class="meta-section"><a style="color:white;" href="https://aarhusuniversity.zoom.us/j/65783702178?pwd=snxZ862z76NloikYZTjtZVKQ63YwH9.1">Zoom Link B</a></span></div><p class="paper-entry"><a href="/papers/paper132" class="paper-title">Treating Games as Plays? Computational Approaches to the Detection of Scenes in Game Dialogs</a><span class="paper-type">(short)</span><span class="paper-authors">Martin Schlenk, Thomas Efer and Manuel Burghardt</span></p>
<p class="paper-entry"><a href="/papers/paper57" class="paper-title">Admiration and Frustration: A Multidimensional Analysis of Fanfiction</a><span class="paper-type">(long)</span><span class="paper-authors">Mia Jacobsen and Ross Deans Kristensen-McLachlan</span></p>
<p class="paper-entry"><a href="/papers/paper102" class="paper-title">Greatest Hits Versus Deep Cuts: Exploring Variety in Set-lists Across Artists and Musical Genres</a><span class="paper-type">(long)</span><span class="paper-authors">Edward Abel and Andrew Goddard</span></p>
</div>
</section>
</div>


<!-- JS for making tabs and sections inside tabs linkable -->
<script>
function activateTabFromHash() {
    // get the current hash from the URL
    var hash = window.location.hash;
    if (hash) {
        // remove the '#' character
        var id = hash.substring(1);

        // first, try to find a radio button (tab control) with that ID
        var tabRadio = document.getElementById(id);
        if (tabRadio && tabRadio.name === 'tabset') {
            // activate the corresponding tab
            tabRadio.checked = true;
        } else {
            // if not found, try to find an element within a tab panel
            var targetElement = document.getElementById(id);
            if (targetElement) {
                // find the closest ancestor with class 'tab-panel'
                var tabPanel = targetElement.closest('.tab-panel');
                if (tabPanel) {
                    // get the id of the tab panel
                    var panelId = tabPanel.id;
                    // find the radio button whose aria-controls matches the panel id
                    var tabRadio = document.querySelector('input[name="tabset"][aria-controls="' + panelId + '"]');
                    if (tabRadio) {
                        // activate the corresponding tab
                        tabRadio.checked = true;
                    }
                }
            }
        }
    }
}

document.addEventListener("DOMContentLoaded", function() {
    activateTabFromHash();

    // update the URL hash when a new tab is selected
    var radios = document.querySelectorAll('.tabset > input[type="radio"]');
    radios.forEach(function(radio) {
        radio.addEventListener('change', function() {
            if (this.checked) {
                // update the URL hash to the radio button's ID
                history.replaceState(null, null, '#' + this.id);
            }
        });
    });
});

// listen for hash changes (e.g., when clicking on links to anchors)
window.addEventListener('hashchange', function() {
    activateTabFromHash();
});
</script>



