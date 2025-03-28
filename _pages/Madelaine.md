---
title: "Bericht von Madelaine"
permalink: /Madelaine/
toc: true
toc_label: "Inhaltsverzeichnis"
author_profile: true

author:
  name     : "Madelaine Linek"
  avatar   : "/assets/images/jph.png"
  bio      : "My awesome biography constrained to a sentence or two goes here."
  location : "Hamburg, USA"
  links:
    - label: "Mastodon"
      icon: "fa-brands fa-mastodon"
      url: "https://mastodon.social/@jphecht"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/jp-hecht"


excerpt: "This post should display a **header with a solid background color**, if the theme supports it."
header:
  overlay_color: "#333"

---

Einleitung
Virtuelle Realität (VR) ist eine Technologie, die es den Nutzern ermöglicht, in computergenerierte Umgebungen einzutauchen und mit ihnen zu interagieren, und zwar auf eine Weise, die eine realistische räumliche Erfahrung simuliert. Obwohl VR ursprünglich hauptsächlich mit dem Bereich der Unterhaltung in Verbindung gebracht wurde, wird sie zunehmend in den Bereichen Bildung, Museen und Kulturerbe eingesetzt. Sie ermöglicht insbesondere die Rekonstruktion historischer Räume und die immersive Präsentation von architektonischen Objekten und schafft damit neue Möglichkeiten der Wissensvermittlung und historischen Interpretation.
Im Kurs „3D-Visualisierung“ vertiefen die Studierenden ihre Fähigkeiten in der 3D-Modellierung und Geodatenvisualisierung. Hauptziel ist der Entwurf eines interaktiven, begehbaren Gebäudes, das in eine speziell entwickelte und modellierte Umgebung eingebettet ist. Konkrete Aufgabe der Anwendung dieser Konzepte ist die digitale Rekonstruktion der Villa Ohlendorff, eines historischen Gebäudes aus dem 19. Jahrhundert in Hamburg (Quelle). Ziel war es, den Originalzustand und den historischen Kontext virtuell nachzustellen. Die VR-Technologie spielt dabei eine wichtige Rolle, denn ein hoher Immersionsgrad ermöglicht es den Teilnehmern, die virtuelle Umgebung objektiv und messbar zu erleben. Immersion kann als eine messbare Eigenschaft eines Systems beschrieben werden, die angibt, inwieweit es die Teilnehmer in eine virtuelle Welt einbindet (Slater et al. 1998). Darüber hinaus erzeugt VR auch ein Gefühl der Präsenz, das als ein mentaler Zustand beschrieben wird, in dem sich die Teilnehmer tatsächlich in der virtuellen Umgebung befinden (ebd.). Diese Wahrnehmung der Präsenz in der virtuellen Welt kann tiefere und authentischere emotionale Reaktionen hervorrufen.
Ziel dieser theoretischen Arbeit ist es, das Potenzial der virtuellen Realität als Medium für die Vermittlung von Geschichten zu untersuchen. Sie konzentriert sich auf die Frage, wie die Interaktionen zwischen Nutzern und virtuellem Raum im Rahmen des Projekts konzipiert wurden. Besonderes Augenmerk wurde auf die technische Umsetzung dieser Interaktionen mit Hilfe des Blueprints-Systems in der Entwicklungsumgebung Unreal Engine gelegt. Ausgehend von einer kurzen Einführung in den Forschungsgegenstand, in der das Modell (Kapitel 2) und die verwendete Software (Kapitel 3) beschrieben werden, widmet sich der Hauptteil (Kapitel 4-5) der Analyse der Gestaltungsprinzipien, Funktionslogik und Interaktionsmechanismen. Darauf aufbauend werden mögliche Ansätze zur praktischen Umsetzung von VR-Elementen vorgestellt (Kapitel 6) und ein Überblick über Chancen und Herausforderungen für zukünftige Anwendungen gegeben (Kapitel 7).
1.1 Definition
Bailey (2017) definiert Virtual Reality folgend: “Based on the immersion and presence literature, VR can be defined as a computing system with objective technological capabilities that creates a surrounding environment in which users feel psychologically located in and/or experience it as real. The technological affordances of VR systems create virtual environments with rich sensory fidelity that block out the physical world, which can influence how users think, feel, and behave.”

