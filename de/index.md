---
layout: Post
title: Web-Vitals
description: Wesentliche Kennzahlen für eine gesunde Website
hero: image/admin/BHaoqqR73jDWe6FL2kfw.png
authors:
  - Philipwalton
date: 30.04.2020
updated: 21.07.2020
tags:
  - Metriken
  - Leistung
  - Web-Vitals
---

Die Optimierung der Qualität der Benutzererfahrung ist der Schlüssel zum langfristigen Erfolg jeder Website im Internet. Unabhängig davon, ob Sie Geschäftsinhaber, Vermarkter oder Entwickler sind, kann Web Vitals Ihnen dabei helfen, das Erlebnis Ihrer Website zu quantifizieren und Verbesserungsmöglichkeiten zu identifizieren.

## Überblick

Web Vitals ist eine Initiative von Google zur Bereitstellung einheitlicher Leitlinien für Qualitätssignale, die für die Bereitstellung eines großartigen Benutzererlebnisses im Web unerlässlich sind.

Google hat im Laufe der Jahre eine Reihe von Tools bereitgestellt, um die Leistung zu messen und darüber zu berichten. Einige Entwickler sind Experten im Umgang mit diesen Tools, während andere es als schwierig empfinden, mit der Fülle an Tools und Metriken Schritt zu halten.

Websitebesitzer sollten keine Leistungsgurus sein, um die Qualität der Erfahrung zu verstehen, die sie ihren Benutzern bieten. Die Web Vitals-Initiative zielt darauf ab, die Landschaft zu vereinfachen und Websites dabei zu helfen, sich auf die Kennzahlen zu konzentrieren, die am wichtigsten sind, die **Core Web Vitals** .

## Kern-Web-Vitals

