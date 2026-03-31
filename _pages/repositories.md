---
page_id: repositories
layout: page
permalink: /repositories/
title: repositories
description: A selection of my GitHub projects and side work.
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub Profile

<div class="d-flex flex-wrap mb-4">
  {% for user in site.data.repositories.github_users %}
  <a href="https://github.com/{{ user }}" target="_blank" rel="nofollow noopener" class="btn btn-outline-dark">
    <i class="fab fa-github mr-2"></i>{{ user }}
  </a>
  {% endfor %}
</div>

---

{% endif %}

{% if site.data.repositories.github_repos %}

## Projects

<div class="row mt-3">
  {% for repo in site.data.repositories.github_repos %}
  {% assign repo_parts = repo.name | split: '/' %}
  <div class="col-sm-6 mb-4">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title font-weight-bold">
          <i class="fab fa-github mr-2"></i>{{ repo_parts[1] }}
        </h5>
        {% if repo.description and repo.description != "" %}
        <p class="card-text text-muted">{{ repo.description }}</p>
        {% endif %}
        {% if repo.language and repo.language != "" %}
        <span class="badge badge-secondary">{{ repo.language }}</span>
        {% endif %}
      </div>
      <div class="card-footer bg-transparent">
        <a href="https://github.com/{{ repo.name }}" target="_blank" rel="nofollow noopener" class="btn btn-sm btn-outline-primary">
          View on GitHub &rarr;
        </a>
      </div>
    </div>
  </div>
  {% endfor %}
</div>

{% endif %}
