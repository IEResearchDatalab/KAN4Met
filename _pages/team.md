---
layout: archive
title: "Team"
permalink: /team/
author_profile: true
---

<!-- Base path for assets -->
{% include base_path %}

<!-- My external stylesheet -->
<link rel="stylesheet" href="{{ base_path }}/assets/css/team.css">

<!-- Display team members -->
<div class="team-members flex-container">
    {% assign sortedMembers = site.team | sort: 'priority'%}
    {% for member in sortedMembers %}
        <div class="team-member">
            <a href="{{ member.profile }}" target="_blank" rel="noopener noreferrer">
                <img src="{{ member.image }}" alt="{{ member.name }}">
            </a>
            <h2 style="font-size: 18px;">{{ member.name }}</h2>
            <p style="font-size: 14px;">{{ member.affiliation }}</p>
        </div>
    {% endfor %}
</div>
