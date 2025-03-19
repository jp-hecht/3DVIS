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
Innerhalb der letzten Jahrzehnte ist die Bedeutung von VR Anwendungen durch die geschaffene multisensorische 3D Umwelt in verschiedenen Feldern gestiegen[^1]. Typische Anwendungsbereiche umfassen unter anderem die Psychologie, Simulatoren, Operationen, Lernumgebungen, Sport oder in der Industrie[^4]. Innerhalb der Architektur, Ingenieurwesen und Konstruktion ermöglichen VR Anwendungen die Immersion von Nutzenden in eine virtuelle Welt, welche den hohen Anforderungen der visuellen Kommunikation in Bezug auf Design, Konstruktion und Management der gebauten Umwelt ermöglicht[^1]. Entsprechend wird die insbesondere die Simulation der realen Welt angestrebt. Erste Versuche von VR Applikationen für die bebaute Umwelt wurden zwar bereits in den 1990er Jahren getestet, jedoch erfolgte eine größere Verbreitung durch praktische Anwendungen erst in den letzten Jahren durch eine Reduktion von Einstiegshürden mittels leistungsfähigerer Hard- und Software. Beispiele für praktische Anwendungen können Kundenbegehungen oder die schrittweise Überprüfung von Bauabläufen sein[^2].
{: style="text-align: justify;"}
Bevor jedoch tiefer in das Thema, sowie das studentische Projekt eingegangen wird, sollte das Verständnis des Begriffes VR offengelegt werden. Eingeordnet werden kann der Begriff in das übergeordnete Thema des Realitäts-Virtualitäts-Kontinuums[^3]. Dabei wird davon ausgegangen, dass sich Augmented Reality (AR), Augmented Virtuality (AV) und VR zwischen den Endpolen physischen Realität und vollständig virtuellen Umgebung befinden[^5]. AR, AV und VR werden dabei unter dem Begriff *extended reality* (XR) zusammengefasst, welches „[...] alle realen und virtuellen kombinierten Umgebungen und Mensch-Maschine-Interaktionen, die durch Computertechnologie und Wearables erzeugt werden“ umfasst[^6]. Vor diesem Hintergrund wurden verschiedene Definition von VR im wissenschaftlichen Kontext erarbeitet, welche nicht im Detail erläutert werden sollen und einzig auf das hier zugrundlegendes Verständnis dargelegt wird:
{: style="text-align: justify;"}
> VR leverages immersive technologies to simulate interactive virtual environments or virtual worlds with which users become subjectively involved and in which they feel physically present[^5]
{: #def}
Basierend auf diesem Verständnis wird im folgenden Bericht zunächst das reale Objekt beschrieben, sowie die Entscheidung des Modelles begründet. Im Anschluss folgt die Konzeption unserer VR Anwendung, ergänzende theoretische Überlegungen zur Anwendung und die verwendete Hard- und Software. Nachdem die Vorraussetzungen festgelegt wurden, wird die Umsetzung konkretisiert, sowie die Limitierungen samt Fazit/Ausblick aufgezeigt. Innerhalb dieses Berichtes wird insbesondere die Entstehung des Außenbereiches, samt aller dazugehörigen Elemente aufgegriffen. Andere Bereiche, wie beispielsweise die Texturierung des Gebäudes, werden erwähnt, aber detailierter in den beiden anderen Berichten aufgegriffen.
{: style="text-align: justify;"}

# Ohlendorff'sche Villa
Wie aus der [Übersichtskarte](#map1) deutlich wird und bereits angedeutet, wurde befindet sich das ehemalige großbügergliche Wohnhaus im Hamburger Stadteil Volksdorf. Im wesentlichen wird das Gebäude vom zugehörigen Park, sowie Gebäuden mit primärer Wohnfunktion eingegrenzt. 
<div class="content-container">
    <div id="map" class="map-container"></div>
    <script>
        document.addEventListener("DOMContentLoaded", function () {
            var map = L.map('map').setView([53.648437464598516, 10.165957827843153], 15);

            L.tileLayer.wms('https://sgx.geodatenzentrum.de/wms_basemapde', {
                layers: 'de_basemapde_web_raster_grau',
                format: 'image/png',
                transparent: true,
                attribution: '&copy; GeoBasis-DE / BKG (2025)'
            }).addTo(map);
            var marker = L.marker([53.648437464598516, 10.165957827843153]).addTo(map);
        });
    </script>
</div> 
*Karte 1: Verortung der Ohlendorff'sche Villa in Volksdorf.*
{: #map1}
Die historische Entwicklung wird auf der Website von der heute besitzenden Stiftung Ohlendorff’sche Villa durch Gerhard Hirschfeld beschrieben. Eine kurze Zusammenfassung wird hier aufgegriffen: Die heutige Villa wurde 1928/29 von Erich Elingius für Hans v. Ohlendorff errichtet. Dieser ließ das vorherige Gutshaus seines Vaters Heinrich v. Ohlendorff abreißen. Die neue Villa hebt sich durch ihre herrschaftliche Gestaltung hervor. Während der Abriss der eklektizistischen Villa seines Vaters dem Zeitgeist entsprach, wählte Hans v. Ohlendorff mit Elingius einen Architekten, der konservative Bauweisen bevorzugte. Besonders auffällig ist die zentrale Auffahrt mit dem hervorgehobenen Eingangsportal, das den repräsentativen Anspruch der Familie unterstreicht. Die asymmetrisch gestaltete Gartenseite wirkt wohnlicher, doch das hohe Sockelgeschoss verhindert eine direkte Verbindung zum Park. Entsprechenden der repräsentativen Funktion wurden die Zimmer im Untergeschoss als Empfangszimmer, Bibliothek, Musikzimmer und Speisezimmer gestaltet. Die obere private Etage umfasste ein großes Schlafzimmer mit Ankleidezimmer und eigenem Bad sowie einen achteckigen Frühstücksraum. Ein separater Flur für das Dienstpersonal führte zur Anrichte und zum Speisenaufzug. Der Gästebereich bestand aus zwei Fremdenzimmern mit einem gemeinsamen Bad. Die Villa zeigt sparsam eingesetzte Schmuckelemente. Werkstein-Umrahmungen betonen die Rundbogenfenster und Rechtecköffnungen, während Balkone und französische Fenster mit gusseisernen Ziergittern versehen sind.[^8]. Hans v. Ohlendorff verkaufte das Anwesen an die Stadt Hamburg im Jahr 1953, welche das Gebäude bis 2006 als Ortsamt nutzte. Im Anschluss wurde das Gebäude bis 2014 saniert und in eine Kultur- und Begegungsstätte des Stadtteils umgestaltet[^10].
{: style="text-align: justify;"}
Die Entscheidung dieses Gebäude zu gestalten, wurde unter anderem wegen der spannenden Historie getroffen. Weitere Gründe waren die Datenverfügbarkeit bzw. die Datenaufbereitung, sowie ein flexibelere Gestaltung und Stilisierung im Vergleich zu den beiden anderen vorgeschlagenen Projekten Schloss Agathenburg und Horneburg.
{: style="text-align: justify;"}
Innerhalb unterschiedlicher Kurse an der HafenCity Universität wurden diverse Daten über das Gebäude aufgenommen und durch die Kursleitung zur Verfügung gestellt. Details über das zur Verfügung gestellte Gebäude können im Bericht von Marlene nachvollzogen werden *LINK*. 
{: style="text-align: justify;"}

# Hauptteil
Konzept &rarr; also überlegungen im Vorfeld &rarr; Ergänzung durch Theorie &rarr; detials der praktischen Implementierung
## Konzeption einer VR Anwendung der Ohlendorff'sche Villa
Vorgegebenes Ziel des Projektes ist die interaktive Begehung und Visuallisierung der Ohlendorff'schen Villa. Entsprechend dieser Anforderung wurde entschlossen das Gebäude in den Mittelpunkt der virtuellen Welt zu stellen. Da jedoch die Villa insbesondere, wie bereits erwähnt, in Zusammenhang und Wirkungsgefüge mit der Umgebung steht, sollte dieses auch eingebunden werden, wobei die Fokussierung auf die Villa nicht verloren gehen sollte. Dieses kann den Nutzenden gleichzeitig ermöglichen ein besseres Verständnis für die Größenrelationen zu erlangen. Da eine großräumige Darstellung beispielsweise von gesamt Volksdorf keinen Mehrwert brächte und ein gesamter Stadtteil vom Umfang nicht gestaltet werden könnte, wurde sich entschiedenen die Villa auf einem Block darzustellen. Die Idee ein markantes Element im Raum in Blockform darzustellen, wurde inspiriert von Darstellung digitaler Geländemodelle als Block ( [Beispiele](https://www.rayshader.com/)). Bei der Wahl der Blockform wurde sich an den natürlichen Gegebenheiten vor Ort orientiert. Ziel war es die Umgebung abzubilden, ohne jedoch die Hauptsichtachsen auf die Front und Rückseite der Villa zu beschränken. In der praktischen Umsetzung erwies sich eine Kreisform als geeignet. 
{: style="text-align: justify;"}
Die Gestaltung des Außenbereiches orientiert sich an kartographischen Darstellungen, welche eher den Sehgewohnheiten der Nutzenden entsprechen, als der Versuch eine realistische Umgebung zu schaffen. Angelehnt an die kartographischen Generalisierung sollten Objekte in einem *Low Poly Stil*, also der Modellierung von Objekten durch ein Netz von wenigen verbunden Punkten, abgebildet werden. Dies ermöglicht zum einen die Performance der gesamten Anwendung deutlich zu erhöhen und zum anderen einen deutlichen Kontrast zwischen einer detailierten und realistischeren gestalteten Villa und der Umgebung herzustellen[^11]. Ein derartiger Kontrast kann bei den Nutzenden die Aufmerksamkeit erhöhen und somit die Wahrnehmung schärfen. 
{: style="text-align: justify;"}
Die Villa wurde im Gegensatz dazu detailiert modelliert und texturiert und kommt somit einer realistischen Darstellung näher. **FARBEN** TEXTUEN &rarr; Was wurde sich diesbezüglich gedacht?
Da eine vollständige und realistische Modellierung des Innenbereiches den Umfang des Projektes übersteigen würde, wurden einzig zwei Räume geschaffen, die in dieser Form in der Realität nicht existieren. Ober- und Untergeschoss wurden nicht, wie in der realen Villa, modelliert. Die zwei geschaffen Räume behandeln verschiedene Animationen und Interaktionen, die angelehnt sind an die historischen Nutzungen, aber frei interpretiert wurden. Folglich ist ein Raum als Musikzimmer gestaltet und der andere beinhaltet Kunstwerke. Neben der Anlehnung an die historischen Gegebenheiten ermöglicht dies die flexibele Umsetzung der geoforderten Interaktionen.
{: style="text-align: justify;"}

## Möglichkeiten zur VR-Umsetzung
Bevor konkrete umgesetzte Elemente beschrieben und Funktionsweisen erläutert werden können, werden sowohl die Arbeitsschritte zur Entwicklung einer VR Anwendung als auch Entscheidungen für konkrete Hard- und Software aufgegriffen.
{: style="text-align: justify;"}
### Theorie
Wie bereits aus der [Definition](#def) hervorgeht, zielt eine VR Anwendung auf die Immersion der Nutzenden in eine virtuelle Welt ab, welche gleichzeitig die Außenwelt versucht auszuschließen[^20]. Um einen hohen Immersionsgrad zu erzeugen, sollte die geschaffene Umgebung im Zusammenspiel aus realer Umgebung, Hardwarekomponenten und Software ähnlich zur Realität zu reagieren[^18]. Einfache Beispiele hierfür können hochauflösende Displays oder räumliche Geräuschkulissen sein.
{: style="text-align: justify;"}
Wenn ein VR-System von großen Komponenten bis zu kleineren Bestandteilen betracht wird, kann zunächst die reale Umgebung der VR-Anwendung betrachtet werden. Diese reichen von einfachen stationären Umgebungen, wo die Nutzenden einzeln sitzen oder stehen bis zu realen Umgebungen, wo ein gesamter Raum ggfs. mit verschiedenen Nutzenden verwendetbar für die VR Applikation ist[^19]. Die nächst größere Komponente ist die Art und Weise, wie den Nutzenden die virtuelle Realität gezeigt wird. Eine Differenzierung in fünf Kategorien kann der nachfolgenden Abbildung entnommen werden:
{: style="text-align: justify;"}
![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/vr_devices.svg)
*Abbildung 1: Differenzierung von Displayarten zur Visualsierung einer VR-Anwendung[^2].*

Als Hauptdifferenzierung kann die Position des Displays genannt werden. Die Bandbreite reicht von verschiedenen Kombinationen an fest montierten Displays, über Displays, die über den Kopf gehalten werden und zuletzt Displays, die in der Hand gehalten werden. Dabei ist das gängige Verständnis, dass VR mit abschließenden Head-based Displays (HBD) verbunden ist. Neben dem Begriff HBD findet sich in der Literatur häufiger der Begriff Head-mounted Display (HMD).
Je nach System kommen diverse integrierte oder externe Sensoren sowie Aktoren zum Display hinzu, um den Grad der Immersion zu erhöhen. Beispiele für Sensoren umfassen Kameras, Bewegungstracker oder Eingabegeräte (Joysticks, Trackpads, Laufbänder, ...). Als Aktoren können neben dem Display, beispielsweise Audiowiedergabegeräte oder Vibrationsmotoren sein[^18]. Als wichtigste Eigenschaft können geringe Latenz und Genauigkeit genannt werden[^19].
Im Zusammenspiel zwischen Hard- und Software können bei einer schlecht eingestellten und gestalteter VR Anwendung auch potenzielle physische, psychologische Schäden für die Nutzenden auftretten. Bevor auf typische Gefährdungen eingegangen werden kann, sollte darauf hingewiesen werden, dass ebenfalls Cyberbedrohung mit höchst sensitiven Daten möglich sind und hier nicht gesondert auf VR, sondern auf gesundheitsrelevante Aspekte in XR Anwendungen bezogen wird. Einen Überblick über die Gefährdungen kann in Abb. XYZ nachvollzogen werden: 
![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/xr_threat.drawio.svg)
*Abbildung 2: Überblick über Bedrohungen für die menschliche Gesunheit und Leben[^19].*

Von praktischer Relevanz in unserem Anwendung Fall sind die Verhinderung von Motion Sickness und physische Verletzungen durch Kollisionen, da unsere Anwendung weder auf die extensive Nutzung durch Kinder abzielt oder bewusst die Nutzenden negativ manipuliert. 
{: style="text-align: justify;"}
Mit den mögliche Hardwarelösungen, sowie Gefährdungen wurden die Möglichkeiten Präsentation der VR-Welt aufgezeigt, jedoch wurde noch nicht auf die je nach Anwendungsfall und Umfang breiten Möglichkeiten zum Bau der Anwendung eingegangen. Von einfacheren JavaScript Bibliotheken wie WebGL bis zu dedizierten Game Engine kann eine VR Anwendung entwickelt werden. Die Arbeitsschritte bis zur fertigen Anwendung bleiben jedoch vergleichbar: 
{: style="text-align: justify;"}
![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d.drawio.svg)
*Abbildung 3: zeigt den schematisches Workflow für eine VR Anwendung. Zunächst werden Eingabedaten in verschiedenen Formaten in eine 3D-Modellierungssoftware oder Game-Engines importiert. Modelle können manuell oder rechnergestützt generiert und für Visualisierungen genutzt oder in Game-Engines weiterverarbeitet werden. Anwendungen aus Game-Engines können anschließend auf Webplattformen und VR-Headsets bereitgestellt werden[^12]. Die Softwarepakete sind nicht umfassend und stellen einzig bekanntere Beispiele dar.*

Zunächst müssen als Eingabedaten Modelle von realen Objekten erstellt oder bezogen werden. Beispiele für die Erstellung beinhalten die selbstständige Modellierung, der Bezug von existierenden Modellen oder prozedurale Erzeugung. Im Anschluss werden das bzw. die Modelle in eine 3D Modellierungssoftware oder 3D Game Engine übertragen, um aus den einzelnen Modellen eine 3D Anwendung zu erzeugen. Die Grenzen zwischen Modellierungssoftware und 3D Game Engine sind dabei nicht trennscharf. Zum Beispiel ermöglicht Blender neben der Modellierung auch die direkte Animation. Die fertige Applikation wird anschließend dem Zielgerät oder der Präsentationssoftware aufbereitet. 
{: style="text-align: justify;"}

### Entwicklungsumgebung
Dieser theoretische Workflow kann in Bezug auf unsere Vorgaben und Konzeption, wie folgt konkretisiert werden
![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d_con.drawio.svg)
*Abbildung 4: Konkretisierung des theoretischen Workflows für die Entwicklung einer VR Anwendung über die Ohlendorff'sche Villa*

Für unsere Anwendung wurden primär existierende 3D Modelle im Vektorformat verwendet. Der Begriff der Vektordaten ist hier nicht beschränkt auf Vektordaten, wie sie typischerweise in geographischen Informationssystemen vorkommen. Die Daten wurden entweder von der Kursleitung zur Verfügung gestellt, selbstständig modelliert oder vorhandene kostenfreie Modelle aus dem Internet verwendet. Im Anschluss wurden die Daten in [blender](https://www.blender.org/) aufbereitet. Dies umfasste alle Schritte, welche notwendig sind, um keine weiteren Veränderungen in einer Game Engine vorzunehmen. Hierzu zählen insbesondere die Positionierung, Modellierung und Texturierung. Zusätzlich zu Blender wurden [BlenderGIS](https://blender-addons.org/blendergis-addon/) und [Rigacar](https://blender-addons.org/rigacar/) als Erweiterungen verwendet. Die speziellen Nutzungen werden in der Implementierung konkretisiert. Die Entscheidung blender zu verwenden liegt hauptsächlich in der hohen Flexibilität inklusive der einfacheren Progammierung, sowie dem Vorteil, dass das OpenSource Projekt den Studierenden dauerhaft zur Verfügung steht. Hierdurch ist der Lerneffekt auch auf andere Projekte übertragbar.
{: style="text-align: justify;"}
Die aufbereiteten Modelle wurden im Anschluss in [Unreal Engine 5.X](https://www.unrealengine.com/en-US) (UE) importiert. UE wurde verwendet um jegliche Form der Interaktion von der Bewegung in der VR Umgebung bis zum Licht zu erstellen. Über [SteamVR](https://store.steampowered.com/app/250820/SteamVR/?l=german) wurden die Anwendung im Anschluss auf eine HTC Vive (Pro) transferiert und getest. Dieses Setup war im Wesentlichen durch die Aufgabenstellung vorgegeben, sodass die Verwendung einer alterantiven Game Engine oder HMD nicht diskutiert wurde.
{: style="text-align: justify;"}
Das System der HTC Vive setzt sich neben dem HMD aus zwei Motion-Controllern und zwei Tracking Sensoren zusammen. Mittels des Trackings kann das HMD, sowie die Motion-Controller im Raum verortet werden und ermöglichen die freie Bewegung einem Raum von ungefährt  4.5m × 4.5m. Mittels der Controller kann mit der VR Welt in Interaktion getreten werden. Ergänzend dazu sind im HMD ein Näherungssensor, ein Beschleunigungsensor und ein Gyroskop verbaut. Neben dem Display exisitieren Lautsprecher sowie haptische Rückmeldungen durch die Controller[^17].
{: style="text-align: justify;"}

### Implementierung für die Ohlendorff'sche Villa
Im nachfolgenden Abschnitten werden die unterschiedlichen Schritte und Details zur Implementierung der Konzeption genauer erläutert. Dabei wird sich von den Objekten im Außenbereich über die implementierte Animationen in den Innenbereich gearbeitet.
{: style="text-align: justify;"}
#### Außenbereich
Das relevant Gebiet wurde in QGIS eingezeichnet und in blender importiert. Das einfache aber durch BlenderGIS richtig positionierte Polygon wurde daraufhin extrudiert. Damit die Nutzenden nicht aus der Welt fallen können, wurde eine Kollsionsbox um die Scheibe erzeugt. Auf dieser Scheibe wurden drei unterschiedliche amtliche Geodatensätze platziert. Als Hintergrund, der das Gebiet vollständig bedeckt, wurden Daten über den Arten- und Biotopsschutz gewählt[^13]. Aufbauend darauf wurden die Feinkartierung der Straßen mit deren expliziter Nutzung hinzugefügt[^14]. Der Datensatz wurde im Vorfeld leicht modifiziert um auch die Wege innerhalb des Ohlendorff'schen Park darzustellen. Zuletzt wurden die Level of Detail II Daten von Hamburg verarbeit, wobei die Daten zunächst in CityJSON konvertiert wurden und im Anschluss zugeschnitten wurden[^15]. Die Gebäude wurden ebenfalls entsprechend der attributierten Höhe extrudiert. Anschließend wurde die jeweiligen Modellen orientiert am angestrebten Kartenstil mit neutraleren Farben eingefärbt. Das resultierend Modell kann hier gesehen werden: 
{: style="text-align: justify;"}

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
*Modell 1:  der Umgebung nach Integration der amtlichen Geodaten. Die Villa selbst wird nicht gezeigt. Die Basis Scheibe wurde nicht dargestellt, da diese zu Artefakten geführt hat. Bei der Gesamtansicht des Modells sind in Teilen noch Artefakte zu beobachten. Die Artefakte konnten in der finalen VR Applikation nicht beobachtet werden.*

Ebenfalls wurden Versuche unternommen ein digitales Höhenmodell zu integrieren, da die Villa in den Hang hinein gebaut wurde. Jedoch ist die Auflösung der amtlichen Daten für eine VR Anwendung zu gering und die eher geringen Höhenunterschiede sind ohne Überhöhung nicht erkennbar. Gleichzeitig führte eine Integration zu massiven Performance verlusten.
Um die Immersion der Nutzenden zu erhöhen, wurden weitere Elemente der realen Umwelt der Applikation hinzugefügt. Hierzu zählen Modelle von Bäumen, Gebüsch, Steine, Autos und Laternen. Die Modelle konnten alle frei verfügbar im Internet gefunden werden und wurden in blender einzig eingefärbt und/oder durch Streckung, Drehungen oder Expansion leicht modifiziert, um visuelle Variation zwischen bspw. Baumtypen herzustellen. Alle zusätzlichen Elemente wurden nicht in einer realistischen Anzahl dargestellt. Diese Entscheidung resultiert von Experimenten, die zeigten, dass zu viele Element die Nutzenden visuell überfordern und somit keinen Mehrwert gebracht haben. Das resultierende Modell sieht, wie folgt aus: 
{: style="text-align: justify;"}

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
*Modell 2: Vollständiger Außenbereich der VR Applikation zur Ohlendorff'schen Villa in Hamburg Volksdorf. Erneut wurde die Villa ausgelassen.*

Abseits der unterschiedlichen Modellen wurden weitere Elemente hinzugefügt, die die Immersion verstärken sollen. Hierzu zählen die Erzeugung einer Geräuschkullisse, Bewegung der Autos und einen Tag-Nacht Rythmus samt verbundener Lichter. 
Visuell am auffällgsten ist der Tag-Nacht Rhytmus. Hierzu wurde der Blueprint des Sun Position Calculators so verändert, dass ein realitätnaher Sonnen und Mondverlauf je nach Position auf der Erde ermöglicht wird. Neben der Definition einer Position auf der Erde lassen sich auch Parameter über die Intensität und Größe, sowie Material der Sterne kontrollieren. *Was genau wurde verändert; Wie genau funktioniert das; PostProcessing Box*. Im Kontext dieser Implementierung wird auch ermöglicht unterschiedliche Lichter je nach Tageszeit an und auszuschalten. Diese Funktionalität benötigt durch die Berechnung der Schatten viele Resourcen und wurde einzig in einem Innenraum, sowie der Straßenbeleuchtung verwendet. Ähnlich dazu wurde ein Material erzeugt, welches auch auf die Tageszeit reagiert und bei den Fahrzeugen dazu führt, dass die Leuchter die Farbe in der Tag und Nacht wechseln. Zwei resultierende Beispiele können hier gezeigt werden:
{: style="text-align: justify;"}

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Island_Day_Night_Opt.gif)
*Abbildung 5: Überblick eines Tag-Nacht Rhytmuses über die ganze Insel. Neben der Veränderung des Lichtes lässt sich bereits die Bewegung der Fahrzeuge erkennen.*

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Haus_Day_Night_Opt.gif)
*Abbildung 6: Detailaufnahme des Tag-Nacht Rhytmuses inklusive der sichtbaren Veränderung der Innenbeleuchtung*

Um die hier sichtbaren Fahrzeuge zu bewegen, wurden diese in blender mittels Rigacar vorbereitet, sodass aus einem statischen Netz ein Skelettnetz erzeugt wurde. Hierdurch wurden die Größe vereinheitlicht, die einzelnen Räder bewegbar gemacht und der Drehpunkt für den späteren Blueprint aufbereiten. In Theorie ist es mit einem solchen Fahrzeug möglich, dass ein Actor einsteigen und fahren kann. Dem jeiligen Fahrzeug wurde ein Blueprint hinzugefügt, der die Fahrzeuge auf einem Spline bewegen lässt und diesen vorher selbstständig auffindet. Insgesamt wurde je ein Spline für jede Fahrrichtung implementiert. Außerhalb der Scheibe sind Markierungen gesetzt, welche die jeweiligen Fahrzeuge erkennen, auf eine Liste schreiben und sichtbar oder unsichtbar machen je nachdem, ob diese bereits auf der Liste existieren.*Detailierte Implementierung*. Das Ergebnis stellt sich, wie folgt dar: 
{: style="text-align: justify;"}
![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Car_Move_Opt.gif)
*Abbildung 7: In der Animation sind drei fahrende Fahrzeuge sichtbar. Der Sportwagen wurde für die Animation an einer ungewöhnlichen Stelle positioniert und findet den Spline.*

Zuletzt wurden unterschiedliche Sounds der Umgebung hinzugefügt. Dabei unterscheidet sich die Komplexität der Sounderstellung. Für die sich bewegenden Fahrzeuge wurde relativ einfach ein Motorensound hinzugefügt und überall in der Welt wurden Vögelgeräusche hinterlegt. Die Vogelgeräusche wurden so implementiert, dass jeweils zufällig zwei von acht möglich Sounds kombiniert gespielt werden. Deutlich komplexer sind die adaptiven Windgeräusche. Das Grundkonzept ist, dass sich Windgeräusche je nach Umgebung des VR Pawns in der Lautstärke verändern, sodass auf einer freien Fläche der volle Sound erklingt und in engen Umgebungen deutlich weniger Windgeräusche. Um diesen Effekt zu ermöglichen, wurde eine Actor Component dem VR Pawn hinzugefügt. Innerhalb dieser Komponente wird zunächst ein aus zwei verschiedenen starken Windgeräuschen zusammengesetzter Sound erzeugt. Ausgehend davon wird ein Timer gestartet, der je nach Zeiteinheit eine Anpassung der Windlautstärke vornimmt. Die Anpassungstärke wird dabei durch die Verändeurng von emittierten Linien der Komponent ermittelt. Hierzu werden bspw. sechs Linien im den Pawn ausgestrahlt, sobald diese Linie ein Objekt trifft, verändert sich der Wert der Linie. Entsprechend muss die Intensität der Windgeräusche verringert werden, sobald mehrere Linien geringere Werte anzeigen. Nach Ermittlung dieses Wertes findet zunächst eine Interpolation statt, um abrupte Veränderungen zu vermeiden. Dieser interpolierte Wert wird im Anschluss verwendet, um die Lautstärke zu verändenr.
{: style="text-align: justify;"}

*Animation Wind*

#### Innenbereich
Der Innenbereich unserer VR-Anwendung wird durch eine bewegliche Tür betreteten, worauf der Nutzende im Empfangsraum landet. Der Empfangsraum beinhaltet keine weitere Interaktion oder Animation. Im vom Nutzeden rechten Raum wurde ein Kunstraum inklusive Interaktion implementiert. Gezeigt werden verschiedene gestohlene Gemälde samt Informationstafeln. Das wertvollste gestohlene Gemälde ist jedoch nicht direkt ausgestellt und muss über eine Zahlenkombination aus einer Truhe "geholt" werden. Hierzu können die Nutzenden die drei notwendigen Zahlen aus den anderen Bild durch eine Lupe suchen. Im Anschluss kann die Truhe geöffnet werden. Details zur Implementierung können bei Madelaine nachvollzogen werden.
{: style="text-align: justify;"}







# Fazit & Ausblick


# Notes

## Animation & Interaktionen

* Teleportation
* Geräusche im Gebäude
### Positiv
* Sehr hohe Frames
* generell performance statsitikken anführne

### Einschränkungen
* Wind
* Nebel
* Wie landing page & und about?
* MUSIK fehlt noch
* Bedeutung Geoinformatics / Visualisierung räumlicher daten: [1.3 3D Modeling and VR in the Geospatial Sciences | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/800)
Geoinformatik und Geodäsie sind dabei eng mit VR und 3D Modellierung verbunden. 
3D Stadtmodelle haben in den letzten Jahren an Bedeutung für diverse Anwendungen gewonnen in den GIScience [^7]
* Beudeutung für städte: Biljecki, F., Stoter, J., Ledoux, H., Zlatanova, S., & Çöltekin, A. (2015). Applications of 3D City Models: State of the Art Review. ISPRS International Journal of Geo-Information, 4(4), 2842–2889. doi:10.3390/ijgi4042842
* Genauer CAD Modelle


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

# Literatur
[^1]: Jeong Kim, Xiangyu Wang, Peter Love, Heng Li & Shih-Chung Kang (2013). Virtual reality for the built environment: a critical review of recent advances, ITcon Vol. 18, pg. 279-305, https://www.itcon.org/2013/14
[^2]: Yuxuan Zhang, Hexu Liu, Shih-Chung Kang & Mohamed Al-Hussein (2020). Virtual reality applications for the built environment: Research trends and opportunities. Automation in Construction. 118. 10.1016/j.autcon.2020.103311
[^3]: Paul Milgram, Haruo Takemura, Akira Utsumi & Fumio Kishino(1994). Augmented Reality: A class of displays on the reality-virtuality continuum. Proceedings of SPIE - The International Society for Optical Engineering Vol. 2351
[^4]: Artur Becker & Carla M. Dal Sasso Freitas (2023). Evaluation of XR Applications: A Tertiary Review. ACM Comput. Surv. Vol. 56, 5, 110 pg.1-35  https://doi.org/10.1145/3626517
[^5]: Isabell Wohlgenannt, Alexander Simons & Stefan Stieglitz (2020). Virtual Reality. Bus Inf Syst Eng. Vol. 62, pg. 455–461. https://doi.org/10.1007/s12599-020-00658-9
[^6]: Übersetzt aus: Åsa Fast-Berglund, Liang Gong & Dan Li (2018): Testing and validating extended reality (xR) technologies in manufacturing. Procedia Manuf. Vol. 25, pg. 31-38. https://doi.org/10.1016/j.promfg.2018.06.054
[^7]: Filip Biljecki, Jantien Stoter, Hugo Ledoux, Sisi Zlatanova & Arzu Çöltekin (2015). Applications of 3D City Models: State of the Art Review. ISPRS Int. J. Geo-Inf. Vol. 4, 4, pg. 2842-2889. https://doi.org/10.3390/ijgi404284
[^8]: Gerhard Hirschfeld (2009). Historie - Die Ohlendorff'sche Villa. https://ohlendorffsche.de/historie/ [Zugriff: 19.03.2025]
[^10]: o.A. (o.J). Umbau und Sanierung - Die Ohlendorff'sche Villa. https://ohlendorffsche.de/umbau-und-sanierung/ [Zugriff: 19.03.2025]
[^11]: Thitiwudh Uasmith, Tantikorn Pukkaman & Peeraya Sripian (2017). Low-poly image stylization. Journal for Geometry and Graphics, Vol. 21, 1, pg. 131-139. https://shibaura.elsevierpure.com/en/publications/low-poly-image-stylization
[^12]: Verändert und erweitert: Alex Klippel, Mahda M. Bagher & Jan Oliver Wallgrün (o.J). 3D and VR Application Building Workflows. https://www.e-education.psu.edu/geogvr/node/559 [Zugriff: 19.03.2025]
[^13]: Freie und Hansestadt Hamburg, Behörde für Umwelt und Energie (2024). Daten: Arten- und Biotopschutz - AuBS (ehem. APRO). https://registry.gdi-de.org/id/de.hh/B8F6865A-1790-4B9D-987E-AF97B88E84D3 [Zugriff: 12.12.2024]
[^14]: Freie und Hansestadt Hamburg, Behörde für Verkehr und Mobilitätswende (2023): Daten: Feinkartierung Straße Hamburg. https://registry.gdi-de.org/id/de.hh/ad7e3cb6-9a9e-4044-81b1-4c1f8d974c2f [Zugriff: 08.12.2024]
[^15]: Freie und Hansestadt Hamburg, Landesbetrieb Geoinformation und Vermessung (LGV) (2024): Daten: 3D-Gebäudemodell LoD2-DE Hamburg.   
https://registry.gdi-de.org/id/de.hh/948321ba-e9b2-4290-88c3-8dda2912defa [Zugriff: 01.12.2024]
[^18]: Christoph Anthes, Rubén Jesús García-Hernández, Markus Wiedemann & Dieter Kranzlmüller (2016). State of the art of virtual reality technology. IEEE Aerospace Conference, Big Sky, MT, USA. pg. 1-19. 10.1109/AERO.2016.7500674.
[^19]: Sara Qamar, Zahid Anwar & Mehreen Afzal (2023). A systematic threat analysis and defense strategies for the metaverse and extended reality systems. Computers & Security
Vol. 128, 103127.
[^20]: Asmaa Saeed Alqahtani, Lamya Foaud Daghestani & Lamiaa Fattouh Ibrahim (2017). Environments and system types of virtual reality technology in STEM: a survey. International Journal of Advanced Computer Science and Applications Vol. 8, 6. 10.14569/IJACSA.2017.080610 . 
[^17]: HTC Corporation (o.J.). VIVE Product Specification. https://www.vive.com/eu/product/vive/ [Zugriff: 19.03.2025]