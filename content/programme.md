---
title: "CHR2025 Programme"
layouttype: "single" 
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
        background-color: #5d4157;
        font-weight: 600;
        margin: 0;
        padding: 1rem 1.5rem;
        color: #fff;
        border-radius: 8px 8px 0 0;
        font-size: 1.25rem;
        line-height: 1.4;
    }
    .session-b h3 {
        background-color: #a8caba;
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
        background: linear-gradient(45deg, #5d4157, #a8caba);
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
        background-color: #5d4157;
    }

    /* Session B meta-data style */
    .session-b .meta-data {
        background-color: #a8caba;
    }

    /* Alt session meta-data style */
    .alt-session .meta-data {
        background: linear-gradient(45deg, #5d4157, #a8caba);
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

.session-a { border-color: var(--color3); }
.session-b { border-color: var(--color2); }

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
  background-color: #5d4157;
  color: white;
}

.session-b .arrow-circle {
  background-color: #a8caba;
  color: white;
}

.card:hover {
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  transform: translateY(-3px);
  border-color: rgba(93, 65, 87, 0.8); /* Slightly intensify the border colour */
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
Programme for the [pre-conference workshops](#parallel-workshops) on [Tuesday](#tuesday), 9th December 2025, and the main conference days on [Wednesday](#wednesday), [Thursday](#thursday), and [Friday](#friday), 10th-12th December 2025. 

The main venue address of CHR2025 is *University of Luxembourg, Belval Campus, 2 place de l’Université, L-4365 Esch-sur-Alzette, Luxembourg*. See [*Finding the Venue*](/venue/location-and-venue). 

<div style="padding: 15px; background-color: #fff3cd; border-left: 5px solid #ffc107; margin: 20px 0;">
  <strong>⚠️ Warning:</strong> This content is currently under revision.
</div>

<!-- DAYS -->
<div class="tabset">

  <!-- button creation -->
  <!-- TUE -->
  <input type="radio" name="tabset" id="tuesday" aria-controls="tuesday">
  <label for="tuesday">Tuesday</label>
  <!-- WED -->
  <input type="radio" name="tabset" id="wednesday" aria-controls="wednesday" checked>
  <label for="wednesday">Wednesday</label>
  <!--   THUR -->
  <input type="radio" name="tabset" id="thursday" aria-controls="thursday">
  <label for="thursday">Thursday</label>
  <!--FRI -->
  <input type="radio" name="tabset" id="friday" aria-controls="friday">
  <label for="friday">Friday</label>
   
  <!-- content -->
  <div class="tab-panels">
  <section id="tuesday" class="tab-panel" alt="tab showing the schedule for tuesday">
   <h2 id="overview-tue" alt="Overview of Tuesday" style="font-weight:bold;">Tuesday, December 9, 2025 (Pre-conference workshops)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:00 - 16:00</td>
            <td>
                <span class="highlight">Registration - Coffee</span>
                <div class="location">
                    MSA 0342090 A-B<br>
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:30 - 13:00</td>
            <td>
                <span class="highlight">Workshop sessions</span>
                <div class="location">
                    <a href="/workshops/#workshop-1">Workshop 1 (morning session)</a>: 3.330 <br>
                    <a href="/workshops/#workshop-2">Workshop 2 (morning session)</a>: 3.010<br>
                    <a href="/workshops/#workshop-3">Workshop 3 (morning-only session)</a>: 3.390
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:00 - 14:00</td>
            <td>
                Lunch Break: MSA 0342090 A-B
            </td>
        </tr>
        <tr>
            <td class="time">14:30 - 17:00</td>
            <td>
                <span class="highlight">Workshop sessions</span>
                <div class="location">
                    <a href="/workshops/#workshop-1">Workshop 1 (afternoon session)</a>: 3.330 <br>
                    <a href="/workshops/#workshop-2">Workshop 2 (afternoon session)</a>: 3.010<br>
                </div>
            </td>
        </tr>
    </table>
  </section>
  <!-- WED -->
    <section id="wednesday" class="tab-panel" alt="tab showing the schedule for wednesday">
    <h2 id="overview-wed" alt="Overview of Wednesday" style="font-weight:bold;">Wednesday, December 10, 2025 (Day 1)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:30 - 16:00</td>
            <td>
                Registration
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">08:30 - 09:30</td>
            <td>
                Coffee & croissants
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:30 - 10:30</td>
            <td>
                <span class="highlight">Welcome by the LO
                Opening by the President of the CHR
                Address by the Program Committee</span>
                <div class="location">
                    3.500
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:30 - 11:00</td>
            <td>
                Coffee Break
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">11:00 - 12:30</td>
            <td>
                <span class="highlight"><a href="#session1A">Session 1A</a> / <a href="#session1B">Session 1B</a></span>
                <div class="location">
                    3.530 / 3.330
                </div>
            </td>
        </tr>
         <tr>
            <td class="time">12:30 - 13:30</td>
            <td>
                Lunch Break
                <div class="location">
                MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:30 - 15:00</td>
            <td>
                <span class="highlight"><a href="#session2A">Session 2A</a> / <a href="#session2B">Session 2B</a></span>
                <div class="location">
                    3.530 / 3.330
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:00 - 15:30</td>
            <td>
                Coffee Break
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:30 - 16:45</td>
            <td>
                <span class="highlight"><a href="/news/keynote-speakers/">Keynote 1: Miguel Escobar Varela</a></span>
                <div class="location">
                3.500
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">16:45</td>
            <td>
                Cocktail reception 
                <div class="location">
                MSA 0342090 A-B + A-A
                </div>
            </td>
        </tr>
    </table>



<!-- session heading -->
<h2 id="session1" style="font-weight:bold; font-size:1.8em;">Session 1</h2>
<!-- Session 1A -->
<div class="session-block session-a">
<h3 id="session1A" alt="Session 1A: narrative, perception, and readership (11:00-12:30)">Session 1A: narrative, perception, and readership (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">"Crying like a Baby": Survival Analysis and the Multimodal Memory of Holocaust Survivors<span class="paper-type">(long)</span><span class="paper-authors">Gabor Mihaly Toth, Mohamed Laib, Cedric Pruski, Marcos da Silveira, Marcus Ma, Shrikanth Narayanan and Alina Bothe</span></p>
<p class="paper-entry">Llamas Don't Understand Fiction: Application and Evaluation of Large Language Models for Knowledge Extraction from Short Stories in English<span class="paper-type">(long)</span><span class="paper-authors">Arianna Graciotti, Franziska Pannach, Valentina Presutti
 and Federico Pianzola</span></p>
<p class="paper-entry">Echoes of Antiquity: Towards Understanding History through
 Human and LLM-Based Classical Text Translations<span class="paper-type">(short)</span><span class="paper-authors">Phillip Benjamin Ströbel and Felix K. Maier</span></p>
<p class="paper-entry">Causal Effect of Character Gender on Readers' Preferences<span class="paper-type">(short)</span><span class="paper-authors">Federica Bologna, Ian Lundberg and Matthew Wilkens</span></p>
</div>
      <!-- Session 1B -->
<div class="session-block session-b">
<h3 id="session1B" alt="Session 1B: Networks of knowledge (11:00-12:30)">Session 1B: Networks of knowledge (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>
<p class="paper-entry">Patterns of Canon: A Multilingual Network Study<span class="paper-type">(long)</span><span class="paper-authors">Judith Brottrager, Jean Barré, Yuri Bizzoni and Pascale
 Feldkamp Moreira</span></p>
<p class="paper-entry">Reading Beyond the Center. Modeling Book Encounters in the
 Danish Periphery (1800-1850)<span class="paper-type">(long)</span><span class="paper-authors">Alie Lassche, Rie Schmidt Eriksen, Pascale Feldkamp, Johan
 Heinsen, Katrine Baunvig and Kristoffer Nielbo</span></p>
<p class="paper-entry">Cluster ambiguity in networks as substantive knowledge<span class="paper-type">(short)</span><span class="paper-authors">Mathieu Jacomy, Tommaso Elli, Andrea Benedetti, Guillaume
 Plique, Benjamin Ooghe-Tabanou, Paul Girard and Alexis
 Jacomy</span></p>
<p class="paper-entry">Bridging Semantics and Structure: a Typed Prosopographical
 Network \of Maximilian I's Court<span class="paper-type">(short)</span><span class="paper-authors">Marcella Tambuscio and Georg Vogeler</span></p>
<p class="paper-entry">“Works on My Machine”: A Case Study of Replicability
 Challenges in Computational Humanities Research<span class="paper-type">(short)</span><span class="paper-authors">Viktor J. Illmer</span></p>

</div>
<!-- session heading -->
<h2 id="session2" style="font-weight:bold; font-size:1.8em;">Session 2</h2>
<!-- Session 2A -->
<div class="session-block session-a">
<h3 id="session2A" alt="Session 2A: stylometry and philology (13:30-15:00)">Session 2A: stylometry and philology (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">Wauchier, Is That You? A multi-manuscript authorship
 analysis of Saint Lambert's life<span class="paper-type">(long)</span><span class="paper-authors">Thibault Clérice and Ariane Pinche</span></p>
<p class="paper-entry">The One and Only? Authorship Verification on Jan van Boendale and the Middle Dutch Antwerp School<span class="paper-type">(long)</span><span class="paper-authors">Caroline Vandyck</span></p>
<p class="paper-entry">From a Computer-Assisted Stemma to a Phylogenetic Tree: The
 Medieval Dutch Martijn Trilogy by Jacob van Maerlant<span class="paper-type">(long)</span><span class="paper-authors">Sofie Moors and Joey McCollum</span></p>
<p class="paper-entry">Biblicality of Early Medieval Canon Law through the Lens of
 Language Modeling<span class="paper-type">(long)</span><span class="paper-authors">Friederike Voit, Gleb Schmidt and Sven Meeder</span></p>
</div>
      <!-- Session 2B -->
<div class="session-block session-b">
<h3 id="session2B" alt="Session 2B: audio, video and visual data (13:30-15:00)">Session 2B: audio, video and visual data (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">Podcasts as Data: Building a Dataset for Large-Scale Audio
 Content Analysis<span class="paper-type">(long)</span><span class="paper-authors">Loren Verreyen</span></p>
<p class="paper-entry">Sitcom Form and Function: Pacing and Production in a
 Collection of Thirty U.S. Series<span class="paper-type">(long)</span><span class="paper-authors">Lauren Tilton and Taylor Arnold</span></p>
<p class="paper-entry">Quantifying Archival Silences: Phylogenetic Diversity
 Analysis of Controlled Vocabulary Utilization<span class="paper-type">(long)</span><span class="paper-authors">Melvin Wevers, Thomas Smits and Folgert Karsdorp</span></p>
<p class="paper-entry">Heritage Weaver: Classifying, Searching, and Linking Museum
 Data with Multimodal AI<span class="paper-type">(long)</span><span class="paper-authors">Kaspar Beelen and Natasha Kitcher</span></p>
</div>
    </section>
  <!-- THUR -->
    <section id="thursday" class="tab-panel" alt="tab showing the schedule for thursday">
    <h2 id="overview-thu" alt="Overview of Thursday" style="font-weight:bold;">Thursday, December 11, 2025 (Day 2) </h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:30 - 16:00</td>
            <td>
                Registration
                <div class="location">
                   MSA 0342090 A-B 
                </div>
            </td>
        </tr>
         <tr>
            <td class="time">08:00 - 09:00</td>
            <td>
                Coffee & croissants
                <div class="location">
                   MSA 0342090 A-B 
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:00 - 10:30</td>
            <td>
                <span class=highlight><a href="#lightningtalks">Lightning Talks</a></span>
                <div class="location">
                    3.530
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:30 - 11:00</td>
            <td>
                Coffee break
                <div class="location">
                   MSA 0342090 A-B 
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">11:00 - 12:30</td>
            <td>
                <span class="highlight"><a href="#session3A">Session 3A</a> / <a href="#session3B">Session 3B</a></span>
                <div class="location">
                    3.530 / 3.330
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:30 - 13:30</td>
            <td>
                Lunch Break
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:30 - 15:00</td>
            <td>
                <span class="highlight"><a href="#session4A">Session 4A</a> / <a href="#session4B">Session 4B</a></span>
                <div class="location">
                    3.540 / 3.330
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:00 - 15:30</td>
            <td>
                Coffee break
                <div class="location">
                   MSA 0342090 A-B 
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:30 - 17:00</td>
            <td>
                <span class="highlight"><a href="#session5A">Session 5A</a> / <a href="#session5B">Session 5B</a></span>
                <div class="location">
                    3.540 / 3.330
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">17:00 - 18:00</td>
            <td>
                <span class="highlight">Poster walk-around</span>
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">20:00</td>
            <td>
                Social event
                <div class="location">
                    <a href="/venue/conference-social-event/">Venue to be confirmed</a>
                </div>
            </td>
        </tr>
    </table>

<!-- sessions overview -->
<h3 style="font-weight:bold; font-size:2.3em;">Detailed View</h3>
<!-- session heading -->
      <h2 id="session3" style="font-weight:bold; font-size:1.8em;">Session 3</h2>
<!-- Session 3A -->
<div class="session-block session-a">
<h3 id="session3A" alt="Session 3A: images (11:00-12:30)">Session 3A: images (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">Castles, Battlefields, and Continents: A Dataset of Maps
 from Literature<span class="paper-type">(long)</span><span class="paper-authors">Axel Bax, David Mimno and Matthew Wilkens</span></p>
<p class="paper-entry">The Illustrated Page: Analyzing Illustrations of Historical
 Childrens Books Using Citizen Science<span class="paper-type">(long)</span><span class="paper-authors">Andrew Piper, Jiaming Jiang and Robert Budac</span></p>
<p class="paper-entry">Vision Language Models for Novel Art Therapy Evaluation in
 Schizophrenia<span class="paper-type">(short)</span><span class="paper-authors">Ivan Nenchev, Karin Dannecker, Maren Rabe, Marie Jeschke
 and Christiane Montag</span></p>
<p class="paper-entry">Framing the Canon: A Computational Study of Canonicity in
 Danish Golden Age Paintings (1750-1870)<span class="paper-type">(short)</span><span class="paper-authors">Louise Brix Pilegaard Hansen, Rie Schmidt Eriksen, Pascale
 Feldkamp, Alie Lassche, Kristoffer Laigaard Nielbo, Katrine
 Frøkjær Baunvig and Yuri Bizzoni</span></p>
<p class="paper-entry">Classification of Script Types and Modes for Medieval
 Hebrew Manuscripts<span class="paper-type">(short)</span><span class="paper-authors">Daria Vasyutinsky Shapira, Irina Rabaev, Jihad El-Sana and
 Ophir Muenz-Manor</span></p>
</div>
      <!-- Session 3B -->
<div class="session-block session-b">
<h3 id="session3B" alt="Session 3B: LLMs and content mining (11:00-12:30)">Session 3B: LLMs and content mining (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span
class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">The Learnability Hierarchy of News Values: What Makes Some
 Journalistic Concepts Harder to Classify?<span class="paper-type">(long)</span><span class="paper-authors">Elisabeth Muth Andersen</span></p>
<p class="paper-entry">Between Woolf and Homer: An Explorative Approach to Intertextuality Detection using Large Language Models<span class="paper-type">(long)</span><span class="paper-authors">Nicolas Werner and Nils Reiter</span></p>
<p class="paper-entry">Identifying stance-bearing keywords in public debates with
 instruction-tuned language models<span class="paper-type">(short)</span><span class="paper-authors">Milena Belosevic</span></p>
<p class="paper-entry">Scalable Verb-Based Literary Semantics<span class="paper-type">(short)</span><span class="paper-authors">Hans Ole Hatzel, Haimo Stiemer, Evelyn Gius and Chris
 Biemann</span></p>
<p class="paper-entry">Continuous sentiment scores for literary and multilingual
 contexts<span class="paper-type">(short)</span><span class="paper-authors">Laurits Wieslander Lyngbæk, Pascale Feldkamp, Yuri Bizzoni,
 Kristoffer Nielbo and Kenneth Enevoldsen</span></p>

</div>
<!-- session heading -->
<h2 id="session4" style="font-weight:bold; font-size:1.8em;">Session 4</h2>
      <!-- Session 4A -->
<div class="session-block session-a">
<h3 id="session4A" alt="Session 4A: Ancient World (13:30-15:00)">Session 4A: Ancient World (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.540</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">Embedded in the Labyrinth: Investigating Latin Word Senses
 through Transformer-Based Contextual Embeddings and
 Attention<span class="paper-type">(long)</span><span class="paper-authors">Vojtěch Kaše, Sarah Lang and Petr Pavlas</span></p>
<p class="paper-entry">Semantic Search for Ancient Inscriptions<span class="paper-type">(long)</span><span class="paper-authors">Micah Tongen, Sara Sprenkle, Rebecca Benefiel and Trevor
 Stalnaker</span></p>
<p class="paper-entry">Towards a Computational Study of Ancient Greek Rhyme<span class="paper-type">(long)</span><span class="paper-authors">Keith Begley and Leon Wash</span></p>
<p class="paper-entry">Automatic Named Entity Linking for Ancient Greek with a
 Domain-Specific Knowledge Base<span class="paper-type">(long)</span><span class="paper-authors">Marijke Beersmans, Evelien de Graaf, Alek Keersmaekers,
 Mark Depauw, Tim Van de Cruys and Margherita Fantoli </span></p>


</div>
      <!-- Session 4B -->
<div class="session-block session-b">
<h3 id="session4B" alt="Session 4B: modelling culture (13:30-15:00)">Session 4B: modelling culture(13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span><span class="meta-section"></span></div>
<p class="paper-entry">The Rest is Silence: Leveraging Unseen Species Models for
 Computational Musicology<span class="paper-type">(long)</span><span class="paper-authors">Fabian C. Moss, Jan Hajič Jr., Adrian Nachtwey and Laurent
 Pugin</span></p>
<p class="paper-entry">Cultural Collapse: Toward a generative formalism for AI
 cultural production<span class="paper-type">(long)</span><span class="paper-authors">Ryan Heuser</span></p>
<p class="paper-entry">Transmission and Survival of Iberian Patristic Texts
 (3rd–5th Centuries)<span class="paper-type">(long)</span><span class="paper-authors">Émilie Guidi, Théo Moins and Jean-Baptiste Camps</span></p>
<p class="paper-entry">Robust Modelling of Ordinal Survey Data Using Probabilistic Programming<span class="paper-type">(long)</span><span class="paper-authors">Aleksi Lahtinen, James Edwards, Marc Calmbach, Isabella
 Tautscher and Leo Lahti</span></p>

</div>
<!-- session heading -->
<h2 id="session5" style="font-weight:bold; font-size:1.8em;">Session 5</h2>
<!-- Session 5A -->
<div class="session-block session-a">
<h3 id="session5A" alt="Session 5A: modelling culture (15:30-17:00)">Session 5A: modelling culture(15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.540</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>
<p class="paper-entry">Global Beats, Local Tongue: Studying Code Switching in
 K-pop Hits on Billboard Charts<span class="paper-type">(long)</span><span class="paper-authors">Aditya Narayan Sankaran, Reza Farahbakhsh and Noel Crespi</span></p>
<p class="paper-entry">Linguistic tools in musical stylometry<span class="paper-type">(long)</span><span class="paper-authors">Kirill Abrosimov, Alexander Grebennikov, George Tzanetakis
 and Anna Sidorova</span></p>
<p class="paper-entry">Global Linguistic Diversity - Adapting the Leinster-Cobbold
 Framework from Ecology for Humanities Research<span class="paper-type">(long)</span><span class="paper-authors">Hannes Essfors</span></p>
<p class="paper-entry">Estranged Predictions: Measuring Semantic Category
 Disruption with Masked Language Modelling<span class="paper-type">(long)</span><span class="paper-authors">Yuxuan Liu, Haim Dubossarsky and Ruth Ahnert</span></p>


</div>
<!-- Session 5B -->
<div class="session-block session-b">
<h3 id="session5B" alt="Session 5B: rhetoric, representation, and interpretation (15:30-17:00)">Session 5B: rhetoric, representation, and interpretation (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>
<p class="paper-entry">Characterizing Religious Rhetoric in the U.S. Congressional
 Record<span class="paper-type">(long)</span><span class="paper-authors">Lavinia Dunagan and Dallas Card</span></p>
<p class="paper-entry">Interrogating Racism in the Medical Literature Using Word
 Embeddings<span class="paper-type">(long)</span><span class="paper-authors">Lauren Liao, Sajia Darwish, Caroline Figueroa, Erin
 Manalo-Pedro, Swetha Pola, Maithili Jha, Fernando De Maio,
 Claudia von Vacano, Chris Kennedy and Pratik Sachdeva</span></p>
<p class="paper-entry">Building Historical Corpora with Multimodal LLMs: Epistemic
 Gaps and Misreadings in 18th-Century Russian Books<span class="paper-type">(long)</span><span class="paper-authors">Maria Levchenko</span></p>
<p class="paper-entry">Says Who? Effective Zero-Shot Annotation of Focalization<span class="paper-type">(long)</span><span class="paper-authors">Rebecca M. M. Hicke, Yuri Bizzoni, Pascale Feldkamp and
 Ross Deans Kristensen-McLachlan</span></p>
</div>

<!-- Session Lightning Talks -->
<div class="session-block alt-session">
<h3 id="lightningtalks" alt="Lightning Talks (9:00-10:30)">Lightning Talks (9:00-10:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: Taylor Arnold</span></div>
<p class="paper-entry"><span class="paper-title">Archipelagic Visualizations: Mapping Imperial Space in 19th-Century Travel Writing Using Voyant Tools</span><span class="paper-authors">Steffen Wöll</span></p>
<p class="paper-entry"><span class="paper-title">Bringing together close reading questions and distant reading methods in the analysis of archived web</span><span class="paper-authors">Victor Harbo Johnston, Helle Strandgaard Jensen and Sasch Berg Bogebjerg</span></p>
<p class="paper-entry"><span class="paper-title">Einstein AI: Contextual Retrieval from the Collected Papers of Albert Einstein Using RAG and GraphRAG Architectures</span><span class="paper-authors">Florin-Stefan Morar</span></p>
<p class="paper-entry"><span class="paper-title">Modeling Intertextuality: An Ontological Framework for Literary Studies</span><span class="paper-authors">Laura Untner</span></p>
<p class="paper-entry"><span class="paper-title">Bayesian inference of sex-specific mortality profiles and product yields from unsexed cattle zooarchaeological remains</span><span class="paper-authors">Mark Thomas</span></p>
<p class="paper-entry"><span class="paper-title">Does culture evolve “one funeral at a time”?</span><span class="paper-authors">Oleg Sobchuk, Jean Barré, Marijn Koolen, Harin Lee and Bret Beheim</span></p>
<p class="paper-entry"><span class="paper-title">Automating the Study of Digital Literary Memory: A Multilingual LLM Pipeline for Wikipedia-Based Cultural Analysis</span><span class="paper-authors">Botond Szemes</span></p>
<p class="paper-entry"><span class="paper-title">Measuring the Synchronicity of Historical European Parliamentary Discourse, 1949-2018</span><span class="paper-authors">Ruben Ros and Risto Turunen</span></p>
<p class="paper-entry"><span class="paper-title">Disorder or (self-)murder? Making sense of suicide in 19th-century British newspapers</span><span class="paper-authors">Nilo Pedrazzini and Daniel Wilson </span></p>
<p class="paper-entry"><span class="paper-title">Mapping Literary Networks through Epigraphs</span><span class="paper-authors">Tomás Espino Barrera</span></p>
<p class="paper-entry"><span class="paper-title">Low-Cost Synthetic Data Generation for HTR Training: Evaluating a Multimodal Strategy for Historical Manuscript Processing</span><span class="paper-authors">Serena Carlamaria Crespi and Carlos-Emiliano González-Gallardo</span></p>
<p class="paper-entry"><span class="paper-title">Quill2Vec: A Tool for Vector Manipulation of Medieval Latin Script</span><span class="paper-authors">Mart Herman Gerrit Makkink</span></p>
<p class="paper-entry"><span class="paper-title">A Diachronic Analysis of Cinematic Trends and Their Reception</span><span class="paper-authors">Jan Tvrz</span></p>
<p class="paper-entry"><span class="paper-title">Beyond the Statistics: Migration to a Kyiv Suburb through the Lens of the 1897 Census</span><span class="paper-authors">Konstantin Mogarichev, Tetiana Shyshkina and Maria Volkova</span></p>
<p class="paper-entry"><span class="paper-title">Speculative Reconstruction and the Ethics of the Fragment: Early Experiments with Generative AI in Art History</span><span class="paper-authors">Katarina Mohar</span></p>
<p class="paper-entry"><span class="paper-title">Building Better Speculative Fiction Datasets with ISFDB</span><span class="paper-authors">Laure Thompson</span></p>
<p class="paper-entry"><span class="paper-title">Leveraging Artificial Intelligence to Promote Scientific Heritage</span><span class="paper-authors">Mikhail Biriuchinskii, Floriane Chiffoleau, Motasem Alrahabi, Glenn Roe, Frédérick Gay and Clément Castellon</span></p>
<p class="paper-entry"><span class="paper-title">Digital Genre Boundaries: Network Backbone Analysis of Steam's User-Generated Classification System</span><span class="paper-authors">Nabeel Siddiqui</span></p>
<p class="paper-entry"><span class="paper-title">Application of T-projection to Fictional Direct Speech Annotation Transfer</span><span class="paper-authors">Anastasia Goppen, Murad Mustafaev and Olga Shablykina</span></p>
<p class="paper-entry"><span class="paper-title">When Larger LLMs Aren’t Enough: Word Segmentation in Historical Chinese Texts</span><span class="paper-authors">Hao Tan</span></p>
<p class="paper-entry"><span class="paper-title">Towards animal-centric affective analysis in poetry</span><span class="paper-authors">Thomas Haider</span></p>
<p class="paper-entry"><span class="paper-title">Neighbourhood Walks: A New Semantic Topology for Historical Map Text</span><span class="paper-authors">Katherine McDonough, Kaspar Beelen and Daniel C. S. Wilson</span></p>
<p class="paper-entry"><span class="paper-title">"Where Empires End: Tracing the Geography of a “Soaring Spirit” in Poetry</span><span class="paper-authors">Antonina Martynenko, Artjoms Šeļa and Petr Plecháč</span></p>
<p class="paper-entry"><span class="paper-title">Rapid cultural analytics using LLMs: a case of dreams</span><span class="paper-authors">Andres Karjus</span></p>

</div>
    </section>
    <!-- FRI -->
    <section id="friday" class="tab-panel" alt="tab showing the schedule for friday">
      <h2 id="overview-fri" alt="Overview of Friday" style="font-weight:bold;">Friday, December 12, 2025 (DAY 3)</h2>
    <table class="schedule-table">
        <tr>
            <td class="time">08:00 - 09:00</td>
            <td>
                Coffee & croissants
                <div class="location">
                   MSA 0342090 A-B 
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">09:00 - 10:00</td>
            <td>
                <span class="highlight"><a href="/news/keynote-speakers/">Keynote 2: Els Lefever</a></span>
                <div class="location">
                     3.500
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:00 - 10:30</td>
            <td>
                Coffee break
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">10:30 - 12:00</td>
            <td>
                <span class="highlight"><a href="#session6A">Session 6A</a> / <a href="#session6B">Session 6B</a></span>
                <div class="location">
                 3.330 / 3.530
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">12:00 - 13:00</td>
            <td>
                Lunch
                <div class="location">
                    MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">13:00 - 14:30</td>
            <td>
                <span class="highlight"><a href="#session7A">Session 7A</a> / <a href="#session7B">Session 7B</a></span>
                <div class="location">
                  3.330 / 3.530
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">14:30 - 15:00</td>
            <td>
                Coffee break
                <div class="location">
                 MSA 0342090 A-B
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">15:00 - 16:30</td>
            <td>
                <span class="highlight"><a href="#session8A">Session 8A</a> / <a href="#session8B">Session 8B</a></span>
                <div class="location">
                  3.330 / 3.530
                </div>
            </td>
        </tr>
        <tr>
            <td class="time">16:30 - 18:00</td>
            <td>
                <span class="highlight">Best Paper Award Ceremony - Closing session (conclusion & farewell)</span>
                <div class="location">
                 3.500
                </div>
            </td>
        </tr>
    </table>


<!-- sessions overview -->
<h3 style="font-weight:bold; font-size:2.3em;">Detailed View</h3>

<!-- session heading -->
<h2 id="session6" style="font-weight:bold; font-size:1.8em;">Session 6</h2>
<!-- Session 6A -->
<div class="session-block session-a">
<h3 id="session6A" alt="Session 6A: narratology (10:30-12:00)">Session 6A: narratology (10:30-12:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">When the hero becomes a girl: Presenting characters’ gender
 with stereotypes in AO3 gender-bending fanfiction<span class="paper-type">(long)</span><span class="paper-authors">Yixi Chen and Jianwei Yan</span></p>
<p class="paper-entry">Happily Ever After: Comparing Sentiment Arcs in
 Emotionally-Inflected Fanfiction Genres Across Fandoms<span class="paper-type">(long)</span><span class="paper-authors">Julia Neugarten, Mia Jacobsen, Pascale Feldkamp and Yuri
 Bizzoni</span></p>
<p class="paper-entry">EmoTracker - A New Framework for Modeling and Forecasting
 Diachronic Emotion Dynamic<span class="paper-type">(long)</span><span class="paper-authors">Max Tiessler, Quim Motger, Florina Piroi and Andreas Baumann</span></p>
<p class="paper-entry">Measuring the Stories in Contemporary Songs<span class="paper-type">(long)</span><span class="paper-authors">David Bamman, Sabrina Baur, Mackenzie Hanh Cramer, Anna Ho
 and Tom McEnaney</span></p>


</div>
<!-- Session 6B -->
<div class="session-block session-b">
<h3 id="session6B" alt="Session 6B: mapping meaning (10:30-12:00)">Session 6B: mapping meaning  (10:30-12:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>


<p class="paper-entry">Text, Terrain, and Algorithms: Searching for Al-Idrisi’s 
 Aqranus with Formal Methods<span class="paper-type">(long)</span><span class="paper-authors">Angel Grigorov and Adela Sobotkova</span></p>
<p class="paper-entry">Mapping News Geography: A Computational Framework for
 Classifying Local Media Through Geographic Coverage Patterns<span class="paper-type">(long)</span><span class="paper-authors">Simona Bisiani, Agnes Gulyas and Bahareh Heravi</span></p>
<p class="paper-entry">Mind the Language Gap in Digital Humanities: LLM-Aided
 Translation of SKOS Thesaur<span class="paper-type">(long)</span><span class="paper-authors">Felix Kraus, Nicolas Blumenröhr, Danah Tonne and Achim
 Streit</span></p>
<p class="paper-entry">Producing Structured Data from Historical Sources: a
 Preliminary Application to French Senate Tables<span class="paper-type">(long)</span><span class="paper-authors">Joël Féral, Joseph Chazalon and Marie Puren</span></p>

</div>
<!-- session heading -->
<h2 id="session7" style="font-weight:bold; font-size:1.8em;">Session 7</h2>
<!-- Session 7A -->
<div class="session-block session-a">
<h3 id="session7A" alt="Session 7A: NER (13:00-14:30)">Session 7A: NER (13:00-14:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">QalamNER: An LLM-based NER Dataset Curation, Annotation and
 Evaluation in Historical Urdu Elegies<span class="paper-type">(long)</span><span class="paper-authors">Saniya Irfan and Syed Juned Ali</span></p>
<p class="paper-entry">From Raw Text to Meaningful Information: Named Entity
 Recognition, Disambiguation, and Semantic Enrichment of a
 Large Corpus of Historical Police Records (Antwerp,
 1876–1945)<span class="paper-type">(long)</span><span class="paper-authors">Lith Lefranc</span></p>
<p class="paper-entry">Fine-grained Named-Entity Recognition for the East-India
 Company domain<span class="paper-type">(long)</span><span class="paper-authors">Sophie Arnoult, Brecht Nijman and Leon van Wissen</span></p>
<p class="paper-entry">Towards Comparable Historical NER: Building a Shared
 Evaluation Corpus for 18th-Century Historical Texts<span class="paper-type">(long)</span><span class="paper-authors">Lu Liu, Andreas Vlachidis, Adam Crymble, Marco Humbel and
 Deborah Lee</span></p>


</div>
<!-- Session 7B -->
<div class="session-block session-b">
<h3 id="session7B" alt="Session 7B: computational literary studies (13:00-14:30)">Session 7B: computational literary studies (13:00-14:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">Modeling the Construction of a Literary Archetype: The Case
 of the Detective Figure in French Literature<span class="paper-type">(long)</span><span class="paper-authors">Jean Barré, Olga Seminck, Antoine Bourgois and Thierry
 Poibeau</span></p>
<p class="paper-entry">Zero-shot Methods for Historical Text Restoration<span class="paper-type">(long)</span><span class="paper-authors">Kiara M.H. Liu, Martin Mueller and Matthew Wilkens</span></p>
<p class="paper-entry">Are You There God? Lightweight Narrative Annotation of
 Christian Fiction with LMs<span class="paper-type">(long)</span><span class="paper-authors">Rebecca M. M. Hicke, Brian Haggard, Mia Ferrante, Rayhan
 Khanna and David Mimno</span></p>
<p class="paper-entry">Computing the Formal and Institutional Boundaries of
 Contemporary Genre and Literary Fiction<span class="paper-type">(long)</span><span class="paper-authors">Natasha Johnson</span></p>
</div>
<!-- session heading -->
<h2 id="session8" style="font-weight:bold; font-size:1.8em;">Session 8</h2>
<!-- Session 8A -->
<div class="session-block session-a">
<h3 id="session8A" alt="Session 8A: computational literary studies (15:00-16:15)">Session 8A: computational literary studies (15:00-16:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>


<p class="paper-entry">Was Poetry Graded Validly?: Text Mining Shipin, a
 Sixth-Century Chinese Work of Literary Criticism<span class="paper-type">(short)</span><span class="paper-authors">Wenyi Shang and Emily Xueyue Liu</span></p>
<p class="paper-entry">Detecting ``Parasitic Poems'': Quantifying Poetic Style in
 Late Imperial Chinese Fiction<span class="paper-type">(short)</span><span class="paper-authors">Jiayu Liu, Rongqian Ma and Keli Du</span></p>
<p class="paper-entry">How are Literary Histories written? An LLM-based Analysis
 of Objects and Perspectives in German Literary History<span class="paper-type">(short)</span><span class="paper-authors">Evelyn Gius, Stefanie Messner and Axel Pichler</span></p>
<p class="paper-entry">Changing Attitudes Toward Animals in Early Modern Dutch
 Literature<span class="paper-type">(short)</span><span class="paper-authors">Arjan van Dalfsen</span></p>
<p class="paper-entry">Authorial Filtering and Computational Models: A Dynamic
 Analysis of Umberto Eco’s Foucault’s Pendulum through a
 Fluid-Dynamics-Inspired Framework<span class="paper-type">(short)</span><span class="paper-authors">Lorenzo Zangari, Davide Picca and Riccardo Fedriga</span></p>
<p class="paper-entry">More Sound, More Soundness? Improving authorship
 attribution with phonemes<span class="paper-type">(short)</span><span class="paper-authors">Simon Gabay, Jean-Luc Falcone and Florian Cafiero</span></p>
</div>
      <!-- Session 8B -->

<div class="session-block session-b">
<h3 id="session8B" alt="Session 8B: information retrieval (15:00-16:15)">Session 8B: information retrieval (15:00-16:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>


<p class="paper-entry">Seeing History Unseen: Evaluating Vision-Language Models
 for WCAG-Compliant Alt-Text in Digital Heritage Collections<span class="paper-type">(short)</span><span class="paper-authors">Moritz Mähr and Moritz Twente</span></p>
<p class="paper-entry">Towards a NAvigator Tool for Dutch Verbaal-Archives:
 Leveraging Nineteenth-Century Archival Logic for Keyword
 Search<span class="paper-type">(short)</span><span class="paper-authors">Sebastiaan Peeters, Christel Annemieke Romein and Andreas
 Weber</span></p>
<p class="paper-entry">Evaluation of Large Language Models on hierarchical entity
 matching for cultural heritage data<span class="paper-type">(short)</span><span class="paper-authors">Bram Bakker and Iris Hendrickx</span></p>
<p class="paper-entry">Benchmarking Multimodal Large Language Models in Zero-shot
 and Few-shot Scenarios: preliminary results on studying
 Christian Iconography<span class="paper-type">(short)</span><span class="paper-authors">Gianmarco Spinaci, Lukas Klic and Giovanni Colavizza</span></p>
<p class="paper-entry">Classifying Name-Date and Year Figures in Mixtec Codices<span class="paper-type">(short)</span><span class="paper-authors">Girish Salunke, Christopher Driggers-Ellis and Christan
 Grant</span></p>
<p class="paper-entry">A Visualization of Word and Document Embeddings <span class="paper-type">(short)</span><span class="paper-authors">Joseph Chataignon and Tobias Hodel</span></p>
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




