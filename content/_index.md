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
        text: Resume
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
        I'm broadly interested in **Robot Learning**, **3D Vision**, and **Simulation**.

        At Penn, I work on computer vision and robotics with Prof. Kostas Daniilidis. My current project is on **event-based vision**.

        During my undergrad, I worked on **physically-based rendering** and **light transport simulation**. At that time, my dream was to create a virtual world with accurate physics and geometry.

        Now, I want to help robots better understand the **physics and geometry** of the world, whether through simulation or beyond it.
    design:
      columns: '1'

  - block: markdown
    content:
      title: '💼 Experience'
      subtitle: ''
      text: |-
        **Research Intern | University of Pennsylvania**  
        *December 2025 – Present | Philadelphia, USA*  
        Working on event cameras and robotics with Prof. Kostas Daniilidis.

        **Research Intern | Manycore Tech**    
        *August 2024 – November 2024 | Hangzhou, China*  
        Developed Monte-Carlo physically-based rendering algorithms for a production-scale rendering pipeline supporting photorealistic synthetic data generation.
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
      fill_image: false

---