---
layout: page
title: Phones
permalink: /phones/
category: "phones"
tagline: "Analysis"
phones: ["AA", "AE", "AH", "AO", "AW", "AY", "B", "CH", "D", "DH", "EH", "ER", "EY", "F", "G", "HH", "IH", "IY", "JH", "K", "L", "M", "N", "NG", "OW", "OY", "P", "R", "S", "SH", "T", "TH", "UH", "UW", "V", "W", "Y", "Z", "ZH"]

---

<div class="abstract">
    <h1>Description</h1>
    <p>
    In this section we display the mean pose of the tongue, lips, and jaw per phone. In our work we used 39 phones without stress from CMUDict. To calculate the pose per phone, first we obtained the sequence of poses per phone by tagging the sequences through
    Montreal Forced Aligner. Then we obtained the mid pose from each phone sample's sequence, and finally we obtain the mean pose per phone. The frontal and sagittal views of each phone are shown in the following figures:
    </p>
</div>

<div class="gallery">
    <h1>Visualization</h1>
</div>

{% for phone in page.phones %}
<div class="phone-display" style="margin-top:5px;margin-bottom:5px">
    <h3>{{phone}}</h3>
    <div style="float:left;margin-right:5px;">
        <a href="{{site.url}}/{{site.baseurl}}/images/phones/{{phone}}_frontal.png" target="_blank">
            <img src="{{site.url}}{{site.baseurl}}/images/phones/{{phone}}_frontal.png" height="365" width="365"  />
        </a>
        <p style="text-align:center;">frontal view</p>
    </div>
    <div style="float:left;margin-right:5px;">
        <a href="{{site.url}}/{{site.baseurl}}/images/phones/{{phone}}_sagittal.png" target="_blank">
            <img src="{{site.url}}{{site.baseurl}}/images/phones/{{phone}}_sagittal.png" height="365" width="365" />
        </a>
        <p style="text-align:center;">sagittal view</p>
    </div>
</div>
<br>
<hr>
{% endfor %}