---
title: Contact
date: 2022-10-24

type: landing

sections:
  - block: contact
    content:
      title: Contact
      text: |-
        Welcome to contact our laboratory!
      email: statlab905@outlook.com
      # phone: 888 888 88 88
      address:
        street: 96 Jinzhai Road
        city: Hefei
        region: Anhui
        postcode: '230026'
        country: China
        country_code: CN
      coordinates:
        latitude: '31.843309'
        longitude: '117.266587'
      directions: Enter the Management and Research Building and take the stairs or elevator to 905 on the 9th floor.
      #office_hours:
        #- 'Monday 10:00 to 13:00'
        #- 'Wednesday 09:00 to 10:00'
      # appointment_url: 'https://calendly.com'
      #contact_links:
      #  - icon: comments
      #    icon_pack: fas
      #    name: Discuss on Forum
      #    link: 'https://discourse.gohugo.io'
    
      # Automatically link email and phone or display as text?
      autolink: true
    
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '1'

  - block: markdown
    content:
      title:
      subtitle: ''
      text:
    design:
      columns: '1'
      background:
        image: 
          filename: background1.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen
---
