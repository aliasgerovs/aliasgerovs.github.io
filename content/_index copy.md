<!-- ---
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

        - title: Lead Machine Learning Engineer
          company: Polygraf.ai
          company_url: 'https://www.polygraf.ai'
          company_logo: poli
          location: Austin, Texas, USA
          date_start: '2023-12-01'
          date_end:   'Present'
          description: |2-
              - Developing AI solutions for data governance, content verification, and AI‐generated content detection.
              - Ensuring the protection of confidential and proprietary data through advanced AI techniques.
              - Developing work flows using AWS components like Sagemaker, Lambda, Step Functions as building blocks for creating pipelines with stages for training, validation, scoring, deployment to production for Machine Learning Models.
              - Fine‐tuning BERT, RoBERTa, DeBERTa, and T5 models for text classification to identify AI‐generated content, achieved a 92% F1 score, and deployed them through AWS SageMaker and Google Cloud (GCP) Deep Learning VM in Python.
              - Utilizing LSTM and pre‐trained CNN models for transfer learning to detect deepfake images andv ideos, preventing misinformation.
              - Developing Retrieval‐Augmented Generation (RAG) models and a hybrid reranking system to enhance text generation quality to avoid hallucination in LLM usage across different domains.

        - title: Lead Machine Learning Engineer
          company: Revenue.ai
          company_url: 'https://www.revenue.ai'
          company_logo: rai
          location: Remote, Amsterdam, Noord-Holland, The Netherlands
          date_start: '2022-04-01'
          date_end:   '2023-07-01'
          description: |2-
              - Musigma - [mu-sigma.com](https://mu-sigma.com/) | 01.2023 - 04.2023, Remote, Illinois, USA. Developed chatbot models, successfully deployed them in production environments, and establishing a robust model traning pipeline.
              - PepsiCo - [pepsico.com.br](https://pepsico.com.br/) | 08.2022 - 01.2023, Remote, Brazil. Developed a custom NLP models and leveraged that for filter detection within user intents. Integrated filter detection into the chatbot and dashboard for enhanced functionality.
              - Anicura - [anicuragroup.com](https://anicuragroup.com/) | 05.2022 - 08.2022, Remote, Italy, Sweden, Germany. Developed text classification NLP models for predicting multi-level product categories within different markets.
              - Louis Dreyfus Company - [ldc.com](https://ldc.com/) | 03.2022 - 05.2022  Remote, France. Developed robust ML models, harnessed data processing and visualization tools to drive data-driven decision-making. 

        - title: Machine Learning Engineer
          company: Koaila
          company_url: 'https://koaila.com/'
          company_logo: koaila
          location: Remote, Paris, France
          date_start: '2023-04-01'
          date_end:   '2023-08-01'
          description: |2-
              - Employed advanced Natural Language Processing techniques to analyze extensive customer and product data.
              - Leveraged AI and granular product usage data to gain profound insights into user behaviors, feature adoption patterns, and customer preferences. 
              - Ensured the privacy and security of sensitive customer data while utilizing advanced machine learning techniques to analyze product data.
              
        - title: Machine Learning Engineer
          company: Voiceloft
          company_url: 'https://voiceloft.com/'
          company_logo: voiceloft
          location: Remote, Middletown, Delaware, United States
          date_start: '2021-03-01'
          date_end:   '2022-07-01'
          description: |2-
              - Neural Space - [neuralspace.ai](https://neuralspace.ai/) | 11.2021 - 03.2022, United Kingdom. Worked on design, development, testing , tuning of ASR - speech recognition models for 11 languages. Developed language identification models for data gathering applications.
              - Imla Project - [imla.az](https://voiceloft.com) | 07.2021 - 11.2021 Azerbaijan. Designed, developed, tested, and fine-tuned cutting-edge ASR speech recognition models for the Azerbaijani language employing frameworks such as PyTorch and Kaldi.
              - Voooice - [voooice.com](https://voooice.com/) | 03.2021 - 07.2021. Collected audio dataset, and created multilingual speech recognition technologies.
        - title: Machine Learning Instructor
          company: Data Science Academy
          company_url: 'https://dsa.az'
          company_logo: dsa
          location: Baku, Azerbaijan
          date_start: '2020-01-01'
          date_end:   '2020-07-01'
          description: |2-
              - Guided hundreds of students in mastering Data Science methodologies using R, Python, Spark, Spark SQL and various machine learning and deep learning methodologies. 
              - Supported trainings to researchers relating to NLP and Machine Learning research methods.
        - title: Student Researcher
          company: Baku Higher Oil School Robotics Lab
          company_url: 'https://bhos.edu.az'
          company_logo: bhos
          location: Baku, Azerbaijan
          date_start: '2018-03-01'
          date_end:   '2019-12-01'
          description: |2-
              - Represented Azerbaijan in Hungary among world countries in World Robot Olympiad with project titled 'Optimizing Road Networks for Automated Vehicles with using Open CV'. 
              - Worked on the optimizing traffic light timing for vehicles with using Open CV. 
              - Adeptly used Python (OpenCV), and build object detection models. 
              - Participated in cutting edge research in computer vision.

                    
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
        - 2022 : State Program on education of Azerbaijani youth abroad Scholarship Winner.
        - 2022 : 3x National Student Scientific Conferences 1st place winner in Machine Learning Applications (2020, 2021, 2022).
        - Achieved an IELTS score of 7.5.
        - Ranked among the top 15 teams at the III World Robot Olympiad in Gyor, Hungary.
        - Awarded the Golden Medal at the III World Robot Olympiad in Azerbaijan.
        - Earned the Presidential Scholarship for exceptional academic performance.
        - Scored an impressive 690 out of 700 on the University Entrance Exam. 
        - High school graduate with a Golden Medal, placing in the top 5% among 60k graduating students.
        - Honored as the Golden Medalist in the Respublic Physics Olympiad.
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

--- -->
