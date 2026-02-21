---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-02-21
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
          - "AI/ML powered real-time auction and ranking systems"
          - "self-serve ad platforms"
          - "high performing empowered teams"
        type_speed: 70
        delete_speed: 40
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
      subtitle: "A selection of my recent work"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Product Strategy
          tag: Product Strategy
        - name: Product Execution
          tag: Product Execution
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
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Visual Tech Stack - Icons organized by category
 # - block: tech-stack
    id: skills
    content:
      title: "Tech Stack"
      subtitle: "Technologies I use to build things"
      categories:
        - name: Languages
          items:
            - name: TypeScript
              icon: devicon/typescript
            - name: JavaScript
              icon: devicon/javascript
            - name: Python
              icon: devicon/python
            - name: Go
              icon: devicon/go
        - name: Frontend
          items:
            - name: React
              icon: devicon/react
            - name: Next.js
              icon: devicon/nextjs
            - name: Tailwind CSS
              icon: devicon/tailwindcss
            - name: Alpine.js
              icon: devicon/alpinejs
        - name: Backend
          items:
            - name: Node.js
              icon: devicon/nodejs
            - name: Express
              icon: devicon/express
            - name: PostgreSQL
              icon: devicon/postgresql
            - name: Redis
              icon: devicon/redis
        - name: DevOps
          items:
            - name: Docker
              icon: devicon/docker
            - name: AWS
              icon: devicon/amazonwebservices-wordmark
            - name: GitHub Actions
              icon: brands/github
            - name: Vercel
              icon: devicon/vercel
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Dec 2023
      items:
        - title: Director of Product, Ads and Offers
          company: Paytm
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
  
  # Recent Blog Posts
 # - block: collection
    id: blog
    content:
      title: Recent Posts
      subtitle: 'Thoughts on web development, tech, and more'
      text: ''
      filters:
        folders:
          - blog
        exclude_featured: false
      count: 3
      order: desc
    design:
      view: card
      columns: 3
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
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
      email: x17kedarnath@iima.ac.in
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # CTA Card
 # - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm currently looking for **senior engineering** or **tech lead** roles.
        
        Let's connect and discuss how I can help your team.
      button:
        text: 'Download Resume'
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
