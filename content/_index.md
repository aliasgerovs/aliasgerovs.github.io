---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:

  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  # - block: features
  #   content:
  #     title: Skills
  #     items:
  #       - name: R
  #         description: 90%
  #         icon: r-project
  #         icon_pack: fab
  #       - name: Statistics
  #         description: 100%
  #         icon: chart-line
  #         icon_pack: fas
  #       - name: Photography
  #         description: 10%
  #         icon: camera-retro
  #         icon_pack: fas
  - block: experience
    id: experience
    content:
      title: Experience 
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:

        - title: Graduate Teaching Assistant
          company: Virginia Tech
          company_url: 'https://www.vt.edu'
          company_logo: vt
          location: Blacksburg, VA, USA
          date_start: '2024-08-10'
          # date_end:   '2025-08-10'

        - title: Lead Machine Learning Engineer
          company: Polygraf.ai
          company_url: 'https://www.polygraf.ai'
          company_logo: poli
          location: Austin, Texas, USA
          date_start: '2023-12-01'
          date_end:   '2024-08-01'

        - title: Lead Machine Learning Engineer
          company: Revenue.ai
          company_url: 'https://www.revenue.ai'
          company_logo: rai
          location: Amsterdam, Noord-Holland, The Netherlands
          date_start: '2022-04-01'
          date_end:   '2023-07-01'
          # description: |2- 
          #     Projects : 
          #     -  Musigma - [mu-sigma.com](https://mu-sigma.com/)
          #     -  PepsiCo - [pepsi.com](https://pepsi.com.br/)
          #     -  Anicura - [anicuragroup.com](https://anicuragroup.com/)
          #     -  Louis Dreyfus Company - [ldc.com](https://ldc.com/)
              
          #     Responsibilities: 
          #     - Research-oriented machine learning engineer. 
          #     - Proficient in Python, PySpark, Azure, and PostgreSQL.
          #     - Built anomaly detection, classification, regression models for alerting pipelines.
          #     - Specialized in designing end-to-end AI/ML modeling pipelines for efficient data-driven solutions.

          # text : Test
        # - title: Lead Machine Learning Engineer
        #   company: Koaila
        #   company_url: 'https://koaila.com/'
        #   company_logo: koaila
        #   location: Paris, France
        #   date_start: '2023-05-01'
        #   date_end:   '2023-08-01'
          # description: |2-
            #  Projects :
            #  - Prophesee - [prophesee.ai](https://prophesee.ai/)
            #  - Microtica - [microtica.com](https://microtica.com/)
            #  - Filestage - [filestage.com](https://filestage.io)
             
            #  Responsibilities: 
            #  - Research and develop clustering, classification, and semi-supervised models for user behavior analysis.
            #  - Proficient in Python, FastAPI, AWS, Git, and modeling techniques.
            #  - Specialize in AI/ML modeling pipeline design.
            #  - Build text classification NLP models for sentiment analysis and content categorization.

        - title: Middle Machine Learning Engineer
          company: Voiceloft
          company_url: 'https://voiceloft.com/'
          company_logo: voiceloft
          location: Middletown, Delaware, United States
          date_start: '2021-02-01'
          date_end:   '2022-04-01'
          # description: |2-
          #    Projects :
          #    - Neural Space - [neuralspace.ai](https://neuralspace.ai/)
          #    - Imla Project - [imla.az](https://voiceloft.com)
          #    - Voooice - [voooice.com](https://voooice.com/)

          #    Responsibilities: 
          #    - Deep learning researcher specialized in designing, developing, and continuously tuning voice recognition models. 
          #    - Proficient in Python, Deep Learning, PySpark, PostgreSQL, AWS, PyTorch, TensorFlow, Speech Recognition.
          #    - Designed deep learning modeling pipelines.

        - title: Machine Learning Instructor
          company: Data Science Academy
          company_url: 'https://dsa.az'
          company_logo: dsa
          location: Baku, Azerbaijan
          date_start: '2020-06-01'
          date_end:   '2021-06-01'
          # description: |2-
          #   Projects :
          #    - QSS Analytics - [qss.az](http://www.qss.az)
          #    - Data Science Bootcamps - [dsa.az](http://www.dsa.az)
            
          #   Responsibilities: 
          #   - Instructed and guided students in machine learning methodologies with proficiency in Python, R, Matlab, and SQL.
          #   - Specialized in mentoring deep learning model research and development.
          #   - Provided hands-on training and practical insights to empower students with the skills needed in the field of machine learning. 
          #   - Participated in hackathons organized by [UNDP](https://www.undp.org), [ABB](https://abb-bank.az).

        - title: Student Researcher
          company: Baku Higher Oil School AI Lab
          company_url: 'https://bhos.edu.az'
          company_logo: bhos
          location: Baku, Azerbaijan
          date_start: '2018-03-01'
          date_end:   '2020-06-01'
          # description: |2-
          #     Projects :
          #     - III World Robot Olympiad - [wro.com](https://wro-association.org)
          #     - AREA - Azerbaijan Robotics Engineering Academy - [robot.az](https://www.robot.org.az)
              
          #     Responsibilities: 
          #     - Student researcher specialized in deep learning model research and development.
          #     - Represented Azerbaijan in Hungary among world countries in World Robot Olympiad with project of optimizing traffic light timing for vehicles with using Open CV.
          #     - Worked on student conference papers focusing on deep learning applications under the guidance of Dr. Ali Parsayan

    design:
      columns: '2'
  # - block: accomplishments
  #   content:
  #     # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
  #     title: 'Accomplish&shy;ments'
  #     subtitle:
  #     # Date format: https://wowchemy.com/docs/customization/#date-format
  #     date_format: Jan 2006
  #     # Accomplishments.
  #     #   Add/remove as many `item` blocks below as you like.
  #     #   `title`, `organization`, and `date_start` are the required parameters.
  #     #   Leave other parameters empty if not required.
  #     #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
  #     items:
  #       - certificate_url: https://www.coursera.org
  #         date_end: ''
  #         date_start: '2021-01-25'
  #         description: ''
  #         organization: Coursera
  #         organization_url: https://www.coursera.org
  #         title: Neural Networks and Deep Learning
  #         url: ''
  #       - certificate_url: https://www.edx.org
  #         date_end: ''
  #         date_start: '2021-01-01'
  #         description: Formulated informed blockchain models, hypotheses, and use cases.
  #         organization: edX
  #         organization_url: https://www.edx.org
  #         title: Blockchain Fundamentals
  #         url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
  #       - certificate_url: https://www.datacamp.com
  #         date_end: '2020-12-21'
  #         date_start: '2020-07-01'
  #         description: ''
  #         organization: DataCamp
  #         organization_url: https://www.datacamp.com
  #         title: 'Object-Oriented Programming in R'
  #         url: ''
  #   design:
  #     columns: '2'
  - block: collection
    id: projects
    content:
      title: Projects
      id: projects
      filters:
        folders:
          - project
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: compact
      
  - block: collection
    id: publications
    content:
      title: Publications
      # text: |-
      #   {{% callout note %}}
      #   Quickly discover relevant content by [filtering publications](./publication/).
      #   {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: markdown
    id: service
    content:
      title: Service
      subtitle: ''
      text: |-
         - Participant at [III World Robot Olympiad](https://wro-association.org/) 2019
    design:
      columns: '1'

  # - block: collection
  #   id: featured
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publication
  #       featured_only: true
  #   design:
  #     columns: '2'git ad
  #     view: card
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     columns: '2'
  #     view: compact
  # - block: tag_cloud
  #   content:
  #     title: Popular Topics
  #   design:
  #     columns: '2'
  - block: contact
    id: contact
    content:
      title: Honors and Awards
      subtitle:
      text: |-
        - 2022, Winner, State Program on education of Azerbaijani youth abroad Scholarship Winner.
        - 2022, Winner, 3x National Student Scientific Conferences 1st place winner in Machine Learning Applications (2020, 2021, 2022).
        - 2021, Certified, Achieved an IELTS score of 7.5.
        - 2020, Finalist, Ranked among the top 15 teams at the III World Robot Olympiad in Gyor, Hungary.
        - 2019, Winner, Awarded the Golden Medal at the III World Robot Olympiad in Azerbaijan.
        - 2018, Winner, Earned the Presidential Scholarship for exceptional academic performance.
        - 2017, Scorer, Scored an impressive 690 out of 700 on the University Entrance Exam. 
        - 2017, Winner, High school graduate with a Golden Medal, placing in the top 5% among 60k graduating students.
        - 2017, Winner,Honored as the Golden Medalist in the Respublic Physics Olympiad.
    design:
      columns: '1'

  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: true
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
      
    #   # Contact (add or remove contact options as necessary)
    #   email: test@example.org
    #   phone: 888 888 88 88
    #   appointment_url: 'https://calendly.com'
    #   address:
    #     street: 450 Serra Mall
    #     city: Stanford
    #     region: CA
    #     postcode: '94305'
    #     country: United States
    #     country_code: US
    #   directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
    #   office_hours:
    #     - 'Monday 10:00 to 13:00'
    #     - 'Wednesday 09:00 to 10:00'
    #   contact_links:
    #     - icon: twitter
    #       icon_pack: fab
    #       name: DM Me
    #       link: 'https://twitter.com/Twitter'
    #     - icon: skype
    #       icon_pack: fab
    #       name: Skype Me
    #       link: 'skype:echo123?call'
    #     - icon: video
    #       icon_pack: fas
    #       name: Zoom Me
    #       link: 'https://zoom.com'
    #   # Automatically link email and phone or display as text?
    #   autolink: true
    #   # Email form provider
    #   form:
    #     provider: netlify
    #     formspree:
    #       id:
    #     netlify:
    #       # Enable CAPTCHA challenge to reduce spam?
    #       captcha: false
    # design:
    #   columns: '2'

---
