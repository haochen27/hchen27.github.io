---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

# Homepage sections, rendered top to bottom.
#   Blocks reference: https://wowchemy.com/blocks/
#   Commented-out blocks are ready to use: uncomment one once you have content for it,
#   and add a matching entry to config/_default/menus.yaml.
sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin

  # News: add new items at the top and keep the list short (drop the oldest).
  - block: markdown
    id: news
    content:
      title: News
      text: |-
        - **Sep 2026** — [DAPS++](publication/daps-plus-plus/) appears at ECCV 2026 in Malmö, Sweden.
        - **Aug 2026** — Our [review on FLIM for the peritumor microenvironment](publication/flim-peritumor-review/) is published in *Cellular and Molecular Bioengineering*.
        - **Jun 2026** — New preprint: [Improving Richardson–Lucy deconvolution with diffusion priors](publication/richardson-lucy-diffusion/).
        - **Apr 2026** — Our [instant FLIM paper](publication/instant-flim-stromal-cells/) (co-first author) is published in *iScience*.
        - **Fall 2025** — Named a Notre Dame SAI (Scientific Artificial Intelligence) Fellow.
        - **Jun 2025** — [Zero-shot FLIM denoising](publication/zero-shot-flim-denoising/) appears at CVPR 2025 Workshops.
    design:
      columns: '2'

  - block: experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      # Required fields are `title`, `company`, and `date_start`.
      # Leave `date_end` empty for a current position.
      items:
        - title: Graduate Research Assistant
          company: University of Notre Dame
          company_url: 'https://www.nd.edu/'
          location: Notre Dame, IN
          date_start: '2022-09-01'
          date_end: ''
          description: |2-
              * Developed probabilistic noise models (mixed Poisson–Gaussian, frequency-domain) for multi-channel imaging systems, improving sensor calibration and noise characterization.
              * Designed diffusion-based reconstruction methods that combine learned image priors with physics-based forward models for denoising, deblurring, super-resolution, and photon-limited microscopy deconvolution.
              * Built simulation and evaluation pipelines, and collaborated with interdisciplinary teams on biomedical imaging in microscopy and FD-NIRS.
        - title: DevOps Engineer Intern, AI Technologies
          company: SAP
          company_url: 'https://www.sap.com/'
          location: Shanghai, China
          date_start: '2021-02-01'
          date_end: '2021-06-30'
          description: |2-
              * Built ML deployment infrastructure on Azure Kubernetes with observability pipelines (Prometheus, Grafana, Jaeger) for performance monitoring.
    design:
      columns: '2'

  - block: collection
    id: publications
    content:
      title: Publications
      text: |-
        {{% callout note %}}
        See [Google Scholar](https://scholar.google.com/citations?user=u5AHuZYAAAAJ) for a full, up-to-date list.
        {{% /callout %}}
      # Show all publications (0 = all)
      count: 0
      filters:
        folders:
          - publication
    design:
      columns: '2'
      view: citation

  # - block: collection
  #   id: posts
  #   content:
  #     title: Recent Posts
  #     count: 5
  #     filters:
  #       folders:
  #         - post
  #   design:
  #     columns: '2'
  #     view: compact

  # - block: portfolio
  #   id: projects
  #   content:
  #     title: Projects
  #     filters:
  #       folders:
  #         - project
  #   design:
  #     columns: '1'
  #     view: showcase
  #     flip_alt_rows: false

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

  # Photo gallery: add images to `assets/media/albums/gallery/` and uncomment.
  # Optional captions (also used as alt text) go in a `gallery_item` list in this
  # front matter, e.g.:
  #   gallery_item:
  #     - album: gallery
  #       image: my-photo.jpg
  #       caption: Conference talk, 2026
  # - block: markdown
  #   id: gallery
  #   content:
  #     title: Gallery
  #     text: |-
  #       {{< gallery album="gallery" >}}
  #   design:
  #     columns: '1'

  - block: contact
    id: contact
    content:
      title: Contact
      email: hchen27@nd.edu
      address:
        street: 276 Fitzpatrick Hall
        city: Notre Dame
        region: IN
        postcode: '46556'
        country: United States
        country_code: US
      contact_links:
        - icon: github
          icon_pack: fab
          name: github.com/haochen27
          link: 'https://github.com/haochen27'
      # Automatically link email and phone or display as text?
      autolink: true
      # No contact form: GitHub Pages is a static host and cannot process form submissions.
      # To add one, sign up at https://formspree.io and set `provider: formspree` and `id`.
      form:
        provider: ''
    design:
      columns: '2'
---
