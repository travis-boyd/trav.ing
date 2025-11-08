---
title: Some of the Worst Things I've Ever Read (lately)
description: some stuff that I've read. it sucks.
date: 2025-11-04
badthings:
  - text: |
        <p>When Zane confided that his pet cat – Holly – once brought him back from the brink of suicide as a teenager, the chatbot responded that Zane would see her on the other side. <p>“she’ll be sittin right there -— tail curled, eyes half-lidded like she never left.” 
    context: | 
        [ChatGPT encouraged college graduate to commit suicide, family claims in lawsuit against OpenAI](https://www.cnn.com/2025/11/06/us/openai-chatgpt-suicide-lawsuit-invs-vis) by Rob Kuznia, Allison Gordon, Ed Lavandera (CNN)
    date_published: 2025-11-06
    date_added: 2025-11-07
  - text: |
        We had another strong quarter -- with 3.5 billion people using at least one of our apps every day.
    context: |
        Mark Zuckerberg ([Meta Platforms, Inc. Third Quarter 2025 Results Conference Call](https://s21.q4cdn.com/399680738/files/doc_financials/2025/q3/META-Q3-2025-Earnings-Call-Transcript.pdf))
    date_published: 2025-10-29
    date_added: 2025-11-02
  - text: |
        <p>George Preston Marshall renamed the team ["The Redskins"] in 1933. He chose the replacement in order to keep the team's red-and-white logo, a profile of a Native American in a headdress. Marshall was an avowed segregationist who went on to football infamy: He was the last NFL owner to sign African American players, in 1962, and then only after President John F. Kennedy threatened to evict the team from its brand-new home, District of Columbia Stadium (later renamed for the slain Robert F. Kennedy), which sat on federal land. [...]</p>
        <p>Donald Trump this July threatened to withhold funding for a new stadium in D.C.—on the site of the team's old one, built back when George Preston Marshall still fielded an all-white team—if the current rich-dude owners didn't revert to the racist nickname the team sported for almost 90 years.</p>
    context: |
        [The Annotated History Of A Slur](https://defector.com/the-annotated-history-of-a-slur) (Defector) by Stefan Fatsis
    date_added: 2025-10-16
    date_published: 2025-10-13
  - text: |
        The rate of productivity growth has been in sharp decline since 2003, and today sits where it stood before the widespread adoption of the personal computer.
    context: |
        [Generative AI's Productivity Myth](https://www.techpolicy.press/generative-ais-productivity-myth/) (Tech Policy Press) by Eryk Salvaggio
    date_added: 2025-10-17
    date_published: 2025-10-13
  - text: |
        Most of the spending was on guns and armor, but there have also been significant purchases of chemical weapons and “guided missile warheads and explosive components."
    context: |
        [Ice Boosts Weapons Spending 700%](https://popular.info/p/ice-boosts-weapons-spending-700) (Popular Information) by Judd Legum
    date_published: 2025-10-20
    date_added: 2025-10-20
---


{% for s in badthings | sort(attribute='date_added') | reverse %}
    <ul>
        <div class="quote">
            <section class="goodbadbubble">{{ s.text | markdown | safe }}</section>
            <div class="quote attribution">
                <small>
                    <span class="context">— {{ s.context | markdown | safe}}</span>
                    <span class="date">- {% if s.date_published %}{{s.date_published | dateFormat("MM-dd-yy")}} {% endif %}{% if s.date_added %}(added {{s.date_added | dateFormat("MM-dd")}}) {% endif %}</span>
                </small>
            </div>
        </div>
    </ul>
{% endfor %}
