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
Bevor jedoch tiefer in das Thema, sowie das studentische Projekt eingegangen wird, sollte das Verständnis des Begriffes VR offengelegt werden. Eingeordnet werden kann der Begriff in das übergeordnete Thema des Realitäts-Virtualitäts-Kontinuums[^3]. Dabei wird davon ausgegangen, dass sich Augmented Reality (AR), Augmented Virtuality (AV) und VR zwischen den Endpolen physischen Realität und vollständig virtuellen Umgebung befinden[^5]. AR, AV und VR werden dabei unter dem Begriff *extended reality* (XR) zusammengefasst, welches „[...] alle realen und virtuellen kombinierten Umgebungen und Mensch-Maschine-Interaktionen, die durch Computertechnologie und Wearables erzeugt werden“ umfasst[^6]. Vor diesem Hintergrund wurden verschiedene Definition von VR im wissenschaftlichen Kontext erarbeitet, welche nicht im Detail erläutert werden sollen und einzig auf das hier zugrundlegendes Verständnis dargelegt werden soll:
{: style="text-align: justify;"}
> VR leverages immersive technologies to simulate interactive virtual environments or virtual worlds with which users become subjectively involved and in which they feel physically present[^5]
{: #def}
Basierend auf diesem Verständnis wird im folgenden Bericht zunächst das reale Objekt beschrieben, sowie die Entscheidung des Modelles begründet. Im Anschluss folgt die Konzeption unserer VR Anwendung, weitere theoretische Überlegungen zur Anwendung und die verwendete Hard- und Software. Nachdem die Vorraussetzungen festgelegt wurden, wird die Umsetzung, sowie die Limitierungen samt Fazit/Ausblick aufgezeigt. Innerhalb dieses Berichtes wird insbesondere die Entstehung des Außenbereiches, samt aller dazugehörigen Elemente aufgegriffen. Für andere Bereiche, wie beispielsweise die Texturierung des Gebäudes, werden erwähnt, aber detailierter in den anderen Berichten aufgegriffen.
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
Blablba
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
### Theorie
Wie bereits aus der [Definition](#def) hervorgeht, zielt eine VR Anwendung auf die Immersion der Nutzenden in eine virtuelle Welt ab, welche gleichzeitig die Außenwelt versucht auszuschließen[^20]. Um einen hohen Immersionsgrad zu erzeugen, sollte die geschaffene Umgebung im Zusammenspiel aus realer Umgebung, Hardwarekomponenten und Software ähnlich zur Realität zu reagieren[^18]. Einfache Beispiele hierfür können hochauflösende Displays oder räumliche Geräuschkulissen sein. 
Wenn ein VR-System von großen Komponenten bis zu kleineren Bestandteilen betracht wird, kann zunächst die reale Umgebung der VR-Anwendung betrachtet werden. Diese reichen von einfachen stationären Umgebungen, wo die Nutzenden einzeln sitzen oder stehen bis zu realen Umgebungen, wo ein gesamter Raum ggfs. mit verschiedenen Nutzenden verwendetbar für die VR Applikation ist[^19]. Die (vermutlich) nächst größere Komponente ist die Art und Weise, wie den Nutzenden die virtuelle Realität gezeigt wird. Eine Differenzierung in fünf Kategorien kann der nachfolgenden Abbildung entnommen werden:
![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/vr_devices.svg)
*Abbildung XY: Differenzierung von Displayarten zur Visualsierung einer VR-Anwendung[^2].*
Als Hauptdifferenzierung kann die Position des Displays genannt werden. Die Bandbreite reicht von verschiedenen Kombinationen an fest montierten Displays, über Displays, die über den Kopf gehalten werden und zuletzt Displays, die in der Hand gehalten werden. Dabei ist das gängige Verständnis, dass VR mit abschließenden Head-based Displays (HBD)verbunden ist. Neben dem Begriff HBD findet sich in der Literatur häufiger der Begriff Head-mounted Display.
Je nach System kommen diverse integrierte oder externe Sensoren sowie Aktoren zum Display hinzu, um den Grad der Immersion zu erhöhen. Beispiele für Sensoren umfassen Kameras, Bewegungstracker oder Eingabegeräte (Joysticks, Trackpads, Laufbänder, ...). Als Aktoren können neben dem Display Audiowiedergabegeräte oder Vibrationsmotoren sein[^18]. Als wichtigste Eigenschaft können geringe Latenz und Genauigkeit genannt werden[^19].
Im Zusammenspiel zwischen Hard- und Software können bei einer schlecht eingestellten und gestalteter VR Anwendung auch potenzielle physische, psychologische Schäden für die Nutzenden auftretten. Bevor auf typische Gefährdungen eingegangen werden kann, sollte darauf hingewiesen werden, dass ebenfalls Cyberbedrohung mit höchst sensitiven Daten möglich sind und hier nicht gesondert auf VR sondern auf gesundheitsrelevante Aspekte in XR Anwendungen bezogen wird. Einen Überblick über die Gefährdungen kann in Abb. XYZ gesehen werden: 
![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/xr_threat.drawio.svg)
*Abbildung XY: Überblick über Bedrohungen für die menschliche Gesunheit und Leben[^19].*



Ich bau von der Definition her hier auf und gehee dann auf aspekete ein
* Immersion
* Was muss eine VR Anwendung aufweisen etc. sollt ehier behandelt werden damit man dann den bezug aufbauen kann
* hier könnten auch die verschiedenen displays gut auftauchen
* Nach VL wären wichtige Themen:
  * Wiedergabetreue, Immersion, navigation und Interaktion &rarr; sollten hier als bewertungskriterien auftauchen
  * Was genau ist eine Game Enigne &rarr; kurz irgendwo definieren undw as kann diese
  * Was kann eignetlich die Brille ... 
  * Workflow in VL ein wenig anders: 3D-Datenerfassung &rarr; 3D-Modellierung &rarr; Texture Mapping &rarr; Implementierung in Game Eninge &rarr; Stema VR als Schnitsttelle &rarr; Visualisierung im VR System
  * Wie viele Frames braucht man performance mäßig
  * Luteraturverzeichnis anschauen ...
* VL2:
  * Thema mit Geoedaten hat er auch
### Entwicklungsumgebung
Die Möglichkeiten eine VR Anwendung zu bauen, sind je intendierten Anwendungsfall und Umfang breit. Von einfacheren JavaScript Bibliotheken wie WebGL bis zu dedizierten Game Engine kann eine VR Anwendung entwickelt werden. Die Arbeitsschritte bis zur fertigen Anwendung bleiben jedoch vergleichbar: 

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d.drawio.svg)
*Abbildung Z zeigt den schematisches Workflow für eine VR Anwendung. Zunächst werden Eingabedaten in verschiedenen Formaten in eine 3D-Modellierungssoftware oder Game-Engines importiert. Modelle können manuell oder rechnergestützt generiert und für Visualisierungen genutzt oder in Game-Engines weiterverarbeitet werden. Anwendungen aus Game-Engines können anschließend auf Webplattformen und VR-Headsets bereitgestellt werden[^12]. Die Softwarepakete sind nicht umfassend und stellen einzig bekanntere Beispiele dar.*

Zunächst müssen als Eingabedaten Modelle von realen Objekten erstellt oder bezogen werden. Beispiele für die Erstellung beinhalten die selbstständige Modellierung, der Bezug von existierenden Modellen oder prozedurale Erzeugung. Im Anschluss werden das bzw. die Modelle in eine 3D Modellierungssoftware oder 3D Game Engine übertragen, um aus den einzelnen Modellen eine 3D Anwendung zu erzeugen. Die Grenzen zwischen Modellierungssoftwayre und 3D Game Engine sind dabei nicht trennscharf. Zum Beispiel ermöglicht Blender neben der Modellierung auch die direkte Animation. Die fertige Applikation wird anschließend dem Zielgerät oder der Präsentationssoftware aufbereitet. 
{: style="text-align: justify;"}
Der theoretische Aufbau kann auf unsere Gegebenheiten vor dem Hintergrund der Projektvorgeben, sowie der Konzeption konkretisiert werden:

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/workflow_3d_con.drawio.svg)
*Abbildung X: Konkretisierung des theoretischen Workflows für die Entwicklung einer VR Anwendung über die Ohlendorff'sche Villa*

