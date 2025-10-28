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
  <!--FRI 
  <input type="radio" name="tabset" id="friday" aria-controls="friday">
  <label for="friday">Friday</label>
   -->
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
                <span class="highlight">Address by Andreas Fickers, Director of the C²DH -
<a href="/news/keynote-speakers/">Keynote 1</a></span>
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
<h3 id="session1A" alt="Session 1A: perception and readership (11:00-12:30)">Session 1A: perception and readership (11:00-12:30)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.530</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>

<p class="paper-entry">"Crying like a Baby": Survival Analysis and the Multimodal Memory of Holocaust Survivors<span class="paper-type">(long)</span><span class="paper-authors">Gabor Mihaly Toth, Mohamed Laib, Cedric Pruski, Marcos da Silveira, Marcus Ma, Shrikanth Narayanan and Alina Bothe</span></p>
<p class="paper-entry">Llamas Don't Understand Fiction: Application and Evaluation of Large Language Models for Knowledge Extraction from Short Stories in English<span class="paper-type">(long)</span><span class="paper-authors">Arianna Graciotti, Franziska Pannach, Valentina Presutti
 and Federico Pianzola</span></p>
<p class="paper-entry">Echoes of Emotion: Linking Narrative and Reader Response of
 Web Novels in Chinese and English<span class="paper-type">(short)</span><span class="paper-authors">Ze Yu and Federico Pianzola</span></p>
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
<p class="paper-entry">From the Antwerp School to the Antwerp Cluster? Authorship
 Verification in Fourteenth Century Middle Dutch Texts<span class="paper-type">(short)</span><span class="paper-authors">Caroline Vandyck</span></p>
<p class="paper-entry">From a Computer-Assisted Stemma to a Phylogenetic Tree: The
 Medieval Dutch Martijn Trilogy by Jacob van Maerlant<span class="paper-type">(long)</span><span class="paper-authors">Sofie Moors and Joey McCollum</span></p>
<p class="paper-entry">Zero-shot Methods for Historical Text Restoration<span class="paper-type">(long)</span><span class="paper-authors">Kiara M.H. Liu, Martin Mueller and Matthew Wilkens</span></p>
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
            <td class="time">09:30 - 10:30</td>
            <td>
                <span class=highlight>Lightning Talks</span>
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
                    <a href="/venue/conference-social-event/">Big Beer Company</a>
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
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span></div>

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
<h3 id="session4B" alt="Session 4B: modelling (13:30-15:00)">Session 4B: modelling (13:30-15:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.330</span><span class="meta-section">Chair: NOT YET DEFINED</span><span class="meta-section"></span></div>
<p class="paper-entry">The Rest is Silence: Leveraging Unseen Species Models for
 Computational Musicology<span class="paper-type">(long)</span><span class="paper-authors">Fabian C. Moss, Jan Hajič Jr., Adrian Nachtwey and Laurent
 Pugin</span></p>
<p class="paper-entry">Cultural Collapse: Toward a generative formalism for AI
 cultural production<span class="paper-type">(long)</span><span class="paper-authors">Ryan Heuser</span></p>
<p class="paper-entry">Transmission and Survival of Iberian Patristic Texts
 (3rd–5th Centuries)<span class="paper-type">(long)</span><span class="paper-authors">Émilie Guidi, Théo Moins and Jean-Baptiste Camps</span></p>
<p class="paper-entry">Probabilistic Modelling of Incomplete Ordinal Survey Data <span class="paper-type">(long)</span><span class="paper-authors">Aleksi Lahtinen, James Edwards, Marc Calmbach, Isabella
 Tautscher and Leo Lahti</span></p>

</div>
<!-- session heading -->
<h2 id="session5" style="font-weight:bold; font-size:1.8em;">Session 5</h2>
<!-- Session 5A -->
<div class="session-block session-a">
<h3 id="session5A" alt="Session 5A: modelling (15:30-17:00)">Session 5A: modelling (15:30-17:00)</h3>
<div class="meta-data bordered-layout"><span class="meta-section">Room: 3.540</span><span class="meta-section">Chair: NOT YET DEFINED</span></div>
<p class="paper-entry">Global Beats, Local Tongue: Studying Code Switching in
 K-pop Hits on Billboard Charts<span class="paper-type">(long)</span><span class="paper-authors">Aditya Narayan Sankaran, Reza Farahbakhsh and Noel Crespi</span></p>
<p class="paper-entry">Linguistic tools in musical stylometry<span class="paper-type">(long)</span><span class="paper-authors">Kirill Abrosimov, Alexander Grebennikov, George Tzanetakis
 and Anna Sidorova</span></p>
<p class="paper-entry">Global Linguistic Diversity - Adapting the Leinster-Cobbold
 Framework from Ecology for Humanities Research<span class="paper-type">(long)</span><span class="paper-authors">Kirill Abrosimov, Alexander Grebennikov, George Tzanetakis
 and Anna Sidorova</span></p>
<p class="paper-entry">Estranged Predictions: Measuring Semantic Category
 Disruption with Masked Language Modelling<span class="paper-type">(long)</span><span class="paper-authors">Yuxuan Liu, Haim Dubossarsky and Ruth Ahnert</span></p>


</div>
<!-- Session 5B -->
<div class="session-block session-b">
<h3 id="session5B" alt="Session 5B: world literature & llms (15:30-17:00)">Session 5B: world literature & llms(15:30-17:00)</h3>
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
    </section>
    <!-- FRI -->
    <section id="friday" class="tab-panel" alt="tab showing the schedule for friday">
      <h2 id="overview-fri" alt="Overview of Friday" style="font-weight:bold;">Friday, December 12, 2025 (DAY 3)</h2>
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




