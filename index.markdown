---
layout: cv
---

<header>
    <h1>Evaldas Latoškinas</h1>

    <section id="contact-details">
        {% for entry in site.data.profile.contact %}
            <div class="profile-entry">
                <i class="{{entry.icon}}"></i>
                <p>
                    {% if entry.link %}
                        <a href="{{entry.link}}">{{entry.value}}</a>
                    {% else %}
                        {{entry.value}}
                    {% endif %}
                </p>
            </div>
        {% endfor %}
    </section>

    <hr>
</header>

<main>
    <section id="work-experience">
        <header>
            <h2>Experience</h2>
        </header>

        <ul class="timeline">
            {% for work in site.data.profile.work_experience %}
                <li class="work-entry">
                    <span class="timeline-line"></span>
                    {% include experience.html %}
                </li>
            {% endfor %}
        </ul>
    </section>


    <section id="education">
        <header>
            <h2>Education</h2>
        </header>

        {% for edu in site.data.profile.education %}
            <div class="education-entry">
                <h3>{{edu.name}}</h3>
                <p class="date">{{edu.start_date}} - {{edu.end_date}}</p>
                <p class="date">Expected graduation: {{edu.expected_graduation}}</p>
                <p>{{edu.degree}}</p>
                <p>GPA: {{edu.gpa}}</p>
            </div>
        {% endfor %}
    </section>

    <section id="technologies">
        <header>
            <h2>Technologies</h2>
        </header>

        {% for tech in site.data.profile.technologies %}
            <p class="technology-entry">{{tech}}</p>
        {% endfor %}
    </section>

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

    <section id="projects">
        <header>
            <h2>Projects</h2>
        </header>

        <ul class="timeline">
            {% for work in site.data.profile.projects %}
                <li class="work-entry">
                    <span class="timeline-line"></span>
                    {% include experience.html %}
                </li>
            {% endfor %}
        </ul>
    </section>
</main>