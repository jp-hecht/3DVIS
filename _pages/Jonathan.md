---
title: "Bericht von Jonathan Hecht"
permalink: /Jonathan/
toc: true
toc_label: "Inhaltsverzeichnis"
author_profile: 
  name: "Jonathan Hecht"
  avatar: "/assets/images/JPH/jph.png"
  bio: "M.Sc. Geodäsie und Geoinformatik"
  location: "Hamburg, Germany"
  links:
    - label: "Mastodon"
      icon: "fa-brands fa-mastodon"
      url: "https://mastodon.social/@jphecht"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/jp-hecht"
excerpt: "Außenbereich und Umgebung der Ohlendorff’schen Villa"
header:
  overlay_image: "/assets/images/JPH/villa_sketch.jpg"
  caption: "Bildquelle: [**ohlendorffsche.de**](https://ohlendorffsche.de/historie/)"
  overlay_filter: 0.5
---

# Einleitung
Die Ohlendorff'sche Villa übernimmt im Hamburger Stadtteil Volksdorf eine hervorgehobene Stellung im urbanen Gefüge, welche insbesondere durch die Zentralität im Stadtteil, sowie die Betonung des Gebäudes durch den umschließenden Park gegeben ist. Um diesen Besonderheiten auch außerhalb einer vor Ort Begehung erfahrbar zu machen und somit die Villa für diverse Menschen zugänglich zu machen, wurde im Rahmen des Kurses 3D-Visualisierung an der HafenCity Universität von Herrn Prof. Kersten eine Virtual Reality (VR) Anwendung zur Ohlendorff'schen Villa entwickelt. Ziel ist es ein zur Verfügung gestelltes historische Gebäude für eine interaktive Begehung und Visualisierung aufzubereiten.
{: style="text-align: justify;"}
Innerhalb der letzten Jahrzehnte ist die Bedeutung von VR Anwendungen durch die geschaffene multisensorische 3D Umwelt in verschiedenen Feldern gestiegen[^1]. Typische Anwendungsbereiche umfassen unter anderem die Psychologie, Simulatoren, Operationen, Lernumgebungen, körperliche Prävention oder in der Industrie[^4]. Innerhalb der Architektur, Ingenieurwesen und Konstruktion ermöglichen VR Anwendungen die Immersion von Nutzenden in eine virtuelle Welt, welche den hohen Anforderungen der visuellen Kommunikation in Bezug auf Design, Konstruktion und Management der gebauten Umwelt ermöglicht[^1]. Entsprechend wird die insbesondere die Simulation der realen Welt angestrebt. Erste Versuche von VR Applikationen für die bebaute Umwelt wurden zwar bereits in den 1990er Jahren getestet, jedoch erfolgte eine größere Verbreitung durch praktische Anwendungen erst in den letzten Jahren durch eine Reduktion von Einstiegshürden mittels leistungsfähigerer Hard- und Software. Beispiele für praktische Anwendungen können Kundenbegehungen oder die schrittweise Überprüfung von Bauabläufen sein[^2].
{: style="text-align: justify;"}

Bevor jedoch tiefer in das Thema, sowie das studentische Projekt eingegangen wird, sollte das Verständnis des Begriffes VR offengelegt werden. Eingeordnet werden kann der Begriff in das übergeordnete Thema des Realitäts-Virtualitäts-Kontinuums[^3]. Dabei wird davon ausgegangen, dass sich Augmented Reality (AR), Augmented Virtuality (AV) und VR zwischen den Endpolen physischen Realität und vollständig virtuellen Umgebung befinden[^5]. AR, AV und VR werden dabei unter dem Begriff *extended reality* (XR) zusammengefasst, welches „[...] alle realen und virtuellen kombinierten Umgebungen und Mensch-Maschine-Interaktionen, die durch Computertechnologie und Wearables erzeugt werden“ umfasst[^6]. Vor diesem Hintergrund wurden verschiedene Definition im wissenschaftlichen Kontext erarbeitet, welche nicht im Detail erläutert werden sollen und einzig auf das hier zugrundlegendes Verständnis dargelegt werden soll:

> VR leverages immersive technologies to simulate interactive virtual environments or virtual worlds with which users become subjectively involved and in which they feel physically present[^5]

Basierend auf diesem Verständnis wird im folgenden Bericht zunächst das reale Objekt beschrieben, sowie die Entscheidung des Modelles begründet. Im Anschluss folgt die Konzeption unserer VR Anwendung, weitere theoretische Überlegungen zur Anwendung und die verwendete Hard- und Software. Nachdem die Vorraussetzungen festgelegt wurden, wird die Umsetzung, sowie die Limitierungen samt Fazit/Ausblick aufgezeigt. Innerhalb dieses Berichtes wird insbesondere die Entstehung des Außenbereiches, samt aller dazugehörigen Elemente aufgegriffen. Für andere Bereiche, wie beispielsweise die Texturierung des Gebäudes, werden erwähnt, aber detailierter in den anderen Berichten aufgegriffen.