Core Web Vitals sind die Teilmenge der Web Vitals, die für alle Webseiten gelten, von allen Websitebesitzern gemessen werden sollten und in allen Google-Tools angezeigt werden. Jeder der Core Web Vitals stellt eine bestimmte Facette des Benutzererlebnisses dar, ist [vor Ort](/user-centric-performance-metrics/#how-metrics-are-measured) messbar und spiegelt die reale Erfahrung eines kritischen [benutzerzentrierten](/user-centric-performance-metrics/#how-metrics-are-measured) Ergebnisses wider.

Die Kennzahlen, aus denen sich die Core Web Vitals zusammensetzen, werden sich im Laufe der Zeit [weiterentwickeln](#evolving-web-vitals) . Das aktuelle Set für 2020 konzentriert sich auf drei Aspekte des Benutzererlebnisses – *Laden* , *Interaktivität* und *visuelle Stabilität* – und umfasst die folgenden Metriken (und ihre jeweiligen Schwellenwerte):

<div class="w-stack w-stack--center w-stack--md">   <img src="lcp_ux.svg" width="400px" height="350px" alt="Größte Contentful Paint-Grenzwertempfehlungen"><img src="fid_ux.svg" width="400px" height="350px" alt="Empfehlungen zum Schwellenwert für die erste Eingabeverzögerung"><img src="cls_ux.svg" width="400px" height="350px" alt="Schwellenwertempfehlungen für die kumulative Layoutverschiebung"> </div>

- **[Largest Contentful Paint (LCP)](/lcp/)** : misst die *Ladeleistung* . Um ein gutes Benutzererlebnis zu gewährleisten, sollte LCP innerhalb von **2,5 Sekunden** nach dem ersten Ladevorgang der Seite erfolgen.
- **[First Input Delay (FID)](/fid/)** : misst *die Interaktivität* . Um eine gute Benutzererfahrung zu bieten, sollten Seiten eine FID von weniger als **100 Millisekunden** haben.
- **[Cumulative Layout Shift (CLS)](/cls/)** : misst *die visuelle Stabilität* . Um eine gute Benutzererfahrung zu bieten, sollten Seiten einen CLS von weniger als **0,1 aufweisen.**

Um sicherzustellen, dass Sie für jede der oben genannten Kennzahlen das empfohlene Ziel für die meisten Ihrer Benutzer erreichen, ist ein guter Schwellenwert zum Messen das **75. Perzentil** der Seitenladevorgänge, segmentiert nach Mobil- und Desktop-Geräten.

Tools, die die Einhaltung der Core Web Vitals bewerten, sollten eine Page Passing in Betracht ziehen, wenn sie die empfohlenen Ziele beim 75. Perzentil für alle oben genannten drei Metriken erreicht.

{% Aside %} Weitere Informationen zur Forschung und Methodik hinter diesen Empfehlungen finden Sie unter: [Definieren der Schwellenwerte für Core Web Vitals-Metriken](/defining-core-web-vitals-thresholds/) {% endAside %}

### Tools zum Messen und Berichten von Core Web Vitals

Google ist davon überzeugt, dass die Core Web Vitals für alle Web-Erlebnisse von entscheidender Bedeutung sind. Aus diesem Grund ist das Unternehmen bestrebt, diese Kennzahlen [in allen seinen beliebten Tools](/vitals-tools/) zur Verfügung zu stellen. In den folgenden Abschnitten wird detailliert beschrieben, welche Tools die Core Web Vitals unterstützen.

#### Feldtools zur Messung der Core Web Vitals

Der[Chrome User Experience Report](https://developers.google.com/web/tools/chrome-user-experience-report) sammelt anonymisierte, reale Benutzermessdaten für jedes Core Web Vital. Diese Daten ermöglichen Websitebesitzern eine schnelle Bewertung ihrer Leistung, ohne dass sie manuell Analysen auf ihren Seiten durchführen müssen, und unterstützen Tools wie [PageSpeed ​​Insights](https://developers.google.com/speed/pagespeed/insights/) und [den Core Web Vitals-Bericht](https://support.google.com/webmasters/answer/9205520) der Search Console.

<div class="w-table-wrapper">
  <table>
    <tr>
      <td> </td>
      <td>LCP</td>
      <td>FID</td>
      <td>CLS</td>
    </tr>
    <tr>
      <td><a href="https://developers.google.com/web/tools/chrome-user-experience-report">Chrome-Benutzererfahrungsbericht</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
    <tr>
      <td><a href="https://developers.google.com/speed/pagespeed/insights/">PageSpeed-Einblicke</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
    <tr>
      <td><a href="https://support.google.com/webmasters/answer/9205520">Search Console (Core Web Vitals-Bericht)</a></td>
      <td>✔</td>
      <td>✔</td>
      <td>✔</td>
    </tr>
  </table>
</div>

{% Aside %} Anleitungen zur Verwendung dieser Tools und welches Tool für Ihren Anwendungsfall das richtige ist, finden Sie unter: [Erste Schritte mit der Messung von Web Vitals](/vitals-measurement-getting-started/) {% endAside %}

Die vom Chrome User Experience Report bereitgestellten Daten bieten eine schnelle Möglichkeit, die Leistung von Websites zu bewerten, liefern jedoch nicht die detaillierte Telemetrie pro Seitenaufruf, die oft erforderlich ist, um Regressionen genau zu diagnostizieren, zu überwachen und schnell darauf zu reagieren. Aus diesem Grund empfehlen wir Websites dringend, eine eigene Echtzeitüberwachung einzurichten.

#### Messen Sie die wichtigsten Web-Vitalwerte in JavaScript

Jeder der Core Web Vitals kann in JavaScript mithilfe von Standard-Web-APIs gemessen werden.

Der einfachste Weg, alle Core Web Vitals zu messen, ist die Verwendung der [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) JavaScript-Bibliothek, einem kleinen, produktionsbereiten Wrapper um die zugrunde liegenden Web-APIs, der jede Metrik auf eine Weise misst, die genau der Art und Weise entspricht, wie sie von allen gemeldet wird Die oben aufgeführten Google-Tools.

Mit der [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek ist das Messen jeder Metrik so einfach wie das Aufrufen einer einzelnen Funktion (die vollständige [Verwendung](https://github.com/GoogleChrome/web-vitals#usage) und [API-](https://github.com/GoogleChrome/web-vitals#api) Details finden Sie in der Dokumentation):

```js
import {getCLS, getFID, getLCP} from 'web-vitals';

function sendToAnalytics(metric) {
  const body = JSON.stringify(metric);
  // Use `navigator.sendBeacon()` if available, falling back to `fetch()`.
  (navigator.sendBeacon && navigator.sendBeacon('/analytics', body)) ||
      fetch('/analytics', {body, method: 'POST', keepalive: true});
}

getCLS(sendToAnalytics);
getFID(sendToAnalytics);
getLCP(sendToAnalytics);
```

Sobald Sie Ihre Website so konfiguriert haben, dass sie die [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek verwendet, um Ihre Core Web Vitals-Daten zu messen und an einen Analyseendpunkt zu senden, besteht der nächste Schritt darin, diese Daten zu aggregieren und Berichte darüber zu erstellen, um zu sehen, ob Ihre Seiten die empfohlenen Schwellenwerte erreichen mindestens 75 % der Seitenaufrufe.

Während einige Analyseanbieter über integrierte Unterstützung für Core Web Vitals-Metriken verfügen, sollten auch diejenigen, die dies nicht bieten, grundlegende benutzerdefinierte Metrikfunktionen enthalten, mit denen Sie Core Web Vitals in ihrem Tool messen können.

Ein Beispiel hierfür ist der [Web Vitals Report](https://github.com/GoogleChromeLabs/web-vitals-report) , der es Websitebesitzern ermöglicht, ihre Core Web Vitals mithilfe von Google Analytics zu messen. Anleitungen zur Messung von Core Web Vitals mit anderen Analysetools finden Sie unter [Best Practices für die Messung von Web Vitals in der Praxis](/vitals-field-measurement-best-practices/) .

Mit der [Web Vitals-Chrome-Erweiterung](https://github.com/GoogleChrome/web-vitals-extension) können Sie auch Berichte zu jedem der Core Web Vitals erstellen, ohne Code schreiben zu müssen. Diese Erweiterung verwendet die [Web-Vitals-](https://github.com/GoogleChrome/web-vitals) Bibliothek, um jede dieser Metriken zu messen und sie Benutzern beim Surfen im Internet anzuzeigen.

Diese Erweiterung kann hilfreich sein, um die Leistung Ihrer eigenen Websites, der Websites Ihrer Mitbewerber und des gesamten Webs zu verstehen.

<div class="w-table-wrapper">
  <table>
    <thead>
      <tr>
        <th> </th>
        <th>LCP</th>
        <th>FID</th>
        <th>CLS</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a href="https://github.com/GoogleChrome/web-vitals">Web-Vitals</a></td>
        <td>✔</td>
        <td>✔</td>
        <td>✔</td>
      </tr>
      <tr>
        <td><a href="https://github.com/GoogleChrome/web-vitals-extension">Web Vitals-Erweiterung</a></td>
        <td>✔</td>
        <td>✔</td>
        <td>✔</td>
      </tr>
    </tbody>
  </table>
</div>

Alternativ können Entwickler, die diese Metriken lieber direkt über die zugrunde liegenden Web-APIs messen möchten, für Implementierungsdetails auf diese Metrikleitfäden verweisen:

- [LCP in JavaScript messen](/lcp/#measure-lcp-in-javascript)
- [FID in JavaScript messen](/fid/#measure-fid-in-javascript)
- [CLS in JavaScript messen](/cls/#measure-cls-in-javascript)

{% Aside %} Weitere Anleitungen zur Messung dieser Metriken mit beliebten Analysediensten (oder Ihren eigenen internen Analysetools) finden Sie unter: [Best Practices für die Messung von Web Vitals im Feld](/vitals-field-measurement-best-practices/) {% endAside %}

#### Labortools zur Messung der Core Web Vitals

Während es sich bei allen Core Web Vitals in erster Linie um Feldmetriken handelt, sind viele davon auch im Labor messbar.

Labormessungen sind die beste Möglichkeit, die Leistung von Funktionen während der Entwicklung zu testen – bevor sie für Benutzer freigegeben werden. Dies ist auch die beste Möglichkeit, Leistungsrückgänge zu erkennen, bevor sie auftreten.

Die folgenden Tools können zur Messung der Core Web Vitals in einer Laborumgebung verwendet werden:

<div class="w-table-wrapper">
  <table>
    <thead>
      <tr>
        <th> </th>
        <th>LCP</th>
        <th>FID</th>
        <th>CLS</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><a href="https://developers.google.com/web/tools/chrome-devtools">Chrome DevTools</a></td>
        <td>✔</td>
        <td>✘ (stattdessen <a href="/tbt/">TBT</a> verwenden)</td>
        <td>✔</td>
      </tr>
      <tr>
        <td><a href="https://developers.google.com/web/tools/lighthouse">Leuchtturm</a></td>
        <td>✔</td>
        <td>✘ (stattdessen <a href="/tbt/">TBT</a> verwenden)</td>
        <td>✔</td>
      </tr>
    </tbody>
  </table>
</div>

{% Aside %} Tools wie Lighthouse, die Seiten in einer simulierten Umgebung ohne Benutzer laden, können die FID nicht messen (es erfolgt keine Benutzereingabe). Die Gesamtblockierzeit (TBT) ist jedoch im Labor messbar und ein hervorragender Indikator für FID. Leistungsoptimierungen, die die TBT im Labor verbessern, sollten die FID im Feld verbessern (siehe Leistungsempfehlungen unten). {% endAside %}

Während Labormessungen ein wesentlicher Bestandteil für die Bereitstellung großartiger Erlebnisse sind, sind sie kein Ersatz für Feldmessungen.

Die Leistung einer Website kann je nach den Gerätefunktionen eines Benutzers, seinen Netzwerkbedingungen, anderen möglicherweise auf dem Gerät ausgeführten Prozessen und der Art und Weise, wie er mit der Seite interagiert, erheblich variieren. Tatsächlich kann die Bewertung jeder der Core Web Vitals-Metriken durch Benutzerinteraktion beeinflusst werden. Nur eine Feldmessung kann das vollständige Bild genau erfassen.

### Empfehlungen zur Verbesserung Ihrer Punktzahl

Sobald Sie die Core Web Vitals gemessen und Verbesserungsmöglichkeiten identifiziert haben, besteht der nächste Schritt in der Optimierung. Die folgenden Leitfäden bieten spezifische Empfehlungen zur Optimierung Ihrer Seiten für die einzelnen Core Web Vitals:

- [LCP optimieren](/optimize-lcp/)
- [FID optimieren](/optimize-fid/)
- [CLS optimieren](/optimize-cls/)

## Andere Web-Vitals

Während die Core Web Vitals die entscheidenden Kennzahlen für das Verständnis und die Bereitstellung einer großartigen Benutzererfahrung sind, gibt es noch andere wichtige Kennzahlen.

Diese anderen Web Vitals dienen häufig als Proxy- oder ergänzende Metriken für die Core Web Vitals, um dabei zu helfen, einen größeren Teil des Erlebnisses zu erfassen oder bei der Diagnose eines bestimmten Problems zu helfen.

Beispielsweise sind die Metriken [„Time to First Byte“ (TTFB)](/time-to-first-byte/) und [„First Contentful Paint“ (FCP)](/fcp/) beide wichtige Aspekte des *Ladeerlebnisses* und beide nützlich bei der Diagnose von Problemen mit LCP (langsame [Serverantwortzeiten](/overloaded-server/) bzw. [Render-blockierende Ressourcen](/render-blocking-resources/) ). .

Ebenso sind Metriken wie [Total Blocking Time (TBT)](/tbt/) und [Time to Interactive (TTI)](/tti/) Labormetriken, die für die Erkennung und Diagnose potenzieller *Interaktivitätsprobleme* , die sich auf FID auswirken, von entscheidender Bedeutung sind. Sie sind jedoch nicht Teil des Core Web Vitals-Sets, da sie weder vor Ort messbar sind noch ein [benutzerzentriertes](/user-centric-performance-metrics/#how-metrics-are-measured) Ergebnis widerspiegeln.

## Sich weiterentwickelnde Web-Vitals

Web Vitals und Core Web Vitals stellen die besten verfügbaren Signale dar, die Entwickler heute haben, um die Qualität der Erfahrung im gesamten Web zu messen. Diese Signale sind jedoch nicht perfekt und zukünftige Verbesserungen oder Ergänzungen sind zu erwarten.

Die **Core Web Vitals** sind für alle Webseiten relevant und werden in relevanten Google-Tools angezeigt. Änderungen an diesen Kennzahlen werden weitreichende Auswirkungen haben; Daher sollten Entwickler damit rechnen, dass die Definitionen und Schwellenwerte der Core Web Vitals stabil sind und Aktualisierungen im Voraus angekündigt werden und einen vorhersehbaren jährlichen Rhythmus haben.

Die anderen Web Vitals sind häufig kontext- oder werkzeugspezifisch und möglicherweise experimenteller als die Core Web Vitals. Daher können sich ihre Definitionen und Schwellenwerte häufiger ändern.

Für alle Web Vitals werden Änderungen in diesem öffentlichen [CHANGELOG](http://bit.ly/chrome-speed-metrics-changelog) klar dokumentiert.
