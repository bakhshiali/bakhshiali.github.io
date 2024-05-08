---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}
<script> const expandElements = shouldExpand => {
        let detailsElements = document.querySelectorAll("details");
        
        detailsElements = [...detailsElements];

        if (shouldExpand) {
            detailsElements.map(item => item.setAttribute("open", shouldExpand));
        } else {
            detailsElements.map(item => item.removeAttribute("open"));
        }
    };</script>
<button style="position: fixed; border: 0 solid #e5e7eb; box-shadow: -6px 8px 10px rgba(81,41,10,0.1),0px 2px 2px rgba(81,41,10,0.2); background-image: linear-gradient(to bottom, #fff, #f8eedb); right: 1px; top:210px; border-radius: .5rem" onClick="expandElements(true)">+All</button>
<button style="position: fixed; border: 0 solid #e5e7eb; box-shadow: -6px 8px 10px rgba(81,41,10,0.1),0px 2px 2px rgba(81,41,10,0.2); background-image: linear-gradient(to bottom, #fff, #f8eedb); right: 1px; top: 250px; border-radius: .5rem" onClick="expandElements(false)">-All</button>
Quote: "Passionate about Research and Innovation"

Contact Info
======

|Tel: 		| 0098-9014122529 |
|:--------|:-------:|
|Email 1: 	|<a href="alibakhshi255255@gmail.com">alibakhshi255255@gmail.com</a>|
|Email 2:	|<a href="ali_bakhshi@alumni.iust.ac.ir">ali_bakhshi@alumni.iust.ac.ir</a>|
|Email 3:	|<a href="ali_bakhshi@ipm.ir">ali_bakhshi@ipm.ir</a>|
|LinkedIn:	|<a href="https://www.linkedin.com/in/ali-bakhshi-/">https://www.linkedin.com/in/ali-bakhshi-/</a>|

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Education
======