# Ohlendorff'sche Villa
## Realität
* Auch auswahl hier begründen vlt. schon der konzeption vorgreifen
* Grundlagen, wo was wie
* Historie
  * Architekt
  * Auftrageber
  * Stil
  * Lage

* Uni Projekt mit möglichen Modellen
* Auswahl von Villa Ohlsdorff
  * Alter stil schwierig
  * Nahe zu hamburg
  * hohe flexibilität

* Weiterer Aufbau des Aritkels
  * FOkuspunkt hier ist der Außenebereich und Umgebung
## Bestehendes Modell
* Verweis auf andere Berichte
* Wurde in rohform zur verfügung gestellt

# Hauptteil
## Konzeption
* Idee
  * Kartenähnlich
  * Kein Fokus auf realistische Darstellung der Umgebung
  * Warum Platte
## Theoretische Überlegungen
* [Immersion, Presence, and Interaction | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/875)
## Statische Dinge
* Warum Platte als Baseline
* Dann Gebäude
* Straßen
* Bedeckung anch Karte
* Immersionsobjekte
  * Bäume/Büsche/Steine
  * Autos
  * Lichter
## Animation & Interaktionen
* Jeweils mit erklärung
* Wind
* UMgebungsgeräusche
* Autos
  * Geräusche
  * Pfad folgen
* Licht bzw. Tag Nacht
* Teleportation
* Geräusche im Gebäude
## Möglichkeiten zur VR-Umsetzung

### Positiv
* Sehr hohe Frames

### Einschränkungen
* Wind
* Nebel
### Software
Umgesetzt wurde die Anwendung in wesentlichen mit drei Software Produkten, die über die Entwicklung des VR Projekt verwendet wurden. 

* THeoretischer Vergleich unterschiedlicher Möglicher software pakete &rarr; VIelfalt aufzeigen
* Blender
  * Datenmanipulation samt Texturierung
  * Blender GIS: Handling von Geodaten 
  * Blender Plugins für autos &rarr; Bewegliche Reifen, Theoretisch Fahrbare Autos

* Export als FBX zu unreal
* UE5
  * Import
  * Modellierung von Animation & Interaktionen
  * Plugin für Sonne als eigene Software für speziellen Blueprint
* Steam VR: Übertragung auf Hardware


### Hardware
* Theoretische viele möglichkeiten bei uns an der uni
* [HTC Vive | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/861)
* mit den bestandteilen für xyz
* den specs

# Fazit & Ausblick

# Literatur

# Notes
* Bericht auch in Präsentation verlinken
* Wie ist unser Umgang mit den anderen berichten
* Wie landing page & und about?
* Fehlt euch sonst noch etwas?
* MUSIK fehlt noch
* Am anfang workflow aufstellen dem anschließend gefolgt wird &rarr; konnte keine quelle dafür finden bzw. kein guidelines
  * Anforderungen bzw. Vorgaben &rarr; Produktanforderungen
  * Konzeption &rarr; Produktanforderungen
  * Input Daten &rarr; Geodaten / Verfügbare Daten / Modelle aus dem netz
  * 3D Modellierung Software &rarr; Blender
  * 3D Application building software/ game engine &rarr; UE5
  * Target Platform &rarr; Vive / VR BRILLE
  * Präsentationsplatform &rarr; Steam
  * [2.6 3D and VR Application Building Workflows | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/559)

# Literature
* Virtual reality applications for the built environment: Research trends and opportunities 
  * first vr for built environment in the 1990s
  * technische möglichkeiten haben die relevanz und praktikalibilität gesteigert
  *  In the context of this research, virtual reality refers to the uses of computer science and behavioral interfaces to simulate the behavior of 3D objects in a virtual world, enabling real-time interactions with each other in pseudo-natural immersion via sensorimotor channels 
  * Different devices could deliver such an experience &rarr; ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/vr_devices.png)


* Kim MJ, Wang X, Love PED, Li H, Kang SC (2013). Virtual reality for the built environment: a critical review of recent advances, ITcon Vol. 18, pg. 279-305, https://www.itcon.org/2013/14
  * > Over the past decades, virtual reality (VR) technology has been increasingly recognized by the architectural, engineering, and construction (AEC) industry for its ability to provide multisensory three- dimensional (3D) environments that immerse the user in a virtual world, specifically to fulfill the high demand for visual forms of communication during the work related to designing, engineering, construction, and management of the built environment 


