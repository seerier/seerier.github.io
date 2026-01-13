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

  - block: experience
    content:
      title: '💼 Experience'
      # 宾夕法尼亚大学经历
      - company: University of Pennsylvania
        company_url: ''
        company_logo: '' # 如果你有图标，可以放入 assets/media/ 并写上文件名
        location: Philadelphia, USA
        title: Research Intern
        date_start: '2025-12-01'
        date_end: '' # 留空显示为 "Present"
        description: Working on event-based computer vision and its applications in robotics under the supervision of Prof. Kostas Daniilidis.
      # 浙江大学-酷家乐联合实验室经历
      - company: ZJU-Coohom Joint Lab of CG&AI
        company_url: ''
        company_logo: ''
        location: Hangzhou, China
        title: Research Intern
        date_start: '2024-08-01'
        date_end: '2024-11-01'
        description: Explored cutting-edge algorithms in high-performance GPU Monte-Carlo ray tracing.
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