1.2 Wahrnehmung und ihre Bedeutung in virtuellen Umgebungen
Ein zentrales Thema im Kontext virtueller Realität ist die menschliche Wahrnehmung, wie sie unter anderem von Prof. Dr. Klaus Jenewein und Dipl.-Psych. Danica Hundt hervorgehoben wird. Sie betonen, dass Wahrnehmung in virtuellen Umgebungen keineswegs als rein passive Reaktion verstanden werden kann, sondern vielmehr als aktiver, kognitiver Prozess. Wahrnehmung umfasst demnach die Interpretation sensorischer Informationen aus der Umwelt in einer Weise, die für das Individuum bedeutungsvoll ist und angemessene Handlungen ermöglicht (Malim, 1994).
In virtuellen Umgebungen kann dieser Prozess durch immersive Elemente gezielt beeinflusst und intensiviert werden. Der Wahrnehmungsprozess beginnt mit der Reizaufnahme durch die Sinnesorgane und setzt sich fort über die kognitive Bewertung und Interpretation des Wahrgenommenen – ein Vorgang, der stark von individuellen Faktoren wie Erinnerungen, situativem Kontext und emotionalem Zustand geprägt ist (Malim, 1994).
Diese subjektive Komponente der Wahrnehmung bestimmt maßgeblich, wie Teilnehmende auf virtuelle Inhalte reagieren und welche emotionale wie auch kognitive Tiefe das Erleben in einer VR-Umgebung erreichen kann. Entsprechend spielt die bewusste Gestaltung der Wahrnehmungsreize in VR eine entscheidende Rolle für die immersive Qualität und damit den Erfolg einer virtuellen Anwendung.
2. Objekt
Im Rahmen des Projekts sollte die Ohlendorff-Villa als immersive, virtuelle Umgebung rekonstruiert werden. Mit den Möglichkeiten der virtuellen Realität soll das historische Gebäude nicht nur visuell, sondern auch räumlich und atmosphärisch erlebt werden. Ein hoher Immersionsgrad ermöglicht es den Nutzern, sich realistisch in der digitalen Repräsentation zu bewegen und ein Gefühl der Präsenz zu erleben - also den mentalen Zustand, sich tatsächlich in der virtuellen Umgebung zu befinden (vgl. Slater et al., 1998). Dies fördert nicht nur eine emotionale Bindung, sondern auch ein tieferes Verständnis für die historische Bedeutung des Ortes.
Die Villa befindet sich im Hamburger Stadtteil Volksdorf, wo sie zentral im alten Dorfkern liegt und heute unter Denkmalschutz steht. Als ehemaliger Wohnsitz der einflussreichen Kaufmannsfamilie von Ohlendorff und architektonisches Zeugnis der Zwischenkriegszeit, stellt sie ein bedeutendes Kulturgut dar.
Die Villa wurde 1928/29 vom Architekten Erich Elingius für Hans von Ohlendorff erbaut, nachdem das ursprüngliche Herrenhaus, ein Bau von Martin Haller aus dem Jahr 1878, abgerissen worden war. Der Neubau im klassizistischen Reformstil verbindet repräsentative Architektur mit privatem Wohnkomfort und spiegelt das Bild einer wohlhabenden Hamburger Familie wider (siehe Ohlendorffsche Villa, 2019, S. 2-6). Ihre prominente Lage, die symmetrische Eingangsfassade und die markanten Innenräume machen sie zu einem wichtigen Beispiel für die herrschaftliche Architektur ihrer Zeit - und damit zu einem idealen Ort für VR-gestützte Erinnerungskultur.