* Definition VR
  * [VR | Bedeutung im Cambridge Englisch Wörterbuch](https://dictionary.cambridge.org/de/worterbuch/englisch/vr): abbreviation for virtual reality: a set of images and sounds, produced by a computer, that seem to represent a place or a situation that a person can take part in: the VR experience
  * Paul Milgram, Haruo Takemura, Akira Utsumi, and Fumio Kishino "Augmented reality: a class of displays on the reality-virtuality continuum", Proc. SPIE 2351, Telemanipulator and Telepresence Technologies, (21 December 1995); https://doi.org/10.1117/12.197321: 
    * > Virtual reality (VR) is a simulated experience that employs 3D near-eye displays and pose tracking to give the user an immersive feel of a virtual world. Applications of virtual reality include entertainment (particularly video games), education (such as medical, safety or military training) and business (such as virtual meetings). VR is one of the key technologies in the reality-virtuality continuum. As such, it is different from other digital visualization solutions, such as augmented virtuality and augmented reality


* Bedeutung Geoinformatics / Visualisierung räumlicher daten: [1.3 3D Modeling and VR in the Geospatial Sciences | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/800)
Geoinformatik und Geodäsie sind dabei eng mit VR und 3D Modellierung verbunden. 
3D Stadtmodelle haben in den letzten Jahren an Bedeutung für diverse Anwendungen gewonnen in den GIScience [^7]
* Beudeutung für städte: Biljecki, F., Stoter, J., Ledoux, H., Zlatanova, S., & Çöltekin, A. (2015). Applications of 3D City Models: State of the Art Review. ISPRS International Journal of Geo-Information, 4(4), 2842–2889. doi:10.3390/ijgi4042842
# Testing

<script type="module" src="https://unpkg.com/@google/model-viewer@latest"></script>
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />


<style>
    /* Ensure the map and 3D viewer have fixed sizes */
    .content-container {
        max-width: 800px; /* Adjust to your needs */
        margin: 0 auto; /* Centering */
    }

    .map-container {
        width: 100%;
        height: 40vh; /* Responsive height */
        border: 1px solid #ccc; /* Optional border */
    }
</style>

<div class="content-container">
    <div id="map" class="map-container"></div>

    <script>
        document.addEventListener("DOMContentLoaded", function () {
            var map = L.map('map').setView([53.648437464598516, 10.165957827843153], 13);

            // Add a tile layer (OpenStreetMap)
            L.tileLayer.wms('https://sgx.geodatenzentrum.de/wms_basemapde', {
                layers: 'de_basemapde_web_raster_grau',
                format: 'image/png',
                transparent: true,
                attribution: '&copy; GeoBasis-DE / BKG (2025)'
            }).addTo(map);

            // Define a polygon (example coordinates)
            var marker = L.marker([53.648437464598516, 10.165957827843153]).addTo(map);
        });
    </script>
</div> 

<model-viewer 
    src="{{ site.url }}{{ site.baseurl }}/assets/model/BaseFill.glb"
    alt="3D model"
    camera-controls 
    auto-rotate
    exposure="1"
    shadow-intensity="1"
    ar
    style="width: 100%; height: 40vh;">
</model-viewer>
<model-viewer 
    src="{{ site.url }}{{ site.baseurl }}/assets/model/Base.glb"
    alt="3D model"
    camera-controls 
    auto-rotate
    exposure="1"
    shadow-intensity="1"
    ar
    style="width: 100%; height: 40vh;">
</model-viewer>

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Car_Move_Opt.gif)


![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d_con.drawio.svg)
![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d.drawio.svg)
*Caption of my image*


[^1]: Kim MJ, Wang X, Love PED, Li H, Kang SC (2013). Virtual reality for the built environment: a critical review of recent advances, ITcon Vol. 18, pg. 279-305, https://www.itcon.org/2013/14
[^2]: https://www.sciencedirect.com/science/article/abs/pii/S0926580520301394
[^3]: Milgram, Paul; H. Takemura; A. Utsumi; F. Kishino (1994). "Augmented Reality: A class of displays on the reality-virtuality continuum". Proceedings of SPIE - The International Society for Optical Engineering Vol. 2351
[^4]: Artur Becker and Carla M. Dal Sasso Freitas. 2023. Evaluation of XR Applications: A Tertiary Review. ACM Comput. Surv. 56, 5, Article 110 (May 2024), 35 pages. https://doi.org/10.1145/3626517
[^5]: Wohlgenannt, I., Simons, A. & Stieglitz, S. Virtual Reality. Bus Inf Syst Eng 62, 455–461 (2020). https://doi.org/10.1007/s12599-020-00658-9
[^6]: Übersetzt aus: Fast-Berglund Å, Gong L, Li D (2018) Testing and validating extended reality (xR) technologies in manufacturing. Procedia Manuf 25:31–38
[^7]: Biljecki, F.; Stoter, J.; Ledoux, H.; Zlatanova, S.; Çöltekin, A. Applications of 3D City Models: State of the Art Review. ISPRS Int. J. Geo-Inf. 2015, 4, 2842-2889. https://doi.org/10.3390/ijgi404284
