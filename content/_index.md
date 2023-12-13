---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography #??? remove about
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
    design:
      banner:
        # Upload a cover image to `assets/media/` folder and reference its filename here (optional)
        filename: ''
  - block: portfolio
    id: projects
    content:
      title: Research
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: ICM
          tag: ICM
        - name: Other
          tag: Other
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: A complete list of projects I have contributed to can be found [here](https://ui.adsabs.harvard.edu/search/p_=0&q=%20author%3A%22Lehle%2C%20Katrin%22&sort=date%20desc%2C%20bibcode%20desc).

        -
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  - block: collection
    id: talks
    content:
      title: Recent & Upcoming Talks
      filters:
        folders:
          - event
    design:
      columns: '2'
      view: compact
  - block: tag_cloud
    content:
      title: Tags
    design:
      columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: ''
      # Contact (add or remove contact options as necessary)
      email: k.lehle@stud.uni-heidelberg.de
      phone: ''
      appointment_url: ''
      address:
        street: Albert-Ueberle Straße 3-5
        city: Heidelberg
        region: 'BW'
        postcode: '69120'
        country: Germany
        country_code: 'DE'
  #    # Choose a map provider in `params.yaml` to show a map from these coordinates
  #    coordinates:
  #      latitude: '49.41440'
  #      longitude: '8.69454'  
  #    contact_links: ''
  #    # Automatically link email and phone or display as text?
  #    autolink: true
  #    # Email form provider
  #    form:
  #      provider: netlify
  #      formspree:
  #        id:
  #      netlify:
  #        # Enable CAPTCHA challenge to reduce spam?
  #        captcha: false
  #  design:
  #    columns: '2'
---
