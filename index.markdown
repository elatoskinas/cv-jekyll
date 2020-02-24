---
layout: cv
---

<header>
    <h1>Evaldas Latoškinas</h1>

    <section id="contact-details">
        {% for entry in site.data.profile.contact %}
            <div class="profile-entry">
                <i class="{{entry.icon}}"></i>
                <p>{{entry.value}}</p>
            </div>
        {% endfor %}
    </section>

    <hr>
</header>

<body>
    <section id="key-skills">
        <header>
            <h2>Key Skills</h2>
        </header>

        <ul>
            {% for skill in site.data.profile.key_skills %}
                <li>{{skill}}</li>
            {% endfor %}
        </ul>
    </section>

    <section id="technologies">
        <header>
            <h2>Technologies</h2>
        </header>

        {% for tech in site.data.profile.technologies %}
            <p class="technology-entry">{{tech}}</p>
        {% endfor %}
    </section>

    <section id="other-interests">
        <header>
            <h2>Other Interests</h2>

            <p>
                {% for interest in site.data.profile.other_interests %}
                    {{interest}} {% if forloop.last != true %} | {%endif%}
                {% endfor %}
            </p>
        </header>
    </section>
</body>