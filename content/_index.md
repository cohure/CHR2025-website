---
title: "CHR 2025"
date: 2019-12-15T11:12:14+01:00
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

.banner {
    background-color: #002147;
    color: white;
    padding: 15px;  /* minimal padding */
    border-radius: 10px;
    display: flex;
    flex-direction: row; /* row to place arrow beside text */
    align-items: center;
    justify-content: space-between; /* space between text and arrow */
    text-decoration: none;
    transition: all 0.3s ease;
    height: 100%;  /* controlled height */
    width: 100%; /* fixed width for consistency */
    text-decoration: none !important;
}

.banner h2 {
    font-size: 1.2rem;
    margin: 0;
    color: white;
    text-align: left; /* align text to left for better flow */
}

.banner .arrow {
    margin-left: 10px;
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background-color: rgba(255, 255, 255, 0.9);
    color: #002147;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.2rem;
    transition: all 0.3s ease;
    box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.banner:hover {
    background-color: #4b0033;
}

.banner:hover .arrow {
    background-color: white;
    color: #4b0033;
}

@media (max-width: 480px) {a
    .banner h2 {
        font-size: 1rem;
    }

    .banner .arrow {
        width: 28px;
        height: 28px;
    }
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

The 2025 edition of the Computational Humanities Research conference will take
place on **December 9-12, 2025** at the Luxembourg Centre for Contemporary and Digital History (C²DH) at the University of Luxembourg. Read more about CHR2025:

<div class="space" style="padding-top:0.5%;"></div>

<div class="banner-grid">
    <a href="/cfp" class="banner" aria-label="View Call for Papers">
        <h2>Call for Papers</h2>
        <div class="banner-footer">
            <div class="arrow" aria-hidden="true">→</div>
        </div>
    </a>
    <a href="/people" class="banner" aria-label="View People">
        <h2>People</h2>
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
<!--
<h2>Keynote Speakers</h2>
We are very honoured and pleased that Lauren Klein and Leon Derczynski have agreed to give keynote lectures at CHR2024.
<div class="card-row">
  <div class="card-col">
    <div class="card" onclick="location.href='/announcements/lauren-klein';" style="cursor: pointer;">
      <div class="card-image">
          <img class="speaker-img" src="/images/announce/lauren-klein.jpg" alt="Portrait of Lauren Klein on card element">
        </a>
      </div>
      <div class="card-content">
        <span class="card-title">Lauren Klein</span>
        <a href="/announcements/lauren-klein" class="read-more">Read More</a>
      </div>
    </div>
  </div>
  <div class="card-col">
    <div class="card" onclick="location.href='/announcements/leon-derczynski';" style="cursor: pointer;">
      <div class="card-image">
          <img class="speaker-img" src="/images/announce/leon-derczynski-square-med-forweb.jpg" alt="Portrait of Leon Derczynski on card element">
        </a>
      </div>
      <div class="card-content">
        <span class="card-title">Leon Derczynski</span>
        <a href="/announcements/leon-derczynski" class="read-more">Read More</a>
      </div>
    </div>
  </div>
</div>
-->
