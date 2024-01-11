<template>
  <section class="section">
    <div class="container is-max-desktop">
      <h1 class="title is-1 mb-6">Treppe hoch Vier</h1>

      <div class="box is-shadowless">
        <div class="content">
          <h2 class="title is-3">Die Fakten</h2>

          <table id="facts" class="table" style="width: auto">
            <tbody>
              <tr>
                <th>Was?</th>
                <td>Spendenlauf (Treppenlauf im Ausdauerformat)</td>
              </tr>
              <tr>
                <th>Für?</th>
                <td>
                  Förderkreis Ulm für tumor- und leukämiekranke Kinder Ulm e.V.
                </td>
              </tr>
              <tr>
                <th>Wann?</th>
                <td>Samstag, 02.03.24 09:30 - 19:00 Uhr</td>
              </tr>
              <tr>
                <th>Wo?</th>
                <td>Maritim Hotel Ulm</td>
              </tr>
              <tr>
                <th>Wer?</th>
                <td>Kostenlose Teilnahme auf Einladung</td>
              </tr>
            </tbody>
          </table>

          <h2 class="title is-3">Der Spendenlauf</h2>

          <p>
            Ein Kind, ein Erwachsener, ein Towerrunner & eine Rettungskraft
            (Feuerwehr, Polizei, THW, ..) sind vier Personen. Vier Personen die
            eine Treppe hochlaufen: <strong>Treppe hoch Vier</strong>!
          </p>

          <p>
            Gelaufen werden jeweils vier Runden pro Stunde. Was sich eigentlich
            ganz einfach anhört, wird im Laufe der Zeit zunehmend schwierig: Die
            Beine wollen nicht mehr, dem Körper reicht's auch - nur der Kopf
            sagt: Durchhalten! Auch deswegen ist das keine Sache die man alleine
            in Angriff nimmt. So wie überall im Leben, sind auch wir auch in
            diesem Fall gemeinsam stark.
          </p>

          <p>
            Von unten bis oben, sind es 318 Stufen. Die geht es in jeder Runde
            einmal hoch und dann wieder runter. Pro Stunde vier mal, macht 2'544
            Stufen in jeder Stunde. Das Ganze acht Stunden lang: 20'352 Stufen
          </p>

          <p>
            Um das zu unterstützen, spenden unsere Sponsoren einen Geldbetrag
            von 15 € pro gelaufener Runde
          </p>

          <h2 class="title is-3">Der Empfänger</h2>
          <p>
            <a href="https://www.foerderkreis-ulm.org"
              >Förderkreis Ulm für tumor- und leukämiekranke Kinder Ulm e.V.
            </a>
            Hier folgen weitere Informationen zur Tätigkeit des FKU
          </p>

          <h2 class="title is-3">Die Sponsoren</h2>

          <div class="columns is-multiline is-vcentered grid">
            <div class="column is-2 has-text-centered">
              <img src="/sponsoren/streidt.png" />
            </div>
          </div>

          <div class="is-clearfix">
            <h2 class="title is-3">Die Location</h2>

            <div class="columns">
              <div class="column is-2">
                <img src="/maritim-ulm.jpg" alt="" />
              </div>
              <div>
                Das
                <a href="https://www.maritim.de/de/hotels/deutschland/hotel-ulm"
                  >Maritim Hotel Ulm</a
                >
                liegt direkt an der Donau und eröffnet, insbesondere vom
                Restaurant in der 16. Etage, einen fantastischen Blick auf das
                Ulmer Münster sowie ganz Ulm und Neu-Ulm. Doch auch das Hotel
                selbst kann mit tollen Einblicken glänzen.
              </div>
            </div>
          </div>
          <h2 class="title is-3">Die Partner</h2>

          <div class="columns is-multiline is-vcentered grid">
            <div class="column is-4 has-text-centered">
              <img src="/partner/maritim.svg" />
            </div>
            <div class="column is-4 has-text-centered">
              <img src="/partner/donau3fm.svg" />
            </div>
          </div>

          <h2 class="title is-3">Die Möglichkeiten</h2>
          <p>Content für die Möglichkeiten</p>

          <h2 class="title is-3">Ihr Kontakt</h2>

          <div class="columns">
            <div class="column is-2">
              <img src="/stefan.jpg" />
            </div>
            <div class="column">
              Stefan Süßkind<br />
              ✉️
              <a href="mailto:stefan@treppe-hoch-vier.de"
                >stefan@treppe-hoch-vier.de</a
              ><br />
              📞 <a href="tel:+4916097048114">0160 940 48 114</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.content h2:not(:first-child) {
  margin-top: 2em;
}
.title:not(:last-child) {
  margin-bottom: 0.5rem;
}

#facts th {
  text-align: right;
}

.grid img {
  /*aspect-ratio: 3/2;*/
  filter: grayscale(1);
}
.grid img.invert {
  filter: invert(1);
}
.grid img.reduced {
  opacity: 0.7;
}
</style>