|Level|University / High school  | GPA , Rank|Year|
|:--------|:-------:|:-------:|:-------:|
|M.Sc.	|"[Iran University of Science and Technology](https://www.iust.ac.ir/en)", Tehran, Iran<br>Nanotechnology-Nanomaterials, Tuition Waiver, Research grant<br><b>Thesis</b>: Manufacturing and evaluation of optical fiber based magnetic field sensor containing graphene-magnetite hybrid coating <br> Supervisor: [Dr. Maisam Jalaly](https://www.iust.ac.ir/content/34106/Dr.-Maisam-Jalaly), score: high:=20  |17.48/20 (3.66/4.0), 1st student |2018-2020| 
|B.Sc.|"[University of Tabriz](https://tabrizu.ac.ir/en)", Tabriz, Iran<br>Engineering Physics (Plasma, Laser, Solid State)<br><b>Thesis</b>: The mechanism of plasma enhanced chemical vapor deposition (PECVD) and its applications<br>Supervisor: Dr. Laya Shahrassai, score: high:=20 |15.67/20 (3.28/4.0), 4th student |2014-2018| 
|Pre-university<br>High school|Shahid Hemat governmental leading school (Magnet school), Tehran, Iran<br>Mathematics and Physics, Tuition Waiver|17.88/20 (3.84/4.0)<br>19.03/20 (4.0/4.0)|2014<br>2013|
|High school| Shahid Bakeri governmental leading school*, Mianeh, East Azerbaijan<br>Mathematics and Physics, Tuition Waiver |-| 2010-2012|
|Middle school| Ostad Shahriar, governmental leading school*, Mianeh, East Azerbaijan<br>1st rank student, Tuition Waiver|4.0/4.0, 1st student| 2007-2010|

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Publications
======

|Title|Publisher|Date|
|:--------|:-------:|:-------:|{% for publication in site.publications reversed %}{% if publication.title %}
| <a href="{{publication.url}}">{{publication.title}}</a> | {{publication.venue}} | {{publication.date  | date_to_long_string: "ordinal", "US"}} |{% endif %}{% endfor %}

<details>
    <summary>Show details (In-progress, submitted, never published, accepted, and translations)</summary>

Wikipedia articles (nanotechnology, biotechnology, quantum physics, …)<br>

Never published:
<ul>
<li>Chitosan-PVA nanofibers antibacterial activity against resistant bacteria</li>
</ul>

Submitted articles:
<ul>
<li>Nanofiber concentrator electrospinning device</li>
<li>Safarzadeh, M., Aghajari, AA., Rahimi, M., Maleki, F., Ghiyabi, E., Rezanezhad, A., Bakhshi, A., Salari, E., Shayesteh, H., Mohammadi, H. (2023). Recent Progress on Advanced Solid Adsorbents for CO2 Capture: From Mechanism to Machine Learning.</li>
<li>Safarzadeh, M., et al., Bakhshi, A. (2024). Porous Carbon: Stupendous Structure with Great Potential for Wide Applications.</li>
</ul>

Accepted Chapters:
<ul>
<li>Naghib, SM., Bakhshi, A., History, Introduction and Types of Quantum Dots, Elsevier, 2023.</li>
<li>Naghib, SM., Bakhshi, A., Synthesis Methods of Quantum Dots, Elsevier, 2023.</li>
<li>Naghib, SM., Bakhshi, A., Quantum Dots for Enhanced Wound Healing, Elsevier, 2023.</li>
<li>Naghib, SM., Bakhshi, A., Quantum Dots as an Advanced Nano System for Cancer Theranostics, Elsevier, 2023.</li>
<li>Bakhshi, M., Naghib, SM., Ahmadi, B., Bakhshi, A., Gold Nanoparticles Based Antibacterial and Antiviral Functional Materials, ACS, 2023.</li>
<li>Naghib, SM., Bakhshi, A., Light-Triggered Micro/Nano Drug Delivery, CRC Press, 2023.</li>
<li>Naghib, SM., Bakhshi, A., Nanotechnology based Light Materials for Bioimplant, Elsevier, 2024.</li>
<li>Naghib, SM., Bakhshi, A., Synthesis Techniques of Smart Coatings, Elsevier, 2024.</li>
<li>Bakhshi, A., Naghib, SM., Rabiee N., Antibacterial and Antiviral Nanofibrous Membranes, ACS, 2024.</li>
<li>Bakhshi, A., Bakhshi, M., Ahmadi, B., Rahdar, A., Multifunctional Theranostic Nanomedicine for Infectious Diseases, Elsevier, 2024.</li>
</ul>
Books:
<ul>
<li>Principles of Regenerative Medicine, 3rd ed.-10 chapter-under editing (English-to-Persian translation, Dr. Reza Moghadasali, Royan Institute)</li>
<li>Nanotechnology and Quantum computers (Persian)-3 of 7 chapters are prepared</li>
<li>From Research to Invention (Persian)-3 of 20 chapters are prepared</li>
</ul>

</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Patents
======

|Patent|Patent No.|Date|
|:--------|:-------:|:-------:|{% for patent in site.patents reversed %}{% if patent.title %}
| <a href="{{patent.url}}">{{patent.title}}</a> | <a href="{{patent.paperurl}}">{{patent.excerpt | split:'Patent No. : '}}</a> | {{patent.date  | date_to_long_string: "ordinal", "US"}} |{% endif %}{% endfor %}

<details>
    <summary>Show details (Filed, never filed and trade secrets)</summary>
	
Filed (Issuing):
<ul>
<li>Novel Cold Plasma system, 2022 </li>
</ul>
note: real title of issuing patents would differ! <br>

Never filed:
<ul>
<li>Plasma-assisted cross-link of polymers (idea-level) (IPM)</li>
<li>Plasma-assisted electrospinning (idea-level) (IPM)</li>
<li>Fabrication of multi-nozzle solution blow electrospinning (SBS) (IPM)</li>
<li>Controllable spark discharge-assisted nanoparticle/nano-alloy synthesis device (IPM)</li>
<li>Smart food spoilage label & sensing device (IPM)</li>
<li>Thick PMMA polymer formulation (IPM)</li>
<li>Industrial level agricultural PAW production design (IPM)</li>
<li>Reusable microneedle patch (idea-concept route) (self-desired)</li>
<li>Fabrication of precise optical fiber tapering device (IUST)</li>
<li>Optical fiber tapering system using motorized CCD and image processing (IUST)</li>
<li>Raman-based quality control of pharmaceutical products (BP and idea level) (IUST)</li>
<li>Special shoes to run on sands (design level) (IUST)</li>
<li>Air purifier filter & gadget using plasma + titania (idea-level) (INIC & Iran khodro)</li>
<li>Medical plants/herbs AI & database (IUST-Tabriz medical university)</li>
<li>CCD array spectrum & plasma bullet analyzer (Tabriz) </li>
</ul>
note: real name of inventions would differ! <br>

Trade secrets:
<ul>
<li>Dye removal from woven fabrics & waste water (Azar sky co.)</li>
</ul>

</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Research Experience
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
		<th>No.</th>
                <th>Organization</th>
                <th>Role</th>
		<th>Date</th>
            </tr>
        </thead>
        <tbody>
		{% assign i = 0 %}
		{% for org in site.data.cv.researchprojects %}
		{% assign i = i | plus:1 %}
		<tr>
			<td>{{i}}</td>
			<td>{{org.organization}}</td>
			<td>{{org.role}}</td>
			<td>{{org.date}}</td>
		</tr>
		<td style=" text-align :left;" colspan="4"><b>Outputs</b><br>{{org.outputs}}</td>
		{% endfor %}
        <!-- Add more rows as needed -->
        </tbody>
	</table>
</details> 

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Skills
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
	{% for skill in site.data.cv.skills %}
	<p style="text-align:center; margin-bottom: 1px; margin-top: 2px;"><b>{{skill.title}}</b></p>
    <p style="margin-bottom: 5px; margin-top: 1px;">{{ skill.skills | newline_to_br }}</p>
	{% endfor %}
</details> 

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Teaching
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Title</th>
                <th>Organization</th>
				<th>Date</th>
            </tr>
        </thead>
        <tbody>
       {% for class in site.teaching reversed %}
		<tr>
			<td><a href="{{class.url}}">{{class.title}}</a></td>
			<td>{{class.venue}}</td>
			<td>{{class.date  | date_to_long_string: "ordinal", "US"}}</td>
		</tr>
		{% endfor %}
			
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>  

Services, leaderships & Memberships
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Title</th>
                <th>Organization</th>
		<th>Date</th>
            </tr>
        </thead>
        <tbody>
       {% for mem in site.data.cv.memberships %}
		<tr>
			<td>{{mem.title}}</td>
			<td>{{mem.organization}}</td>
			<td>{% if mem.date %} {{mem.date}} {% endif %}</td>
		</tr>
		{% endfor %}	
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Languages
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Language</th>
                <th>Level</th>
            </tr>
        </thead>
        <tbody>
       {% for lan in site.data.cv.languages %}
		<tr>
			<td>{{lan.language}}</td>
			<td>{{lan.level}}</td>
		</tr>
		{% endfor %}
			
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Certificates (Only notables, Complete list in [LinkedIn](https://www.linkedin.com/in/ali-bakhshi-/))
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Title</th>
                <th>Organization</th>
		<th>Ref.</th>
		<th>Date</th>
            </tr>
        </thead>
        <tbody>
       {% for cert in site.data.cv.certificates %}
		<tr>
			<td>{{cert.title}}</td>
			<td>{{cert.organization}}</td>
			<td>{% if cert.ref%} <a href="{{cert.ref}}">ref 1</a> {% endif %}</td>
			<td>{% if cert.date%} {{cert.date  | date_to_long_string: "ordinal", "US"}} {% endif %}</td>
		</tr>
		{% endfor %}
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

Softwares
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Software</th>
                <th>Level</th>
            </tr>
        </thead>
        <tbody>
       {% for software in site.data.cv.softwares %}
		<tr>
			<td>{{software.name}}</td>
			<td>{{software.level}}</td>
		</tr>
		{% endfor %}
			
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

<!-- Honors & Awards & Grants --------------------------------------------------------------------------------- -->

Honors & Awards & Grants
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
<table>
        <thead>
            <tr>
                <th>Title</th>
                <th>Organization / Honor</th>
                <th>Date</th>
            </tr>
        </thead>
        <tbody>
		{% for honor in site.data.cv.honors %}
		<tr>
			<td>{{honor.title}}</td>
			<td>{{honor.organization}}</td>
			<td>{{honor.date}}</td>
		</tr>
		{% endfor %}
		</tbody>
	</table>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

<!-- Social and extracurricular activities ------------------------------------------------------- -->

Social and extracurricular activities
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
<ul>
<li>Business coaching and due diligence</li>
<li>Patent engineering (attroney, filing, drafting, and consulting)</li>
<li>Patent Analysis (landscapes, searching, clustering, visualization, and interpretation)</li>
<li>Study of Quantum computers (SET qubit, photon entanglement, quantum holography, and error correction)</li>
<li>Innovation in Cold plasma technologies (synthesis, modification, and coating)</li>
<li>Nano and quantum teaching</li>
<li>Study of biology and genetics</li>
<li>Website, application and program design</li>
<li>Molecular dynamics teaching</li>
<li>Consulting for fabrication of nanomaterial production and analysis system</li>
<li>Analysis of nanomaterials</li>
<li>Analysis of disk diffusion, real time PCR, MBC, MIC, …</li>
<li>Genetic data mining (Bleeding-edge)</li>
<li>Robotic competitions refereeing</li>
</ul>
</details>

<div class="wrapper">
	<div class="divider div-transparent div-dot"></div>
</div>

<!-- References -------------------------------------------------------------------------------- -->

References
======

<details>
    <summary>Show details</summary>
    <!-- Your content goes here -->
    <table>
        <thead>
            <tr>
                <th>Name</th>
                <th>Position</th>
                <th>Affiliation(s)</th>
				<th>Email</th>
				<th>Relation(s)</th>
            </tr>
        </thead>
        <tbody>
       {% for ref in site.data.cv.references %}
		<tr>
			<td><a href="{{ref.link}}">{{ref.name}}</a></td>
			<td>{{ref.position}}</td>
			<td>{{ref.affiliation}}</td>
			<td>{% if ref.email %} <a href="mailto:{{ref.email}}">Email 1</a>{% endif %}</td>
			<td>{{ref.relation}}</td>
		</tr>
		{% endfor %}
			
            <!-- Add more rows as needed -->
        </tbody>
    </table>
</details>
