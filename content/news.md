---
title: "News"
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
        <a href="/news/board-vacancies"><img src="/images/news/board-vacancies.jpg" alt="Foto of buildings in Luxembourg, covered in snow"></a>
        <div class="content">
            <h3>APPLY FOR THE BOARD!</h3>
            <p>
Looking to make an impact in Computational Humanities? The Society of Computational Humanities Research (SCHR) is recruiting an Early Career Representative and a Proceedings Officer to join its board. These volunteer roles are perfect opportunities to shape the field and support its growing community. Apply by 21 February 2025! ...
            </p>
            <a class="link-button" href="/news/board-vacancies" aria-label="Press to read about the two vacancies in the CHR boardg">Read More</a>
        </div>
    </div>