Software
Für das Projekt wurde die Unreal Engine, eine etablierte 3D-Engine für die Entwicklung von Spielen und Simulationen, verwendet, die sich insbesondere durch fotorealistisches Rendering, hohe Leistung und flexible Interaktionsmöglichkeiten auszeichnet. Dank des Blueprints-Systems bietet die Unreal Engine ein visuelles Skripting-Tool, mit dem komplexe Interaktionen ohne tiefgreifende Programmierkenntnisse entworfen werden können. So war es möglich, Benutzerinteraktionen wie das Bewegen durch Räume, das Aktivieren von Informationspunkten oder das Fokussieren auf architektonische Details direkt in die virtuelle Umgebung zu integrieren.
Ein weiterer Vorteil der Unreal Engine ist die Unterstützung von Virtual-Reality-Plattformen wie der HTC Vive, die ein immersives, räumliches Erlebnis im Maßstab 1:1 ermöglicht. Die Integration von hochwertigen Beleuchtungssimulationen, Materialsystemen und Post-Processing-Effekten trägt wesentlich zur realistischen Wahrnehmung der rekonstruierten Villa bei.
In Kombination mit 3D-Modellierungssoftware wie Blender - die zur Erstellung und Optimierung der geometrischen Strukturen verwendet wurde - ermöglichte Unreal eine effektive Kombination aus historischer Rekonstruktion, technischer Umsetzung und immersiver Kommunikation. Die Wahl dieser Softwaretools war somit entscheidend für das Erreichen des Projektziels, die Ohlendorff-Villa im virtuellen Raum möglichst authentisch und emotional erlebbar zu machen.








Daten
Grundlage des Projekts waren verschiedene digitale Daten, die in mehreren Schritten zur virtuellen Rekonstruktion der Villa Ohlendorff bearbeitet und in die Unreal Engine importiert wurden.
Das Hauptobjekt, ein 3D-Modell des Gebäudes, wurde im FBX-Format exportiert und in die Unreal Engine 5 importiert, wo eine weitere Texturierung und Platzierung auf dem vorbereiteten Terrain stattfand. Zusätzlich wurden Vegetationselemente wie Bäume, Sträucher und Wiesen aus der hauseigenen Bibliothek integriert, um dem Terrain ein realistisches Aussehen zu verleihen. Um die Immersion zu erhöhen, wurden weitere Umgebungseffekte integriert, darunter Wolken, Nebel und Lichteinstellungen für Tag- und Nachtzyklen sowie Umgebungssound. 

Interaktionsmechanismen
1.	Tuer 



Das in der Skizze dargestellte System ist die Logik einer interaktiven Kiste in einer virtuellen Umgebung, die als verschlossener Behälter fungiert. Die Kiste enthält ein wichtiges Objekt - in diesem Fall ein gestohlenes Gemälde - und kann nur unter bestimmten Bedingungen geöffnet werden: Der Benutzer gibt den richtigen Code ein.

Die Logik basiert auf einem Ereignisauslöser, der ausgelöst wird, sobald ein gültiger Code eingegeben wird. Nach erfolgreicher Eingabe wird ein Soundeffekt ('Play Sound at Location') abgespielt, um dem Benutzer eine hörbare Rückmeldung über den Erfolg der Eingabe zu geben. Dies dient nicht nur dem Eintauchen, sondern auch der intuitiven Führung des Benutzers.

Unmittelbar danach wird das Objekt „BP_gestohlenes_Bild“ - also das gestohlene Bild - in der Spielwelt mit Hilfe des Knotens „SpawnActor“ erzeugt. Die aktuelle Position der Truhe wird als Transformationsreferenz verwendet, so dass eine konstante Verschiebung in Z-Richtung über die Truhe definiert wird. Dadurch sieht das Bild an der gewünschten Position räumlich korrekt aus.

Darüber hinaus werden Parameter wie Skalierung, Drehung und Kollisionseigenschaften kontrolliert, so dass eine fehlerfreie Objektplatzierung gewährleistet ist. 

.


[^1]: My reference.
