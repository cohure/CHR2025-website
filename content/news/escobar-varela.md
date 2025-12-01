---
title: "Keynote Miguel Escobar Varela"
date: 2021-02-19T16:05:25+01:00
---

<style>
    img.first_image {
        max-width: 100%; 
        max-height: 400px;
        display: block;
        margin-left: auto;
        margin-right: auto;
    }

    .abstract {
        text-align: justify;
        font-size:0.8rem;
        padding: 1rem;
        background-color: rgba(96,24,67,0.03);
        border-left: 4px solid #2c5282;
        border-radius: 0 6px 6px 0;
    }
</style>

<div class="announce">
    <h2 id ="about-escobar-varela">About Miguel Escobar Varela</h2>
    <p>
    <a href="https://miguelescobar.com/">Miguel Escobar Varela</a> is Associate Professor of Theatre Studies at the National University of Singapore and deputy director of the Centre for Computational Social Science and Humanities (CSSH). He studies the changing landscape of Southeast Asian cultural heritage by combining fieldwork with computational methods (such as NLP, computer vision and network analysis). His aim is to understand how the production and reception of cultural forms have changed over time, in areas such as the performing arts, print media, and digital spaces. Besides academic publications, he develops public-facing projects, which include museum installations and digital platforms. He is the author of Theater as Data (University of Michigan Press, 2021).
    </p>
    <h2 id="the-keynote">The Keynote</h2>
    <p>
    Title: <em>“A watch by Kran Kamu”: Exploratory finetuning for cultural reliability</em>
    </p>
    <h3>Abstract</h3>
    <div class="abstract">
    <p>Supervised Finetuning (SFT) can be a game changer for the humanities because it allows us to adapt powerful general-purpose models to specialized domains. Importantly, this approach doesn’t need massive amounts of data. Well-curated, small datasets can be used to tailor large open-weights models to particular historical periods, languages, or cultural contexts. However, significant errors remain, as knowledge from the model's original training data inevitably leaks into the results, and we need strategies to identify and reduce these types of errors. Part of the solution is purely technical and draws from available methods in the machine learning toolkit. For example, typical approaches for extracting more signal from limited data include hyperparameter optimization, active learning, and data augmentation. For reliability estimation, recent methods include metamorphic relation (MR) testing, which validates model outputs by checking whether they satisfy invariant properties when inputs are transformed. However, a narrow engineering perspective can lead to fundamental blind spots, as Lauren Klein, Joy Buolamwini, Kate Crawford, and others have demonstrated. Critical practices, from devising interactive artworks to closely reading datasets, should also inform the ways machine learning models are developed and evaluated. In this spirit, my research group designed a series of exploratory probes as an integral part of our model finetuning pipeline. In subsequent experiments, these probes helped us identify failure modes not surfaced by other methods, enabling the creation of better synthetic data, and the design of more robust tests. This approach led to measurable improvements in model performance and reliability. The main case studies in this talk come from research on Southeast Asian historical newspapers, but these methods can be generalized across humanities domains where cultural reliability is crucial.</p>
    </div>
</div>