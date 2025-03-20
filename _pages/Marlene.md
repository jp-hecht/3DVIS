---
title: "Bericht von Marlene"
permalink: /Marlene/
toc: true
toc_label: "Inhaltsverzeichnis"
author_profile: true
author:
  name     : "Marlene"
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


excerpt: "Ohlendorff’sche Villa - Vom Model zur VR-Visualisierung"
header:
  overlay_color: "#333"

---


[//]: # ()
# 1. Einleitung
In den letzten Jahrzehnten hat die bedeutung von Virtueller Realität (VR) an Bedeutung gewonnen und ist von einem wissenschaftlichen Konzept zu einer weit verbreiteten Technologie gewachsen. Inzwischen erlaubten spezialisierte Gertäte wie VR-Headset und dazugehörigen Steuerungselementen ein immersives Erleben digitaler Welten. Die Bedeutung dieser Technologie wächste kontinuierlich und findet Anwendung in einer Vielzahl von Bereichen, darunter Medizin, Bildung, Industrie und Unterhaltung (Slater & Sanchez-Vives, 2016)[^1]. Im Rahmen des Kursen 3D-Visualisierung, sollen die Studierenden ihre Kenntnisse in der Modellierung und dreidimensionlen Visualisierung von Geodaten ausbauen. Ziel ist dabei die interaktive Begehung eines Gebäudes, die in eine ebenfalls modelierte und gestaltete Umwelt eingebettet ist. Der Vorteil einer 3D-Visualisierung von Geodaten liegt in der realitätsnahen Darstellung komplexer räumlicher Strukturen und erweitert die Analysemöglichkeiten in Bereichen wie Stadtplanung, Umweltmonitoring und Geowissenschaften. Für Geoinformatik-Studierende ist sie daher vorteilhaft sich mit diesen Technologien auseinander zu setzen, um fundierte Entscheidungen zu unterstützen.
{: style="text-align: justify;"}
Unter Virtueller Realität versteht man eine computergenerierte Umgebung, die die physische Welt simuluiert bzw. erweitert oder eine erfundene Welt darstellt und eine immersive Erfahrung in dieser Welt ermöglicht. Nutzerende erleben VR durch spezielle Endgeräte wie Head-Mounted Displays (HMDs), die 3D-Bilder mit hoher Bildwiederholrate anzeigen, sowie durch Bewegungssensoren, die Interaktionen in Echtzeit erfassen. Ein zentrales Merkmal einer VR-Anwendung ist die Immersion, also das Gefühl, vollständig in der virtuellen Umgebung zu sein. Dies wird durch visuelle, auditive und haptischer Reize verstärkt (Burdea & Coiffet, 2003)[^2]. 
{: style="text-align: justify;"}
Die ersten Idenn der VR lassen sich im 19. Jahrhundert finden. Bereits 1838 entwickelte Sir Charles Wheatstone das Stereoskop, das durch zwei leicht versetzte Bilder eine dreidimensionale Wahrnehmung erzeugte (Wheatstone, 1838)[^3].
Die Grundlagen für moderne VR-Systeme wurden in den 1960er Jahren von Ivan Sutherland gelegt, der das "Ulimate Display" entwickelte. Dieses gilt als Vorläufer für moderne VR-Technologien. Das 1968 wntwickelte Head-Mounted Display gehörte zu den ersten Geräten mit denen es möglich war computergenerierte Bilder in Echtzeit zu visualisieren. Schon damals nannte Sutherland Immerson und Interaktivität als zentrale Elemente der VR (Sutherland, 1968)[^4]. 
{: style="text-align: justify;"}
In den 1980er Jahren wurde ein weiterer entscheidender Fortschritt erreicht, also Jaron Lanier mit seinem Unternehmen VPL Research die ersten kommerziellen VR-Systeme entwickelte, darunter auch Datenhandschuhe und VR-Brillen (Burdea & Coiffet, 2003)[^2]. Dennoch waren diese technologischen Innoviationen im Bereich der VR aufgrund der mangelnden Rechenleistung nicht massentauglich. Das änderte sich erst in den 2010er Jahren als durch gestiegene Rechenleistungen und konstengünstigere Sensorik eine massenhafte Verbreitung ermöglicht wurde. Seitdem wurden weitere Forschritte erzielt, insbesondere in den Bereichen Computergraphik, Sensorik und Mensch-Maschine-Interaktion. Die Entwicklung leistungsfähigerer Computer und fortschrittlicher Display-Technologien ermöglichte realistischere und immersivere VR-Erfahrungen (Grasnick, 2020)[^5]. 
{: style="text-align: justify;"}
Moderne VR-Technologien basieren auf einer Kombination aus Hochleistungscomputergrafik, Bewegungserkennung und immersiven Audio- sowie haptischen Rückmeldesystemen (LaValle, 2017). Die wichtigsten Komponenten eines VR-Systems sind:
- **Head-Mounted Displays (HMDs)**: Diese Geräte projizieren stereoskopische Bilder mit hoher Bildwiederholrate und niedriger Latenz, um Motion Sickness zu reduzieren.
- **Bewegungserfassung**: Durch Inside-Out-Tracking oder externe Sensoren werden Kopf- und Handbewegungen in Echtzeit erfasst.
- **Interaktive Eingabegeräte**: Controller oder Handschuhe mit haptischem Feedback ermöglichen die Manipulation virtueller Objekte.
- **Rendering-Engines**: Software-Plattformen wie Unreal Engine oder Unity ermöglichen die realitätsnahe Darstellung virtueller Welten.

Die Einsatzmöglichkeiten der VR-Technologie sind vielfältig und reichen von medizinischen Anwendungen über industrielle Nutzung bis hin zur Unterhaltung.
- **Medizinische Anwendungen**: VR wird in der Medizin zur Schmerztherapie, Behandlung von Angststörungen und für chirurgische Simulationen genutzt . Durch realitätsnahe Trainingssimulationen können Mediziner in einer sicheren Umgebung üben (Rizzo & Koenig, 2017).
- **Bildung und Training**: Immersive Lernumgebungen ermöglichen es Schülern und Studierenden, historische Ereignisse nachzuerleben oder komplexe Prozesse zu visualisieren (Freina & Ott, 2015).
- **Industrie und Design**: In der Produktentwicklung und Architektur wird VR zur Prototypenerstellung eingesetzt, wodurch Entwicklungszyklen verkürzt werden (Whyte et al., 2018).
- **Unterhaltung**: Die Spieleindustrie treibt die Weiterentwicklung von VR maßgeblich voran. Plattformen wie Oculus Quest oder PlayStation VR bieten ein intensives Spielerlebnis mit interaktiven Elementen (Zyda, 2005).
- **Psychologie und Therapie**: VR wird zunehmend zur Behandlung posttraumatischer Belastungsstörungen (PTBS) und anderer psychischer Erkrankungen genutzt (Gonçalves et al., 2020).

Die Virtuelle Realität hat sich von einem experimentellen Konzept zu einer vielfältig genutzten Technologie in vielen Anwendungsbereichen entwickelt. Wie die vorangegangene Entwicklung zeigt, wird aufgrund weiterer Fortschritte in Hardware und Software zukünftige VR-Systeme noch immersiver, realistischer und leichter zugänglich sein. Insbesondere die Integration von VR mit anderen Technologien wie Augmented Reality (AR) und Künstlicher Intelligenz (KI) wird neue Möglichkeiten eröffnen (Milgram & Kishino, 1994). 

[//]: # (Die Forschung konzentriert sich zunehmend auf die Verbesserung der Benutzererfahrung, Reduktion von Motion Sickness und die Erweiterung interaktiver Möglichkeiten.)  

Im Rahmen des Seminars "3D-Visualisierung" soll ein Projekt entwicklet werden, dass die realisitische Darstellung eine 3D-Modells und die Einbettung in eine immersive 3D-Umgebung zum Ziel hat. Dies hat zum Ziel, die Fähigkeiten der Studierenden im Bereich von digitaler (dreidimensionaler) Visualisierung zu erhöhen und die Kompetenz in den wachsenden Anwendungsfelder zu erweitern. Daber seht neben der realitätsnahen Visualisierung (Modellierung und Texturierung) eines 3D-Modells auch Interaktionen der SpielerIn mit der Umgebung im Vordergrund. Dieses schriftliche Ausarbeitung zeigt die dafür notwenigen Schritte auf. Dies sind folgende: 3D-Modellierung, Testaurierung und Einbindung in eine VR-Umgebung, sowie die Interaktionsmöglichkeiten. Schlussendlich werden auch die Herausforderungen beleuchtet und ein Fazit gezogen. 


# 2. Objekt

Woher haben wir das objekt, welche standen noch zu auswahl und warum haben wir und dafür entschiden

Im Zentrum unseres Projektes steht die Ohlendorff’sche Villa. Dabei handelt es sich um eine denmalgeschützte Villa aus dem Jahr 1929, die in Hamburg-Volksdorf steht. Die zweigeschossige Gebäude im Stil des Neoklassizismus, sollte nach der Erbauung sowohl als Einfamilienhaus wie auch als Repräsentationgebäude Hans von Ohlendorff dienen. Aus diesem Grund ist die Vorderseite des Gebäudes mit einem hervorgehobenen Portal und einem Erscheinungsbalkon auf ein imposantes Erscheinungsbild ausgerichtet. Um die Villa herum befindet sich ein Park, der ebenfalls Teil des Geländes ist. 
Heute wird die Villa von der "Stiftung Ohlendorff'sche Villa" geführt und beherbert ein Café, eine Kinderhort und mehrere Tagungsräume (*Die Ohlendorff'sche Villa*, o.J.).

## Daten
Damit der Ergebnis dieses Projektes, die Virtual-Reality-Anwendung (VR) eine realisitische und immersive Erfahrung ermöglicht ist eine sorgfältige Erfassung der Daten sowie eine Optimierung dieser erforderlich. Hochwertige 3D-Modelle, detaillierte Texturen und konsistente Daten sind essenziell, um eine glaubwürdige visuelle Darstellung sicherzustellen (Slater & Sanchez-Vives, 2016).
Die Erfassung von 3D-Objekten kann manuell in Modellierungssoftware erfolgen, erfordert jedoch Fachkenntnisse und Zeit. Alternativ bieten photogrammetrische Verfahren oder Laserscanning-Technologien eine automatisierte Erfassung realer Objekte in Form von Punktwolken. Diese können darufhin genutzt werden um 3D-Modelle zu generieren (Whyte et al., 2018). Prozedurale Generierungsmethoden ermöglichen zudem die automatische Erstellung komplexer Strukturen, sind jedoch oft weniger detailliert (Hermann, 2019).
Nach der Erfassung müssen die 3D-Modelle für VR optimiert werden. Dies umfasst die Reduktion der Polygonanzahl zur Verbesserung der Performance, das Backen von Texturen sowie den Einsatz von Level-of-Detail-Techniken (Dörner et al., 2019).

Die zur Verfügung gestellten Daten für das Modell der Ohlendorff'schen Villa enthielten eine FBX-Datei, Informationen zu den Maßen des Gebäudes und der einzelenen Räume, Metadaten (DWG-Datei), sowie eine virtual Tour und verschiedenste Bilder. Im weiteren Fortlauf des Projektes wurde hauptsächlich mit der FBX-Datei gearbeitet. 

[BILD VOM GESAMTEN MODELL]

Wie in der Abbildung zu erkennen, lässt sich die FBX-Datei in Blender öffnen und betrachten. Auf den ersten Blick wirkt das Modell passend und mit der Realität übereinstimend. Auch im Vergleich mit den Fotos, lässt sich das Modell als zutreffend bewerten. Bei näherer Betrachtung fällt jedoch auf, dass das Modell an einigen Stellen unsauber ist. Zum Beispiel ist zwischen Eingangsportal und Hauswand eine nicht unerhebliche Lücke. Außerdem sind die Fenster an der westlichen Hauswand nicht passend in die Aussparungen der Hauswand eingefügt worden, so sind auch hier Lücken zwischen Hauswand und Fensterrahmen zu finden. Ein weiteres Beispiel für die Mängel der Modellierung ist das Dachgesims an der Nordseite des Gebäudes, welches nicht die Verzierungen wie an der anderen Seiten hat, und zusätzlich, vermutlich durch die Überlagerunger mehrer Objekte, ein Flackern aufweist.

[BILDER DER DREI MÄNGEL]

Insgesamt stellen das Modell eine gute Grundlage dar, um das Modell für die VR-Anwendung zu entwickeln, da das große (übergeordnete) Erscheinungbild des Gebäudes mit der Realität übereinstimmt. Gleichzeitig ist noch Modellierungarbeit nötig, um die beschriebenen Mängel des Modell auszubessern, damit die finale VR-Anwendung ein realistisches und immersives Ergebnis erzielt. 

# 3. Konzept
Das Projekt verfolgt die Idee einer stilisierten 3D-Karte, die einen kleinen Ausschnitt der realen Welt, auf einer Scheibe, darstellt. Dieser Ausschnitt enthält die wesentlichen Wege, Straßen und umstehenden Gebäude in einer abstrahierten, kartografisch inspirierten Form. Dies ist eine Möglichkeit bekannte Karten, wie Google Maps oder Open Street Map, in einer 3D-Umgebung darzustellen. Die Darstellung kombiniert dabei realistische und abstrahierte Elemente, um Erkennbarkeit der Wirklichkeit und künstlerischer Freiheit zu vereinen.
Zentrales Element dieser Visualisierung ist die realitätsnah modellierte Ohlendorff'sche Villa, die mittig auf der Scheibe plaziert ist. Während das Gebäude in Bezug auf Architektur und Texturierung detailliert gestaltet ist, werden die umstehenden Gebäude in einer vereinfachenden Level-of-Detail-1-Darstellung abgeildet, also mit reduzierter geometrischer Komplexität. Dies hebt die Villa als Augenmerk der Visualisierung hervor und macht den bewusst gewählten Stilkontrast innerhalb der Visualisierung deutlich. Zusätzlich wird die Fläche, sprich der Außenbereich um die Villa, mit low-poly Bäumen und Autos ergänzt. Diese reduzierten Modelle verstärken den Gegensatz zwischen der detaillierten Texturierung der Villa und der stilisierten Umgebung, was dem zugrundeliegenden Konzept folgt.

Die Idee einer stilisierten 3D-Karte verbindet klassische kartografische Prinzipien mit modernen Möglichkeiten der dreidimensionalen Visualisierung. Im Gegensatz zu klassischen zweidimensionalen Karten, die eine Abstraktion der Realität wiedergeben, wird bei dreidimensionalen Karten eine weitere Informationsebene eingeführt. Hierbei können gezielt bestimmte Objekte hervorgehoben, Maßstäbe verzerrt oder Details reduziert werden, um die Wahrnehmung zu steuern (Jobst & Germanchis, 2007). Die für das Projekt gewählte Methodik nutzt diese Prinzipien, indem sie eine schematische Umgebung mit einem realistisch modellierten zentralen Objekt kombiniert. Ein solche Ansatz findet sich in verschiedenen Bereichen wieder, darunter Stadtplanung, Architekturvisualisierung und digitale Museumslandschaften (Kraak & Ormeling, 2020).

Die Villa im Zentrum der Szene wurde bewusst detaillierter gestaltet als die Umgebung. Sie orientiert sich in ihrer Form an dem realen Bauwerk, wobei die Texturen nicht der tatsächlichen Erscheinung entsprechen, sondern stilistisch an die gewählte Konzept angepasst wurden. Während einige Bereiche bewusst heruntergekommen wirken, finden sich an anderen Stellen luxuriöse Materialien wie Marmor, um eine geheimnissvollere Atmosphäre zu schaffen.
Die Gestallung des Gebäudes soll dabei die inhaltliche Idee unterstützen, dass die Villa als versteckter Ort für wertvolle Kunstgegenstände dient. Durch die Nutzung von Texturen, die neben Verfall auch Exklusivität darstellen, wird ein Ort geschaffen, der sowohl Geheimnisse birgt als auch den Reichtum der ausgestellten Objekte widerspiegelt. Der eingebaute Tag-Nacht-Modus unterstützt ebenfalls die geheimnissvolle Atmosphäre, wenn in der Nacht nicht mehr alle Gegenstände in der Villa ausgeleutet sind.

Das Innere der Villa ist in zwei thematische Räume unterteilt:
**Das Musikzimmer**: 
In diesem Raum sind verschiedene Musikinstrumente aus unterschiedlichen Teilen der Welt ausgestellt. Die Auswahl spiegelt eine kulturelle Vielfalt wider und lädt dazu ein, sich mit internationalen Klängen auseinanderzusetzen.
**Das Kunstzimmer**:
Hier werden fünf berühmte, aber verschollene oder gestohlene Kunstwerke inklusive eines Informationsplakat mit ihren Besonderheiten präsentiert. Dies verstärkt die narrative Komponente des Projekts: Die Villa dient als geheimer Aufbewahrungsort für wertvollen Werke. Die Gestaltung des Raumes mit hochwertigen Materialien wie Marmor schafft eine Umgebung, die dem Wert der ausgestellten Objekte gerecht wird, während andere Elemente bewusst abgenutzt wirken, um die mysteriöse Atmosphäre zu schaffen.

Das Projekt setzt sich zusammen aus eine katrographischen Basis, die bewusst reduziert wurden und ein realistischen Darstellung verschiedener Modelle mit großer Detailtiefe, um eine einzigartige 3D-Visualisierung zu kreieren. Durch den Kontrakt entsteht eine besondere, einzigartige Ästhetik. Gleichzeitig wird das Projekt durch die Innenraumgestaltung der Villa um eine sinnstiftende Erzählung erweitert, die das visuelle Konzept ergänzt und vertieft.

# 4. Software
Um die unterschiedlichen Teilaufgaben mit des Projekt durchführen zu können, wurde auf unterschiedliche Software zurückgegriffen. Da alle Mitglieder unserer Gruppe bisher keine Erfahrung im Bereich Modellierung, Texturierung oder VR-Interaktionen gemacht haben, erfolgte eine Neueinarbeitung in die Programmen. Für die Modellierung der Villa, um die oben beschriebenen Mängel auszubessern wurde die Software Blender verwendet. Bei Blender handelt es sich um eine Open Source Software, die für die Betriebssysteme Linux, Windows und macOS zur Verfügung steht, was in unserer Gruppe wichtig war, damit alle mit den unterschiedlichen Programmen arbeiten konnten. Das Blender einen sehr umfangreichen Werkzuegkasten für die Erstellung und Bearbeitung von 3D-Graphiken bereitstellt, haben wir uns entschieden auch die Texturen in Blender zu bearbeiten. 
Für die Erstellung einer virtuellen Realität, wurde sich für die Unreal Engine des Entwicklers Epic Games entschieden. Wie Blender kann die Software kostenlos heruntergelanden werden und eignet sich gut für die Erstellung von VR-Anwendungen. Hier lassen sich auch Interaktionen für die VR-Anwenung mithilfe von Blueprints erstellen, die am Ende ein immersiveres Erlebnis schaffen. 

# 5. Modellierung & Texturierung
## Modellierung
Die Modellierung der Villa erfolgte in Blender, wobei bereits die Grundstruktur des Gebäudes vorhanden war (s. Kapitel Daten). Der Fokus der weiteren Arbeit lag daher auf der Behebung kleinerer Unstimmigkeiten sowie der Verfeinerung der Geometrie, um ein möglichst realistisches Modell zu schaffen.
Wie bereits im Kapitel Daten beschrieben, wies das 3D-Modell der Ohlendorff'schen Villa einige kleinere Unstimmigkeiten auf. Zunächst wurden Lücken zwischen verschiedenen Objekten, wie beispielsweise zwischen dem Eingangsportal und der Gebäudewand, geschlossen. In einigen Fällen war es ausreichend, die Position der Objekte leicht zu justieren, während an anderen Stellen gezielt Anpassungen an den Geometrien vorgenommen wurden. So wurden etwa die Lücken zwischen Fensterrahmen und Gebäudewand durch das gezielte Verschieben einzelner Vertices sowie durch Anpassungen der Skalierung entlang der Achsen im Modellierungsprogramm behoben.
Des Weiteren wurden vier Fenster entfernt, die in das Dachmodell integriert worden waren. Die ursprünglich vorhandenen Fenster bestanden aus Volumenkörpern, die lediglich an den jeweiligen Positionen auf dem Dach platziert worden waren, ohne dass entsprechende Öffnungen im Dachmodell selbst existierten. Zudem waren an mehreren Gebäudeseiten die Fensterscheiben als eigenständige Volumenkörper modelliert, was in einigen Fällen dazu führte, dass sich zwei oder mehr überlappende Fensterscheiben an derselben Öffnung befanden. Diese überflüssigen Geometrien wurden entfernt, um eine saubere Modellstruktur zu gewährleisten.
Darüber hinaus wurde das Dachgesims an der Eingangsseite der Villa überarbeitet. Hierbei wurden Überlappungen zwischen der Gebäudewand und dem Gesims beseitigt, sodass eine konsistente und stimmige Architektur entstand. Zudem wurde im Erdgeschoss eine zusätzliche Innenwand modelliert, wodurch der offene Bereich in eine kleine Eingangshalle und zwei annähernd gleich große Räume unterteilt wurde. Diese dienten später als Kunst- und Musikraum.
Zum Abschluss wurde eine Eingangstreppe hinzugefügt, um den Zugang zur Villa innerhalb der VR-Umgebung zu ermöglichen. Da die Außenwelt konzeptionell auf einer flachen Plattform mit keinen Höhenunterschieden angelegt wurde, war die Schaffung eines angepassten Eingangsbereichs erforderlich. Diese Herausforderung wurde durch die Modellierung der Treppe gelöst.

Aufgrund der begrenzten Projektzeit und der vielfältigen weiteren Aufgaben im Rahmen der VR-Entwicklung wurde entschieden, kleinere Unstimmigkeiten am Modell in Kauf zu nehmen. Dieser pragmatische Ansatz ermöglichte es, sich auf nachfolgende Arbeitsschritte zu konzentrieren und die Modellierung effizient abzuschließen, ohne dass die finalen immersiven Qualitäten der VR-Anwendung erheblich beeinträchtigt wurden. 

## Texturierung
Für realistische und immersive VR-Anwendungen sind Texturen von großer Bedeutzung. Durch Texturen werden 3D-Objekten Oberflächenmerkmale wie Farben, Muster und Materialeigenschaften verliehen, wodurch diese Objekte in der VR-Anwendung glaubwürdierg und ansprechender wirken.
Durch den Einsatz von Techniken wie Texture Mapping, Bumpmapping und Parallax Mapping können Oberflächenstrukturen simuliert werden, die dem Benutzer das Gefühl vermitteln, sich in einer realen Umgebung zu befinden. Durch diese Methoden werden Details wie Rauheit, Glanz oder Unebenheiten dargestellt, ohne dad die Geometrie des Modells verändert werden muss, was sich auch positiv auf die Performacne der VR-Anwendung auswirkt. 
Texture Mapping ist eine zentrale Technik in der Computergrafik, die es ermöglicht, zweidimensionale Bildinformationen (Texturen) auf dreidimensionale Modelle zu projizieren. In VR-Anwendungen trägt Texture Mapping entscheidend dazu bei, die visuelle Echtheit der VR-Umgebung zu steigern. Durch die präzise Platzierung von Texturen auf 3D-Modellen können spezifische Materialien wie Holz, Metall oder Stein realistisch nachbildet werden. Ein wichtiger Aspekt des Texture Mappings ist das UV-Mapping. Hierbei wird die Oberfläche eines 3D-Modells auf eine zweidimensionale Ebene "abgewickelt", um die Textur passgenau aufzubringen. Dieser Prozess stellt sicher, dass die Textur ohne Verzerrungen oder Unstimmigkeiten auf dem Modell erscheint, was für die visuelle Qualität unerlässlich ist  (Dörner et al., 2019).

Da mit der Modellierung schon eine Einarbitung in Blender erfolgte, haben wir uns entschieden, die Texturierung ebenfalls mit Blender zu machen. Ein großer Vorteil von Blender bei der Textaurierung, dass ein Objekt mehrer Texturen aufweisen kann. Dafür können die einzelnen Faces ausgewählt werden, die einen Volumenkörper bilden und nur diesen eine bestimmte Textur zugewiesen werden. 
Um realitätsnahe Texturen zu schaffen, wurden frei verfügbare Texturen verwendet, die verschiedene Material- und Texturdaten enthielten, die in Blender importiert und gezielt auf 3D-Objekte angewendet wurden. Zu den wichtigsten Texture-Maps, die in diesem Projekt eingesetzt wurden, gehören:

- Color – Die Grundfarbtextur des Materials, welche das visuelle Erscheinungsbild der Oberfläche bestimmt.
- Normal Map – Enthält Informationen über die feinen Unebenheiten und Oberflächenstrukturen, ohne die Geometrie selbst zu verändern.
- Roughness Map – Steuert den Reflexionsgrad der Oberfläche, wobei dunklere Bereiche glänzender und hellere matter erscheinen.
- Metallic Map – Bestimmt, welche Bereiche der Textur metallisch erscheinen und welche nicht.

Diese Texturen wurden in Blender über den Shader Editor in das Materialsystem eingebunden und mit einem Principled BSDF Shader kombiniert, um eine realistische Licht- und Materialinteraktion zu erzeugen.

Da die importierten Texturen nicht automatisch optimal auf die 3D-Geometrie gemappt sind, musste ein manuelles UV-Mapping durchgeführt werden. Dabei wurden folgende Schritte vorgenommen:

- UV Unwrapping – Die Mesh-Oberflächen wurden entfaltet, um eine zweidimensionale Darstellung für die Texturen zu erstellen.
- UV-Optimierung – Durch das manuelle Verschieben der UV-Inseln in der UV-Editing-Ansicht wurde sichergestellt, dass keine Verzerrungen oder falschen Skalierungen auftraten.

Um sicherzustellen, dass die Texturen korrekt ausgerichtet sind, wurden verschiedene Mapping-Techniken wie Box Projection Mapping und Manual Projection Painting genutzt. Ziel der Texturierung war nicht die exakte Nachbildung der realen Oberflächen der Villa, sondern eine stilisierte, dennoch realistische Darstellung, die sich in das Gesamtkonzept der virtuellen Umgebung einfügt. Die gewählten Texturen sollten den visuellen Kontrakt zur Umgebung unterstreichen und die Villa damit in den Fokus rücken und die narrative Idee des Gesamtkonzepts unterstützen.

## Innenraumgestaltung
### Kunstzimmer
Das Kunstzimmer der Villa wurde mit besonderer Sorgfalt gestaltet, um eine Atmosphäre von Geheimnis und Entdeckung zu schaffen. An den Wänden hängen fünf bedeutende Kunstwerke, die entweder verschollen sind oder es einst waren:

- Fräulein Lieser von Gustav Klimt
- L'Olivier près de l'Estaque von Georges Braque
- View of Auvers-sur-Oise von Paul Cézanne
- The Painter on His Way to Work von Vincent van Gogh
- The Chorus von Edgar Degas

Neben jedem dieser Werke befindet sich ein Poster, das einen kurzen Einblick in die Geschichte des jeweiligen Bildes gibt und so den Besuchern Hintergrundinformationen liefert.
Zentral im Raum steht ein Untersuchungstisch, auf dem eine Lupe platziert ist. Diese lädt die Besucher dazu ein, die ausgestellten Gemälde genauer zu betrachten. Bei näherer Inspektion entdecken sie auf den fünf Bilder drei kleine Zahlen. Diese Zahlenkombination dient als Code für eine im Raum stehende Truhe. Geben die Besucher den korrekten Code ein, öffnet sich die Truhe, und das sechste Gemälde, The Concert von Johannes Vermeer, erscheint in der Raummitte.
The Concert gilt als das wertvollste gestohlene Kunstwerk der Welt. Es wurde 1990 aus dem Isabella Stewart Gardner Museum in Boston entwendet und hatte 2015 einen geschätzten Wert von 250 Millionen US-Dollar (Kurkjian, 2015). 
Diese interaktive Gestaltung des Kunstzimmers ermöglicht es den Besuchern, nicht nur die Kunstwerke zu bewundern, sondern auch aktiv an der Entdeckung des verborgenen Meisterwerks teilzunehmen.

### Musikzimmer
Das Musikzimmer der Villa wurde so konzipiert, dass es Besucher*innen auf eine akustische Reise durch verschiedene Kulturen und Epochen mitnimmt. Im Mittelpunkt stehen sieben Musikinstrumente aus unterschiedlichen Teilen der Welt:

- Klavier – Ein klassisches westliches Tasteninstrument, das seit Jahrhunderten in der Kunst- und Unterhaltungsmusik eine zentrale Rolle spielt.
- Guqin – Ein traditionelles chinesisches Saiteninstrument mit tiefen kulturellen Wurzeln, das für seine sanften, meditativen Klänge bekannt ist.
- Balalaika – Ein dreisaitiges Zupfinstrument aus Russland, das durch seinen charakteristischen Klang in der Folkmusik weit verbreitet ist.
- Djembe – Eine westafrikanische Trommel, die in rituellen und gemeinschaftlichen Kontexten für rhythmische Dynamik sorgt.
- Dombo – Ein traditionelles Instrument aus Südamerika, das durch seine einzigartigen Klangfarben besticht.
- Doncamatic – Eine frühe elektromechanische Rhythmusmaschine aus Japan, die in der modernen Musikproduktion große Bedeutung hat.
- Gitarre – Ein weltweit verbreitetes Saiteninstrument, das in unzähligen Musikstilen von Klassik bis Rock eingesetzt wird.

Um eine immersive Erfahrung zu schaffen, reagiert der Raum dynamisch auf die Bewegungen der Besucherinnen. Sobald man sich einem der Instrumente nähert, wird eine Klangsequenz abgespielt, die das jeweilige Instrument in einem typischen musikalischen Kontext präsentiert. Dies ermöglicht ein tiefgehendes Eintauchen in verschiedene Klangwelten und schafft eine interaktive Verbindung zwischen den Besucherinnen und den Musikinstrumenten.
Durch diese Gestaltung wird nicht nur ein visueller, sondern auch ein auditiver Zugang zu den ausgestellten Instrumenten ermöglicht. Dies verstärkt die Immersion in der virtuellen Umgebung und lädt dazu ein, die klangliche Vielfalt verschiedener Kulturen aktiv zu erleben.

# 6. Möglichkeiten zur VR-Umsetzung
Die Unreal Engine bietet eine leistungsstarke Umgebung für die Entwicklung von VR-Anwendungen und eignet sich daher besonders gut für ein Universitätsprojekt. Ein zentraler Vorteil ist die erstklassige Grafikqualität, die durch fortschrittliche Rendering-Technologien wie Lumen für dynamische Beleuchtung und Nanite für hochdetaillierte Modelle ermöglicht wird. Diese Features tragen entscheidend zur Immersion in der virtuellen Realität bei.
Ein weiterer wichtiger Aspekt ist die Benutzerfreundlichkeit der Engine. Dank der Blueprint-Skripting-Sprache können interaktive Elemente auch ohne tiefgehende Programmierkenntnisse erstellt werden, was den Einstieg erleichtert.
Zudem verfügt die Unreal Engine über eine optimierte VR-Unterstützung mit nativen Funktionen für Headsets wie Meta Quest, HTC Vive oder Valve Index. Die Engine bietet integrierte VR-Interaktionssysteme und performante Rendering-Techniken wie Variable Rate Shading (VRS), die für eine flüssige Darstellung in VR-Anwendungen essenziell sind (Epic Games, 2023). Seitens der Universität wurde uns eine HTV Vive zur Verfügung gestellt. Da Unreal Engine dieses Headset unterstützt war die Kompatibilität mit dieser Hardware kein Problem. 
Ein weiter wichtiger Punkt ist, dass Unreal Engine kostenlos verfügbar ist und entsprechend eine umfangreiche Community bietet, die zahlreiche Informationen und Beispiele online zur Verfügung stellen, die die Entwicklung einer VR-Anwendung unterstützen. 

## Umgebung

# 7. Fazit & Ausblick
# 8. Literatur
[^1]: Slater, Mel & Sanchez-Vives, Maria (2016). Enhancing Our Lives with Immersive Virtual Reality. Frontiers in Robotics and AI. 3. 10.3389/frobt.2016.00074. 
[^2]: Burdea, Grigore & Coiffet, Philippe (2003). Virtual Reality Technology. Presence. 12. 663-664. 10.1162/105474603322955950. 
[^3]: Wheatstone, Charles (2011). Contributions to the Physiology of Vision.—Part the First. On some remarkable, and hitherto unobserved, Phenomena of Binocular Vision. The Scientific Papers of Sir Charles Wheatstone. Cambridge University Press. pg. 225–283
[^4]: Sutherland, Ivan E. (1998). A head-mounted three dimensional display. Seminal graphics: pioneering efforts that shaped the field. Association for Computing Machinery Vol. 1, pg. 295–302. https://doi.org/10.1145/280811.281016
[^5]: Grasnick, Armin (2020). Grundlagen der virtuellen Realität: Von der Entdeckung der Perspektive bis zur VR-Brille. Springer Verlag. 10.1007/978-3-662-60785-5. 

- *Die Ohlendorff'sche Villa* (o.J.) Zugriff auf: https://ohlendorffsche.de/historie/ (6. März 2025).
- Dörner, R., Broll, W., Grimm, P. & Jung, B. (Hrsg.). (2019). *Virtual und augmented reality (vr/ar)* (2. Aufl.). Springer Vieweg Berlin, Heidelberg. Zugriff auf https:// doi.org/10.1007/978-3-662-58861-1 (Published: 11 October 2019) doi: 10 .1007/978-3-662-58861-1
- Epic Games (2023). *Virtual Reality Development with Unreal Engine.* Verfügbar unter: https://www.unrealengine.com
- Freina, L., & Ott, M. (2015). *A literature review on immersive virtual reality in education: State of the art and perspectives*. eLearning & Software for Education (eLSE).

- Gonçalves, R., Pedrozo, A. L., Coutinho, E. S., Figueira, I., & Ventura, P. (2020). *Efficacy of virtual reality exposure therapy in the treatment of PTSD: A systematic review*. PLoS ONE, 15(7).
- Hermann, S. (2019). *Prozedurale generierung von 3d-stadtmodellen (Bachelorarbeit).* Koblenz. (Zur Erlangung des Grades Bachelor of Science (B.Sc.) im Studiengang Computervisualistik).
- Jobst, M., & Germanchis, T. (2007). *The paradigm of 3D cartography.* Proceedings of the 23rd International Cartographic Conference (ICC).
- Kraak, M. J., & Ormeling, F. (2020). *Cartography: Visualization of spatial data.* Routledge.
- Kurkjian, Stephen (2015). *Master Thieves: The Boston Gangsters Who Pulled Off the World's Greatest Art Heist.* New York: PublicAffairs. ISBN 978-1-61039-632-5.

- LaValle, S. M. (2017). *Virtual Reality*. Cambridge University Press.
- Mazuryk, T., & Gervautz, M. (1996). *Virtual Reality—History, applications, technology and future*. Technical Report, TU Wien.
- Milgram, P., & Kishino, F. (1994). *A Taxonomy of Mixed Reality Visual Displays*. IEICE Transactions on Information and Systems.
- Rizzo, A., & Koenig, S. (2017). *Is clinical virtual reality ready for primetime?*. Neuropsychology.
- Slater, M. (2009). *Place illusion and plausibility can lead to realistic behaviour in immersive virtual environments*. Philosophical Transactions of the Royal Society.
- Slater, M., & Sanchez-Vives, M. V. (2016). *Enhancing our lives with immersive virtual reality*. Frontiers in Robotics and AI.
- Sutherland, I. (1968). *A head-mounted three-dimensional display*. Proceedings of the AFIPS Fall Joint Computer Conference.
- Whyte, J., Bouchlaghem, D., Thorpe, A., & McCaffer, R. (2018). *From CAD to virtual reality: modelling approaches, data exchange and interactive 3D building design tools*. Automation in Construction.
- Zyda, M. (2005). *From visual simulation to virtual reality to games*. IEEE Computer.