Für unsere Anwendung wurden primär existierende 3D Modelle im Vektorformat verwendet. Der Begriff der Vektordaten ist hier nicht beschränkt auf Vektordaten, wie sie typischerweise in Geographischen Informationssystemen vorkommen. Die Daten wurden entweder von der Kursleitung zur Verfügung gestellt, selbstständig modelliert oder vorhandene kostenfreie Modelle aus dem Internet verwendet. Im Anschluss wurden die Daten in [blender](https://www.blender.org/) aufbereitet. Dies umfasste alle Schritte, welche notwendig sind, um keine weiteren Veränderungen in einer Game Engine vorzunehmen. Hierzu zählen insbesondere die Positionierung, Modellierung und Texturierung. Zusätzlich zu Blender wurden [BlenderGIS](https://blender-addons.org/blendergis-addon/) und [Rigacar](https://blender-addons.org/rigacar/) als Erweiterungen verwendet. Die speziellen Nutzungen werden in der Implementierung konkretisiert. Die Entscheidung blender zu verwenden liegt hauptsächlich in der hohen Flexibilität inklusive der einfacheren Progammierung, sowie dem Vorteil, dass das OpenSource Projekt den Studierenden dauerhaft zur Verfügung steht. Hierdurch ist der Lerneffekt auch auf andere Projekte übertragbar.
{: style="text-align: justify;"}
Die aufbereiteten Modelle wurden im Anschluss in [Unreal Engine 5.4](https://www.unrealengine.com/en-US) (UE) importiert. UE wurde verwendet um jegliche Form der Interaktion von der Bewegung in der VR Umgebung bis zum Licht zu erstellen. Über [SteamVR](https://store.steampowered.com/app/250820/SteamVR/?l=german) wurden die Anwendung im Anschluss auf eine HTC Vive Pro transferiert. Dieses Setup war im Wesentlichen durch die Aufgabenstellung vorgegeben, sodass die Verwendung einer alterantiven Game Engine oder Head-Mounted Display (HMD) nicht diskutiert wurde.
{: style="text-align: justify;"}


**ABSATZ VIVE** &rarr; was ist dadurch quasi schon vorgegeben

### Implementierung für die Ohlendorff'sche Villa
Im nachfolgenden Abschnitten werden die unterschiedlichen Schritte und Details zur Implementierung der Konzeption genauer erläutert. Dabei wird sich von den Objekten im Außenbereich über die implementierte Animationen in den Innenbereich gearbeitet.
#### Außenbereich
*Kollsion muss irgendwo noch erwähnt werden*


Das relevant Gebiet wurde in QGIS eingezeichnet und in blender importiert. Das einfache aber durch BlenderGIS richtig positionierte Polygon wurde daraufhin extrudiert. Auf dieser Scheibe wurden drei unterschiedliche amtliche Geodatensätze platziert. Als Hintergrund, der das Gebiet vollständig bedeckt, wurden Daten über den Arten- und Biotopsschutz gewählt[^13]. Aufbauend darauf wurden die Feinkartierung der Straßen mit deren expliziter Nutzung hinzugefügt[^14]. Der Datensatz wurde im Vorfeld leicht modifiziert um auch die Wege innerhalb des Ohlendorff'schen Park darzustellen. Zuletzt wurden die LOD II Daten von Hamburg verarbeit, wobei die Daten zunächst in CityJSON konvertiert wurden und im Anschluss zugeschnitten wurden[^15]. Die Gebäude wurden ebenfalls entsprechend der attributierten Höhe extrudiert. Anschließend wurde die jeweiligen Modellen orientiert am angestrebten Kartenstil mit neutraleren Farben eingefärbt. Das resultierend Modell kann hier gesehen werden: 

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
*Modell der Umgebung nach Integration der amtlichen Geodaten. Die Villa selbst wird nicht gezeigt. Die Basis Scheibe wurde nicht dargestellt, da diese zu Artefakten geführt hat. Bei der Gesamtansicht des Modells sind in Teilen noch Artefakte zu beobachten. Die Artefakte konnten in der finalen VR Applikation nicht beobachtet werden.*

Ebenfalls wurden Versuche unternommen ein digitales Höhenmodell zu integrieren, da die Villa in den Hang hinein gebaut wurde. Jedoch ist die Auflösung der amtlichen Daten für eine VR Anwendung zu gering und die eher geringen Höhenunterschiede sind ohne Überhöhung nicht erkennbar. Gleichzeitig führte eine Integration zu massiven Performance verlusten
Um die Immersion der Nutzenden zu erhöhen, wurden weitere Elemente der realen Umwelt der Applikation hinzugefügt. Hierzu zählen Modelle von Bäumen, Gebüsch, Steine, Autos und Laternen. Die Modelle konnten alle frei verfügbar im Internet gefunden werden und wurden in blender einzig eingefärbt und oder durch Streckung, Drehungen oder Expansion leicht modifiziert, um visuelle Variation zwischen bspw. Baumtypen herzustellen. Alle zusätzlichen Elemente wurden nicht in einer realistischen Anzahl dargestellt. Diese Entscheidung resultiert von Experimenten, die zeigten, dass zu viele Element die Nutzenden visuell verwirren **?** und keinen Mehrwert gebracht haben. Das resultierende Modell sieht, wie folgt aus: 

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
*Vollständiger Außenbereich der VR Applikation zur Ohlendorff'schen Villa in Hamburg Volksdorf. Erneut wurde die Villa ausgelassen.*

Neben den unterschiedlichen Modellen wurden weitere Elemente hinzugefügt, die die Immersion verstärken sollen. Hierzu zählen die Erzeugung einer Geräuschkullisse, Bewegung der Autos und einen Tag-Nacht Rythmus samt verbundener Lichter. 
Visuell am auuffällgsten ist der Tag-Nacht Rhytmus. Hierzu wurde der Blueprint des Sun Position Calculators so verändert, dass ein realitätnaher Sonnen und Mondverlauf je nach Position auf der Erde ermöglicht wird. Neben der Definition einer Position auf der Erde lassen sich auch Parameter über die Intensität und Größe, sowie Material der Sterne kontrollieren. *Was genau wurde verändert; Wie genau funktioniert das; PostProcessing Box*. Im Kontext dieser Implementierung wird auch ermöglicht unterschiedliche Lichter je nach Tageszeit an und auszuschalten. Diese Funktionalität benötigt durch die Berechnung der Schatten viele Resourcen und wurde einzig in einem Innenraum, sowie der Straßenbeleuchtung verwendet. Ähnlich dazu wurde ein Material erzeugt, welches auch auf die Tageszeit reagiert und bei den Fahrzeugen dazu führt, dass die Leuchter die Farbe in der Tag und Nacht wechseln.   Zwei resultierende Beispiele können hier gezeigt werden:

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Island_Day_Night_Opt.gif)
*Abbildung X: Überblick eines Tag-Nacht Rhytmuses über die ganze Insel. Neben der Veränderung des Lichtes lässt sich bereits die Bewegung der Fahrzeuge erkennen.*

![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Haus_Day_Night_Opt.gif)
*Abbildung X: Detailaufnahme des Tag-Nacht Rhytmuses inklusive der sichtbaren Veränderung der Innenbeleuchtung*

Um die hier sichtbaren Fahrzeuge zu bewegen, wurden diese in blender mittels Rigacar vorbereitet, sodass diese de facto kein statische Netz sind, sondern ein Skelettnetz sind. Hierdurch wurde die Größe vereinheitlicht, die einzelnen Räder bewegbar gemacht und der Drehpunkt für den späteren Blueprint aufbereiten. In Theorie ist es mit einem solchen Fahrzeug möglich, dass ein Actor einsteigen kann. Dem jeiligen Fahrzeug wurde ein Blueprint hinzugefügt, der die Fahrzeuge auf einem Spline bewegen lässt und diesen vorher selbstständig auffindet. Insgesamt wurde je ein Spline für jede Fahrrichtung implementiert. Außerhalb der Scheibe sind Markierungen gesetzt, welche die jeweiligen Fahrzeuge erkennen, auf eine Liste schreiben und sichtbar oder unsichtbar machen je nachdem, ob diese bereits auf der Liste existieren.*Detailierte Implementierung*. Das Ergebnis stellt sich, wie folgt dar: 
![alt]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/Car_Move_Opt.gif)
*Abbildung X: In der Animation sind drei fahrende Fahrzeuge sichtbar. Der Sportwagen wurde für die Animation an einer ungewöhnlichen Stelle positioniert und findet den Spline.*
Zuletzt wurden unterschiedliche Sounds der Umgebung hinzugefügt. Dabei unterscheidet sich die Komplexität der Sounderstellung. Für die sich bewegenden Fahrzeuge wurde relativ einfach ein Motorensound hinzugefügt und überall in der Welt wurden Vögelgeräusche hinterlegt. Die Vogelgeräusche wurden so implementiert, dass jeweils zufällig zwei von acht möglich Sounds gespielt werden. Deutlich komplexer sind die adaptiven Windgeräusche. Das Grundkonzept ist, dass sich Windgeräusche je nach Umgebung des VR Pawns in der Lautstärke verändern, sodass auf einer freien Fläche der volle Sound erklingt und in engen Umgebungen deutlich weniger Windgeräusche. Um diesen Effekt zu ermöglichen, wurde eine Actor Component dem VR Pawn hinzugefügt. Innerhalb dieser Komponente wird zunächst ein aus zwei verschiedenen starken Windgeräuschen zusammengesetzter Sound erzeugt. Ausgehend davon wird ein Timer gestartet, der je nach Zeiteinheit eine Anpassung der Windlautstärke vornimmt. Die Anpassungstärke wird dabei durch die Verändeurng von emittierten Linien der Komponent ermittelt. Hierzu werden bspw. sechs Linien im den Pawn ausgestrahlt, sobald diese Linie ein Objekt trifft, verändert sich der Wert der Linie. Entsprechend muss die Intensität der Windgeräusche verringert werden, sobald mehrere Linien geringere Werte anzeigen. Nach Ermittlung dieses Wertes findet zunächst eine Interpolation statt, um abrupte Veränderungen zu vermeiden. Dieser interpolierte Wert wird im Anschluss verwendet, um die Lautstärke zu verändenr.

