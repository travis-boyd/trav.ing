---
title: Weekly Update (October 2025)
description: some stuff that I've seen this week
date: 2025-10-30
image_galleries:
  - id:  wunderkammer
    caption: "Wunderkammer Photos"
    images: 
      - src: "/blog/weekly_post/1/img1.jpg"
        alt: "img1 description"
        caption: "Isabelle's *Self-Portrait*, first runner-up for Best in Show"
        id: "img1"
      - src: "/blog/weekly_post/1/img2.jpg"
        alt: "img2 description"
        id: "img2"
        caption: "The Best in Show winner, *Guardian Angel*"
      - src: "/blog/weekly_post/1/img3.jpg"
        alt: "img3 description"
        id: "img3"
        caption: "the Frank Frock"
      - src: "/blog/weekly_post/1/img4.jpg"
        alt: "img4 description"
        id: "img4"
        caption: "I don't know what this is. It's cool though."
---

## some stuff I did 
### Wunderkammer 2025
<p>Last week, Isabelle and I drove to Brooklyn so that Isabelle could present two of their pieces at Wunderkammer, described both as (when it was initially pitched to me) an "art show" and (by the time we arrived at the venue) a "taxidermy competition." For a three day trip that included two full days of driving, it was a great way to spend twenty four vacation hours.  
<p>Wunderkammer -- in its fifth year -- was being filmed for a feature documentary. Isabelle and their work were professionally photographed for the documentary, and also for a magazine feature in a new taxidermy arts magazine. I don't know when we're going to see those pictures, but they will be very cool whenever we do. The venue was dark and the A/V setup inadequate and everybody seemed to agree afterwards that we wanted, needed a better look at just about every piece that was presented.  
<p>Isabelle's *My Beautiful Sons*, cast-iron dead-baby chickens in handmade bird nests of found materials -- robbed in its category and, as always, underappreciated by all. Their *Self Portrait*, a found and tattered taxidermy fox repaired unnaturally with sheets of plasma cut metals, won First Runner Up for Best in Show (2nd best piece in the entire show!). So proud of them.  
<p>I wish I could post better pictures of the event and, particularly, Isabelle's work.</p>


{% for gallery in image_galleries %}
  {% set image_gallery = gallery %}
  {% include "photo-grid.njk" %}
{% endfor %}


### made the above photo grid

I spent way too long today fiddling with this css-only grid. I'm calling it done, first draft, publish 