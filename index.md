---
title: Home
sections:
  - type: hero_section
    title: Welcome to the AndrewsTech Website!
    subtitle: 'Student, Developer & Youtuber'
    actions:
      - label: YouTube
        url: 'https://youtube.com/andrewstech'
        style: primary
      - label: Contact Us
        url: /contact
        style: secondary
    align: left
    image: images/YOUTUBE.png
    image_alt: Hero placeholder image
    image_position: right
    has_background: true
    background:
      background_color: blue
      background_image: images/diagonal-lines.svg
      background_image_opacity: 20
      background_image_size: auto
      background_image_repeat: repeat
  - type: features_section
    title: Projects
    features:
      - content: >
          Google home/Assistant Skill to teach young children maths. By
          embracing smart technology such as Amazon echo's and Google Home's.
          This skill was quite popular at the start but became less popular over
          time as bugs started to develop in the skill. This meant often the
          skill would crash.
        align: left
        image: images/extra revision.png
        image_alt: Feature 1 placeholder image
        image_position: right
        actions:
          - label: Learn More
            url: /extra-revision
            style: secondary
        title: Extra Revision
      - title: Mr Maths
        content: >
          Mr Maths was a flashcard based Maths quiz available on Alexa and
          Google Assistant in 2019 to early 2020.
        align: left
        image: images/mr maths.png
        image_alt: Feature 2 placeholder image
        image_position: left
        actions: []
      - title: Hibbert Home Tech
        content: >
          Hibbert Home Tech was an Alexa skill I developed for a Youtuber named
          [Paul Hibbert](https://www.youtube.com/user/wolfsweb). This skill was
          around for around 2 years but left Alexa skill store after little use.
        align: left
        image: images/unnamed.jpg
        image_alt: Feature 3 placeholder image
        image_position: right
        actions: []
  - type: blog_feed_section
    title: New Blog Posts
    show_recent: true
    recent_count: 3
  - type: cta_section
    title: GitHub Projects
    subtitle: See our open source projects.
    actions:
      - label: Learn More
        url: 'https://github.com/andrewstech'
        style: primary
    has_background: true
    background_color: gray
seo:
  title: AndrewsTech
  description: 'Student, Developer and YouTuber'
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Stackbit Starter Theme
      keyName: property
    - name: 'og:description'
      value: The preview of the Starter theme
      keyName: property
    - name: 'og:image'
      value: images/starter-preview.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Stackbit Starter Theme
    - name: 'twitter:description'
      value: The preview of the Starter theme
    - name: 'twitter:image'
      value: images/starter-preview.png
      relativeUrl: true
layout: advanced
---
