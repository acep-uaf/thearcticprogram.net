---
layout: page
show_meta: false
title: "Alaska Regional Collaboration for Innovation and Commercialization (ARCTIC) Program"
subheadline: "About the project and partners"
teaser: "An Office of Naval Research initiative"
#header:
#   image_fullwidth: "header_homepage_13.jpg"
permalink: "/about/"
---

The Alaska Regional Collaboration for Technology Innovation and Commercialization (ARCTIC) is a collaboration designed to promote commerce and partnerships between Alaska and the Arctic and Pacific regions through advancements in energy through resiliency research, technology development/deployment and education.

The ARCTIC Program is an  [Office of Naval Research](https://www.onr.navy.mil/) (ONR)  Initiative and through their support the ARTIC project partners are able to promote partnerships with Arctic and Pacific nations for the open exchange of technology advancements and educational activities. The current ONR ARCTIC funding is focused on **Energy Resiliency**.   

The core mission of ARCTIC is to build capacity and support a thriving economy, centered on expertise in the energy sector, and related areas of emphasis (i.e. food, water).

Build human resource capacity and industrial capabilities in energy and resiliency through promoting commerce and partnerships in the Arctic and Pacific regions and advancing resource technology (energy, food, water, waste management) education, research, development, demonstration, and deployment.

This includes fostering relationships between world-leading U.S. research institutions; advancing U.S. economic base by providing technologies that meet Arctic and Pacific needs; and promoting Arctic and Pacific region talent development and education (certificate to advanced degrees) through these activities, ARCTIC promotes partnerships with Arctic and Pacific nations for the open exchange of technology advancements and educational opportunities.

The ARCTIC Program members want a strong future for Alaskans by providing opportunities to live and work in Alaska with interesting jobs that connect to a global economy.  We want smart people in Alaska solving local problems and connecting them global networks.

## ARCTIC Program members

{% for partner in site.partners %}
## [{{partner.name}}]({{ partner.url }}) - {{partner.tagline}}
{% endfor %}
