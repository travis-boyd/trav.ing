---
title: some of the worst things I've ever read (lately)
description: some stuff that I've read. it sucks.
date: 2025-10-13
badthings:
  - text: |
        \[Owner\] George Preston Marshall renamed the team in 1933. He chose ["The Washington Redskins"] in order to keep the team's red-and-white logo, a profile of a Native American in a headdress. Marshall was an avowed segregationist who went on to football infamy: He was the last NFL owner to sign African American players, in 1962, and then only after President John F. Kennedy threatened to evict the team from its brand-new home, District of Columbia Stadium (later renamed for the slain Robert F. Kennedy), which sat on federal land.
        <br><br>[...]<br><br>
        Donald Trump this July threatened to withhold funding for a new stadium in D.C.—on the site of the team's old one, built back when George Preston Marshall still fielded an all-white team—if the current rich-dude owners didn't revert to the racist nickname the team sported for almost 90 years.  

        <strong>"This is Trump's whole movement in rancid miniature: extolling and bringing back the bad times, one reflexive trip on Beelzebub's hamster wheel after another</strong>," Ray Ratto wrote.
    context: |
        [The Annotated History Of A Slur](https://defector.com/the-annotated-history-of-a-slur) (Defector) by Stefan Fatsis
    date_added: 2025-10-16
  - text: |
        The rate of productivity growth has been in sharp decline since 2003, and today sits where it stood before the widespread adoption of the personal computer.
    context: |
        [Generative AI's Productivity Myth](https://www.techpolicy.press/generative-ais-productivity-myth/) (Tech Policy Press) by Eryk Salvaggio
    date_added: 2025-10-17
  - text: |
        Most of the spending was on guns and armor, but there have also been significant purchases of chemical weapons and “guided missile warheads and explosive components."
    context: |
        [Ice Boosts Weapons Spending 700%](https://popular.info/p/ice-boosts-weapons-spending-700) (Popular Information) by Judd Legum
    date_published: 2025-10-20
    date_added: 2025-10-20
---

## some stuff that sucks

{% for s in badthings | reverse %}
    <ul>
        <div class="quote">
            <section class="goodbadbubble">{{ s.text | markdown | safe }}</section>
            <div class="quote attribution">
                <small>
                    <span class="context">— {{ s.context | markdown | safe}}</span>
                    <span class="date">- {% if s.date_published %}{{s.date_published.toISOString().slice(0,10)}} {% endif %}</span>
                    <span class="date">{% if s.date_added %}added {{s.date_added.toISOString().slice(5,10)}} {% endif %}</span>
                </small>
            </div>
        </div>
    </ul>
{% endfor %}
## some stuff that doesn't

{% for s in goodthings | reverse %}
    <ul>
        <div class="quote">
            <section class="goodbadbubble">{{ s.text | markdown | safe }}</section>
            <div class="quote attribution">
                <small>
                    <span class="context">— {{ s.context | markdown | safe}}</span>
                    <span class="date">{% if s.date_written %}added on {{s.date_written.toISOString().slice(0,10)}} {% endif %}</span>
                    <span class="date">{% if s.date_added %}added on {{s.date_added.toISOString().slice(0,10)}} {% endif %}</span>
                </small>
            </div>
        </div>
    </ul>
{% endfor %}
