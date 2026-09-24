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

  # - block: experience
  #   id: experience
  #   content:
  #     title: Experience
  #     date_format: Jan 2006
  #     # Required fields are `title`, `company`, and `date_start`.
  #     # Leave `date_end` empty for a current position.
  #     items:
  #       - title: Graduate Research Assistant
  #         company: University of Notre Dame
  #         company_url: 'https://www.nd.edu/'
  #         location: Notre Dame, IN
  #         date_start: '20XX-08-01'
  #         date_end: ''
  #         description: ''
  #   design:
  #     columns: '2'

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
