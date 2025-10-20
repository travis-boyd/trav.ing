---
title: some of the best things I've ever read (lately)
description: some stuff that I've read. it's lovely.
draft: true
goodthings:
  - text: |
        <h4>Tony and Maria's first encounter in West Side Story</h4>
        <div class="ichat">
            <div class="bubble left"> <strong>Tony</strong>: You're not thinking I'm someone else? </div>
            <div class="bubble right"> <strong>Maria</strong>: I know you are not. </div>
            <div class="bubble left"> <strong>Tony</strong>: Or that we've met before? </div>
            <div class="bubble right"> <strong>Maria</strong>: I know we have not. </div>
            <div class="bubble left"> <strong>Tony</strong>: I felt-- I knew something-never-before was going to happen. Had to happen. But this is... </div>
            <div class="bubble right"> <strong>Maria</strong>: My hands are cold... yours too.</div>
            <div class="bubble right"> \*touches ur face\* </div>
            <div class="bubble right"> <strong>Maria</strong>: So warm. </div>
            <div class="bubble left"> <strong>Tony</strong>: Yours, too... </div>
            <div class="bubble right"> <strong>Maria</strong>: But of course. They are the same. </div>
            <div class="bubble left"> <strong>Tony</strong>: It's so much to believe. </div>
            <div class="bubble left"> <strong>Tony</strong>: You're not joking me? </div>
            <div class="bubble right"> <strong>Maria</strong>: I have not yet learned how to joke that way. I think now I never will. </div>
        </div>
    context: >
        West Side Story, Act I Scene IV <br>
        Tony and Maria's first encounter
    date_added: 2025-10-16
---
## some stuff that doesn't

{% for s in goodthings | reverse %}
    <ul>
        <div class="quote">
            <section class="goodbadbubble">{{ s.text | markdown | safe }}</section>
            <div class="quote attribution">
                <small>
                    <span class="context">— {{ s.context | markdown | safe}}</span>
                    <span class="date">{% if s.date_added %}added on {{s.date_added.toISOString().slice(0,10)}} {% endif %}</span>
                </small>
            </div>
        </div>
    </ul>
{% endfor %}
