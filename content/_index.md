---
title: 'CHR 2025'
date: 2025-08-12
---

<style>
  h1, h2 {
    margin-top: 1em; 
    margin-bottom: 0rem;
  }

  /* Card row layout */
  .card-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem; /* Small consistent gap */
    justify-content: center; /* Align cards to the left */
    align-items: stretch; /* Make sure all cards are the same height */
  }

  .card-col {
    display: flex;
    flex-grow:1;
    margin-bottom: 1rem; /* vertical margin between cards */
    max-width: 350px;
    width: 100%;
  }

  .card {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    
    border: 2px solid #ccc;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease; /* Adding a smooth hover effect */
  }

  .card.image img{
    width: 80% !important;

  }

  @media (hover: hover) {
    .card:hover {
      transform: translateY(-5px); /* Hover lift effect */
    }
  }

  .card-title {
    font-size: 20px !important; /* make size a bit bigger (override) */
    padding: 4px;
  }

  /* hide read more by default (on bigger screens) */
  .read-more {
  display: none;
  }

  /* show mobile read more since hover does not work */
  @media (hover: none) {
    .read-more {
      display: inline-block;
      margin-top: auto;
      align-self: flex-start;
      padding: 0.5rem 1rem;
      border: 1px solid;
      border-radius: 24px;
      text-decoration: none !important;
    }
  }

/* define banner for about page */
.banner-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 0px;
}
</style>

<h2 class="center"><b><span style="text-align:center";>Sixth Conference on</br> Computational Humanities Research</span></b></h2>

<h3 class="center">
    <b><span style="text-align:center; font-size:1.3em;"> <!-- make a little bigger than H3 -->
    December 9-12, 2025
    </span></b>
    </h3>

<div class="space" style="padding-top:0.5%;"></div>

The Computational Humanities Research (CHR) community is an international and
interdisciplinary community that supports researchers with an interest in computational
approaches to the humanities.

<div class="space" style="padding-top:0.5%;"></div>
<h3 style="max-width: 500px; margin: auto; text-align: center; padding: 0.5%">We are honored to have Miguel Escobar Varela and Els Lefever as our keynote speakers!</h3>

<div class="space" style="padding-top:0.5%;"></div>

The 2025 edition of the Computational Humanities Research conference will take
place on <b>December 9-12, 2025</b> at the Luxembourg Centre for Contemporary and Digital History (C²DH) at the University of Luxembourg.

Read more about CHR2025:

<div class="space" style="padding-top:0.5%;"></div>

<div class="banner-grid">
    <a href="/news/keynote-speakers" class="banner" aria-label="View Keynote Speakers">
        <h2>Keynote Speakers</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
    <a href="/cfp" class="banner" aria-label="View Call for Papers">
        <h2>Call for Papers</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
    <a href="/organization" class="banner" aria-label="View People">
        <h2>Organization</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
  <a href="/venue" class="banner" aria-label="View Venue">
        <h2>Venue</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
    <!--
    <a href="/programme" class="banner" aria-label="View Programme">
        <h2>Programme</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
    -->
</div>

<div class="space" style="padding-top:0.5%;"></div>
