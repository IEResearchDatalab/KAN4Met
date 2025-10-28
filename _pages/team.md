---
layout: archive
title: "Team"
permalink: /team/
author_profile: true
---

{% include base_path %}

<!-- My external stylesheet -->
<link rel="stylesheet" href="{{ base_path }}/assets/css/team.css">

<!-- Display team members -->
<div class="team-members flex-container" style="display: flex; flex-wrap: wrap; justify-content: space-between;">
    {% assign sortedMembers = site.team | sort: 'priority'%}
    {% for member in sortedMembers %}
        <div class="team-member" style="flex: 0 0 30%; box-sizing: border-box; padding: 10px; text-align: center;">
            <a href="{{ member.profile }}" target="_blank" rel="noopener noreferrer">
                <img src="{{ member.image }}" alt="{{ member.name }}" style="border-radius: 50%; width: 100px;">
            </a>
            <h2 style="font-size: 18px;">{{ member.name }}</h2>
            <p style="font-size: 14px;">{{ member.affiliation }}</p>
        </div>
    {% endfor %}
</div>
