---
title: 'News'
date: 2021-02-19T16:05:25+01:00
---

<style>
    div.news {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(min(320px, 100%), 1fr));
        grid-column-gap: 24px;
        grid-row-gap: 24px;
    }
    .announce {
        /*border: 1px solid;*/
        display: flex;
        flex-direction: column;
    }

    .announce .content {
        padding: 0 0rem 1rem 0rem;
        display: flex;
        flex-direction: column;
        flex-grow: 1;
    }

    .announce .content h3 {
        margin-bottom: 0px;
    }
    .announce img {
        width: 100%;
        aspect-ratio: 2/1;
        object-fit: cover;
        object-position: 100% 0;
    }

    p {
        font-size: 1rem;
    }

    .link-button {
        display: inline-block;
        padding: 0.5rem 1rem;
        border: 1px solid;
        border-radius: 24px;
        margin-top: auto;
        align-self: flex-start;
        text-decoration: none !important;
    }
</style>

<div class="news">
    <div class="announce">
        <a href="/news/keynote-speakers"><img src="/images/news/keynote-speakers.jpg" alt="Keynote Speakers annnounced"></a>
        <div class="content">
            <h3>We are happy to announce the keynote speakers of the CHR2025 conference!</h3>
            <p>
            We are proud to have <a href="https://miguelescobar.com/" target="_blank">Miguel Escobar Varela</a> and <a href="https://research.flw.ugent.be/en/els.lefever" target="_blank">Els Lefever</a> as keynote speakers at the Computational Humanities Research 2025 (CHR2025) conference. Their expertise in computational methods and their contributions to the field will provide valuable insights for all attendees. ...
            </p>
            <a class="link-button" href="/news/keynote-speakers" aria-label="Press to read more">Read More</a>
        </div>
    </div>
    <div class="announce">
        <a href="/cfp"><img src="/images/news/CHR2025-cfp.001.jpeg" alt="Call for Papers"></a>
        <div class="content">
            <h3>CALL FOR PAPERS</h3>
            <p>
The Call for Papers for the Computational Humanities Research 2025 (CHR2025) conference is now out. CHR2025 continues its tradition of providing a dedicated platform for presenting computational work that bridges formal methods and traditional inquiry in the arts and humanities. ...
            </p>
            <a class="link-button" href="/cfp" aria-label="Press to read the Call for Papers">Read More</a>
        </div>
    </div>
    <div class="announce">
        <a href="/news/board-vacancies"><img src="/images/news/board-vacancies.jpg" alt="Foto of buildings in Luxembourg, covered in snow"></a>
        <div class="content">
            <h3>APPLY FOR THE BOARD!</h3>
            <p>
Looking to make an impact in Computational Humanities? The Society of Computational Humanities Research (SCHR) is recruiting an Early Career Representative and a Proceedings Officer to join its board. These volunteer roles are perfect opportunities to shape the field and support its growing community. Apply by 21 February 2025! ...
            </p>
            <a class="link-button" href="/news/board-vacancies" aria-label="Press to read about the two vacancies in the CHR board">Read More</a>
        </div>
    </div>
</div>
