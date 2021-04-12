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

    This section displays the tongue, lips, and jaw pose from our data on a phone level basis. In our work, we used 39 phones without stress from CMUDict as we obtained the sequence of poses per phone by tagging the mocap sequences through the Montreal Forced Aligner. Then we obtained the mid pose from each phone's samples' sequences. Finally, we computed the mean pose per phone from all the mid poses. 
</div>
<br>
<div class="gallery">
    <h1>Visualization</h1>
    In this section we visualize the frontal and sagittal views of each phones mean mid pose. The colored spheres represent the sensors, the red mesh represents the tongue, the palate's surface is an approximation from three sagittal and coronal traces. The lips and jaw are just displayed for reference and do not represent their actual size.
</div>
<br>
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