---
title: "Teams"
layout: gridlay
excerpt: "Teams"
permalink: /teams/
---

<div class="lab-index-header">
  <h1>Hylogenesis Teams</h1>
  <p class="epigraph">“If you want to go fast, go alone. If you want to go far, go together.” — African Proverb</p>
</div>

<div class="team-grid">
  {% assign teams_sorted = site.teams | sort: "title" %}
  {% for team in teams_sorted %}
    {% assign members = site.data.teams[team.team_key] %}
    <a href="{{ team.url | relative_url }}" class="team-card">
      <div class="team-card__image">
        <img src="{{ team.image | relative_url }}" alt="{{ team.title }}" />
      </div>
      <div class="team-card__body">
        <h3 class="team-card__name">{{ team.title }}</h3>
        <p class="team-card__subtitle">{{ team.subtitle }}</p>
        <p class="team-card__excerpt">{{ team.excerpt }}</p>
        <span class="team-card__count">
          {{ members | size }} member{% if members.size != 1 %}s{% endif %}
        </span>
      </div>
    </a>
  {% endfor %}
</div>

<p><b>Hylogenesis Teams</b> is a distributed, translation-oriented research collective working at the intersection of programmable nanomaterials, 
autonomous fabrication, and regenerative medicine. We connect molecular design, AI-guided discovery, and field-deployable devices—from 
handheld electrospinning and optical nanosensors to molecularly imprinted recognition interfaces and encapsulated therapeutic cargo. 
Our ethos is simple: design at the smallest scale, validate at the system level, and translate with intent.</p>

<p>Hylogenesis—from <i>hyle</i> (matter) and <i>genesis</i> (coming-into-being)—reflects our interest in materials that are not merely made, 
but designed to assemble, adapt, and repair.</p>