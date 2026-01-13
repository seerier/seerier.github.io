---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download CV
        url: uploads/GaoxiangZhao-resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      css_class: hbx-bg-gradient
      avatar:
        size: medium
        shape: circle

  - block: markdown
    content:
      title: '🔬 My Research'
      subtitle: ''
      text: |-
        I'm broadly interested in **Computer Graphics**, **Computer Vision**, and **Robotics**. 
        
        My current research focuses on **event-based computer vision** and its applications in robotics at the University of Pennsylvania, advised by Prof. Kostas Daniilidis.
        
        Previously, I worked on **physically-based rendering** and **physical simulation**, exploring how to accurately simulate physical light transport through complex scenes.
        
        My overarching goal is to advance robotic perception and embodied intelligence through physics-grounded simulation and learning.
    design:
      columns: '1'

  - block: markdown
    content:
      title: '💼 Experience'
      subtitle: ''
      text: |-
        **Research Intern** | University of Pennsylvania  
        *December 2025 – Present | Philadelphia, USA*  
        Working on event-based computer vision and its applications in robotics under the supervision of Prof. Kostas Daniilidis.
        
        **Research Intern** | ZJU-Coohom Joint Lab of CG&AI  
        *August 2024 – November 2024 | Hangzhou, China*  
        Explored cutting-edge algorithms in high-performance GPU Monte-Carlo ray tracing.
    design:
      columns: '1'

  - block: markdown
    content:
      title: '🚀 Selected Projects'
      subtitle: ''
      text: |-
        **Monte-Carlo Rendering Engine** | *December 2023 – January 2025*
        - Developed a high-performance C++ simulation engine solving high-dimensional light transport equations via Monte-Carlo integration
        - Implemented advanced variance reduction techniques (Importance Sampling, MIS) and stochastic algorithms (Path Tracing, Bidirectional Path Tracing, Metropolis-Hastings Light Transport)
        - Optimized performance through multithreading and efficient memory management
        
        **Diffraction Simulation** | *June 2024 – August 2024*
        - Reproduced complex wave optics models to simulate light diffraction using numerical methods
        - Integrated wave-based optics into Monte-Carlo raytracing framework
        - Conducted convergence analysis between discretized RGB and full-spectrum continuous models
    design:
      columns: '1'

  - block: collection
    id: projects
    content:
      title: 'Selected Projects'
      filters:
        folders:
          - projects
    design:
      view: card

  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - events
    design:
      view: card
      fill_image: false

  - block: collection
    id: news
    content:
      title: Recent News
      subtitle: ''
      text: ''
      page_type: blog
      count: 5
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ''
      offset: 0
      order: desc
    design:
      view: card
      spacing:
        padding: [0, 0, 0, 0]
---