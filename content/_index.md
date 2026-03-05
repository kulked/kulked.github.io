---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026
type: landing

design:
  # Default section spacing
  spacing: '0'

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me
      greeting: "Hi, I'm"
      show_status: true
      show_scroll_indicator: true
      typewriter:
        enable: true
        prefix: "I build"
        strings:
          - "ads and offers monetisation levers"
          - "AI/ML powered auction and ranking systems"
          - "self-serve ad platforms"
          - "high performing empowered teams"
        type_speed: 80
        delete_speed: 50
        pause_time: 2500
      cta_buttons:
        - text: View My Work
          url: "#projects"
          icon: arrow-down
        - text: Get In Touch
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]
  
  # Filterable Portfolio - Alpine.js powered project filtering
  - block: portfolio
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my PM work on hypothetical scenarios at real world companies"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Product Strategy
          tag: Product Strategy
        - name: Product Discovery
          tag: Product Discovery
        - name: Product Launch
          tag: Product Launch
        - name: Product Analytics
          tag: Product Analytics
      default_button_index: 0
      # Archive link auto-shown if more projects exist than 'count' above
      # archive:
      #   enable: false  # Set to false to explicitly hide
      #   text: "Browse All"  # Customize text
      #   link: "/work/"  # Custom URL
    design:
      columns: 3
      view: card
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  
  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: 2023
      items:
        - title: Director of Product, Ads and Offers
          company: Paytm, Bengaluru, India
          company_url: ''
          company_logo: ''
          location: Bengaluru, India
          date_start: '2023-12-01'
          date_end: ''
          description: |2-
            * As the Head of Product for Ads and Offers, set the roadmap and OKRs for ad formats, ads manager, audiences, targeting, ad serving, auction/ ranking, and measurement charters. Delivered yield improvements for Paytm and content relevance for 100M MAUs via machine learning platform initiatives.
        - title: Lead Product Manager, Marketing Experiences
          company: Grab
          company_url: ''
          company_logo: ''
          location: Singapore
          date_start: '2022-02-01'
          date_end: '2023-06-31'
          description: |2-
            * Defined the product roadmap, OKRs, and led execution for the marketing experiences problem area. Drove multi-million dollar ad revenue impact for Grab (the leading mobile super app in SE Asia) and delivered relevant promoted content for 40M MTUs.
        - title: Senior Product Manager
          company: LG Ads
          company_url: ''
          company_logo: ''
          location: Bangalore, Mountain View, New York
          date_start: '2018-05-01'
          date_end: '2021-12-31'
          description: |2-
            * Drove the consumer insights and monetization initiatives by building ad tech products for activating and measuring display and video media across 120M TVs at Silicon Valley video AI startup Alphonso (now LG Ads Solutions, following investment by electronics giant LG).
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  
  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something amazing together"
      text: |-
        I'm always interested in hearing about new projects and opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  
---