*Animation Wind*



* Innenbereich
  * 

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

### Positiv
* Sehr hohe Frames

### Einschränkungen
* Wind
* Nebel


### Hardware
* Theoretische viele möglichkeiten bei uns an der uni
* [HTC Vive Pro| GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/861)
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
  * Target Platform &rarr; Vive Pro/ VR BRILLE
  * Präsentationsplatform &rarr; Steam
  * [2.6 3D and VR Application Building Workflows | GEOG 497: 3D Modeling and Virtual Reality](https://www.e-education.psu.edu/geogvr/node/559)

# Literature
* Virtual reality applications for the built environment: Research trends and opportunities 
  * first vr for built environment in the 1990s
  * technische möglichkeiten haben die relevanz und praktikalibilität gesteigert
  *  In the context of this research, virtual reality refers to the uses of computer science and behavioral interfaces to simulate the behavior of 3D objects in a virtual world, enabling real-time interactions with each other in pseudo-natural immersion via sensorimotor channels 
  * Different devices could deliver such an experience &rarr; ![alt text]({{ site.url }}{{ site.baseurl }}/assets/images/JPH/vr_devices.svg)


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










[^1]: Kim MJ, Wang X, Love PED, Li H, Kang SC (2013). Virtual reality for the built environment: a critical review of recent advances, ITcon Vol. 18, pg. 279-305, https://www.itcon.org/2013/14
[^2]: https://www.sciencedirect.com/science/article/abs/pii/S0926580520301394
[^3]: Milgram, Paul; H. Takemura; A. Utsumi; F. Kishino (1994). "Augmented Reality: A class of displays on the reality-virtuality continuum". Proceedings of SPIE - The International Society for Optical Engineering Vol. 2351
[^4]: Artur Becker and Carla M. Dal Sasso Freitas. 2023. Evaluation of XR Applications: A Tertiary Review. ACM Comput. Surv. 56, 5, Article 110 (May 2024), 35 pages. https://doi.org/10.1145/3626517
[^5]: Wohlgenannt, I., Simons, A. & Stieglitz, S. Virtual Reality. Bus Inf Syst Eng 62, 455–461 (2020). https://doi.org/10.1007/s12599-020-00658-9
[^6]: Übersetzt aus: Fast-Berglund Å, Gong L, Li D (2018) Testing and validating extended reality (xR) technologies in manufacturing. Procedia Manuf 25:31–38
[^7]: Biljecki, F.; Stoter, J.; Ledoux, H.; Zlatanova, S.; Çöltekin, A. Applications of 3D City Models: State of the Art Review. ISPRS Int. J. Geo-Inf. 2015, 4, 2842-2889. https://doi.org/10.3390/ijgi404284
[^8]: https://ohlendorffsche.de/historie/
[^10]: https://ohlendorffsche.de/umbau-und-sanierung/
[^11]: https://shibaura.elsevierpure.com/en/publications/low-poly-image-stylization
[^12]: Verändert und Ereitert: https://www.e-education.psu.edu/geogvr/node/559
[^13]: https://metaver.de/trefferanzeige?cmd=doShowDocument&docuuid=B8F6865A-1790-4B9D-987E-AF97B88E84D3
[^14]: https://metaver.de/trefferanzeige?cmd=doShowDocument&docuuid=A02FCB1D-8B20-4937-BC9A-235D736B8569
[^15]: https://metaver.de/trefferanzeige?docuuid=2C1F2EEC-CF9F-4D8B-ACAC-79D8C1334D5E
[^18]: https://ieeexplore.ieee.org/abstract/document/7500674
[^19]: https://www.sciencedirect.com/science/article/pii/S0167404823000378
[^20]: Alraizzah, A., Lamya, F., Fattouh, L., 2017. Environments and system types of virtual reality technology in STEM: a survey. International Journal of Advanced Com- puter Science and Applications 8. doi: 10.14569/IJACSA.2017.080610 . 