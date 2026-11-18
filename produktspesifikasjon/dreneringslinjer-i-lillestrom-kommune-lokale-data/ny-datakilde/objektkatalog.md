### Datamodell

**Kilde:** [SOSI UML XMI-fil](https://sosi.geonorge.no/svn/SOSI/SOSI%20Del%202/Stedsnavn.xml)

<a href="ny-datakilde_feature_catalogue.png" title="Klikk for stor visning"><img src="ny-datakilde_feature_catalogue.png" alt="Datamodell Ny datakilde" style="max-width: 100%; height: auto;" /></a>

#### Vedtaksområde

Skal brukes for å vise utstrekningen av et samlevedtak. Et gitt vedtaksområde kan brukes av flere samlevedtak.

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>område</td>
      <td>Område er et slags navn for å lettere kunne søke opp vedtaksområdet og gjenbruke det i andre samlevedtak. Vedtaksområdene vil som regel være et administrativt område, jf. stedsnavnloven § 5 tredje ledd, men det kan ha blitt registrert gjort samlevdtak utover disse. I fremtiden kan man også se for seg en endring som gjør at det må vær mulig å gjøre samlevedtak med helt andre vedtaksområder enn kun innenfor et administrativt område.</td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
    <tr>
      <td>oppdatertdato</td>
      <td>Dato for siste oppdatering.</td>
      <td>Date<wbr />Time</td>
      <td>1</td>
    </tr>
    <tr>
      <td>polygon</td>
      <td>Geometri for vedtaksområde.</td>
      <td>GM_<wbr />Surface</td>
      <td>1</td>
    </tr>
    <tr>
      <td>registrertdato</td>
      <td>Dato for første registrering.</td>
      <td>Date<wbr />Time</td>
      <td>1</td>
    </tr>
  </tbody>
</table>

#### Sted

Sted inneholder all egenskapene som er felles for de ulike stedsnavnene (og deres skrivemåter) for en lokalitet, uavhengig av språk.<br /><br />Med felles egenskaper menes posisjon, presentasjonsinformasjon, land, kommune, matrikkelnummer, navnetype, osv.

Egenskaper

<table class="feature-attribute-table">
  <thead>
    <tr>
      <th>Egenskap</th>
      <th>Beskrivelse</th>
      <th>Type</th>
      <th>Multiplisitet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>land</td>
      <td>Hvilke land steder ligger i.<br /><br />Tobokstavers kodeliste, subsett av ISO 3166-1 alpha-2.</td>
      <td><a href="#kodeliste-landkode">Land<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>navneobjekthovedgruppe</td>
      <td>Hovedgruppene følger i hovedsak Inspire "NamedPlaceTypeValue", men populatedPlace og building er samlet under bebyggelse og hydrography er delt mellom sjø og ferskvann.</td>
      <td><a href="#kodeliste-navneobjekthovedgruppe">Navneobjekthovedgruppe</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>navneobjektgruppe</td>
      <td>Inndeling i kategorier under hver hovedgruppe.</td>
      <td><a href="#kodeliste-navneobjektgruppe">Navneobjektgruppe</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>navneobjekttype</td>
      <td>Stedets navneobjekttype er en underinndeling av navneobjektgruppene som igjen er inndeling av navneobjekthovedgruppene.</td>
      <td><a href="#kodeliste-navneobjekttype">Navneobjekttype</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>posisjon</td>
      <td>Stedfesting av objektet med eller uten utstrekning. Flate, kurve, punkt eller punktsky.</td>
      <td>GM_<wbr />Object</td>
      <td>1</td>
    </tr>
    <tr>
      <td>sortering</td>
      <td>Sorteringsegenskapene skal benyttes til å angi stedets viktighet i forskjellige målestokker (i forhold til andre stedsnavn).</td>
      <td>Sortering<br />(datatype)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- sortering1<wbr />Kode</td>
      <td>Bokstavkode fra A til N der N er viktigste objekttype som tegnes først, mens A er de minst viktige som vises dersom det er plass.</td>
      <td><a href="#kodeliste-sortering1kode">Sortering1<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- sortering2<wbr />Kode</td>
      <td>Tall fra 1 til 99 som brukes til å sortere innefor sortering1kode, der 99 har høyest prioritet.</td>
      <td><a href="#kodeliste-sortering2kode">Sortering2<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>stedstatus</td>
      <td>Stedstatus forteller om stedet (navneobjektet) eksisterer, er historisk eller er planlagt.</td>
      <td><a href="#kodeliste-stedstatuskode">Stedstatus<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>språkprioritering</td>
      <td>Angir rekkefølgen av navn på forskjellige språk som skal vises på skilt og kart, jf. forskriften § 7 annet ledd.</td>
      <td><a href="#kodeliste-språkprioriteringkode">Språkprioritering<wbr />Kode</a><br />(kodeliste)</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>tilleggsopplysninger</td>
      <td>Her kan registerføreren legge inn opplysninger som er relevante for stedet.</td>
      <td>Tilleggsopplysning<br />(datatype)</td>
      <td>0..*</td>
    </tr>
    <tr>
      <td>- eksterne<wbr />Opplysninger</td>
      <td>Lenke til opplysnnger som ligger utenfor registeret/databasen, for eksempel en nettside.</td>
      <td>URI</td>
      <td>0..1</td>
    </tr>
    <tr>
      <td>- oppdateringsdato</td>
      <td>Dato for siste oppdatering.</td>
      <td>Date<wbr />Time</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- registreringsdato</td>
      <td>Dato for første registrering.</td>
      <td>Date<wbr />Time</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- tekst</td>
      <td>Her føres opplysninger som ikke er direkte knyttet til etymologi.</td>
      <td>Character<wbr />String</td>
      <td>0..*</td>
    </tr>
    <tr>
      <td>- tilleggsopplysningstype</td>
      <td>Viser hvilken type opplysning dette er. For eksempel kan en slik kode være "språkfaglig", som brukes når navneansvarlig ser behov for utdypende informasjon om et stedsnavns opphav.</td>
      <td><a href="#kodeliste-tilleggsopplysningtypekode">Tilleggsopplysningtype<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>stedsnummer</td>
      <td>Stedsnummer, stedsnavnsnummer og skrivemåtenummer skal sammen utgjøre en såkalt tematisk id som brukes av registerførere som opplslagsnummer. Identifikatoren ligner litt på Gnr/Bnr/Fnr.<br /><br />Stedsnummeret er et løpende nummer systemet gir stedet som en identifikator. Stedsnummeret er unikt og kan ikke brukes om igjen.</td>
      <td>Integer</td>
      <td>1</td>
    </tr>
    <tr>
      <td>vedtaksmyndighet</td>
      <td>Vedtaksmyndigheten er bestemt av loven og avhengig av navneobjekttype og geografisk beliggenhet.</td>
      <td><a href="#kodeliste-vedtaksmyndighetkode">Vedtaksmyndighet<wbr />Kode</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>kommune</td>
      <td></td>
      <td>Kommune<br />(datatype)</td>
      <td>0..*</td>
    </tr>
    <tr>
      <td>- kommunenummer</td>
      <td></td>
      <td><a href="#kodeliste-kommunenummer">Kommunenummer</a><br />(kodeliste)</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- kommunenavn</td>
      <td>Navnet på kommunen, navnet vises på flere språk dersom kommunen er flerspråklig.</td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- fylkesnummer</td>
      <td></td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
    <tr>
      <td>- fylkesnavn</td>
      <td>Navnet på fylket, navnet vises på flere språk med riktig rekkefølge på spårkene dersom fylket er flerspråklig.</td>
      <td>Character<wbr />String</td>
      <td>1</td>
    </tr>
  </tbody>
</table>

Relasjoner

**Assosiasjoner**
Stedsnavn – rolle: stedsnavn – kardinalitet: 1..*
Matrikkelreferanse – rolle: matrikkelreferanse – kardinalitet: 0..1

### Kodelister

#### <a id="kodeliste-landkode"></a>«CodeList» LandKode

**Definisjon:** Landkoder, subsett av&lt;b&gt; ISO 3166-1 alpha-2&lt;/b&gt; som kun inneholder de landkodene som vi har bruk for for å konvertere SSR til SSR 2.0. Etter produksjonsetting utvides kodelista ved behov.

Merk: XZ - "Internasjonalt farvann" og ZZ "Uspesifisert" er brukerdefinerte koder (tillatt etter ISO-beskrivelsen). Det vil si at koden ikke har noen bestemt betydning i ISO-kodelista, og vår kodeliste må være tilgjengelig for at eksterne parter kan tolke vår bruk av kodeverdiene.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/LandKode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/LandKode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Norge</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Danmark</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Sverige</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Finland</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Island</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Grønland</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Russland</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Storbritannia</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Tyskland</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Svalbard_og_Jan_Mayen</td>
      <td>Svalbard og Jan Mayen</td>
      <td></td>
    </tr>
    <tr>
      <td>Færøyene</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>internasjonaltFarvann</td>
      <td>Brukerdefinert</td>
      <td></td>
    </tr>
    <tr>
      <td>uspesifisert</td>
      <td>Brukerdefinert</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-navneobjekthovedgruppe"></a>«CodeList» Navneobjekthovedgruppe

**Definisjon:** Hovedgruppering av navneobjekttypene. Hovedgruppene følger i hovedsak Inspire "NamedPlaceTypeValue", men populatedPlace og building er samlet under bebyggelse og hydrography er delt mellom sjø og ferskvann.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjekthovedgruppe">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjekthovedgruppe</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>terreng</td>
      <td>Alle  grupper som beskriver terrengformasjoner.
Tilsvarer Inspire temaet "landform".</td>
      <td></td>
    </tr>
    <tr>
      <td>markslag</td>
      <td>Alle grupper som er relevante under hovedgruppe Markslag. Tilsvarer Inspire temaet "landcover".</td>
      <td></td>
    </tr>
    <tr>
      <td>ferskvann</td>
      <td>Alle grupper som er relevante under hovedgruppe Ferskvann. Under Inspire temaet "hydrography" som vi har delt i to.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjø</td>
      <td>Alle grupper som er relevante under hovedgruppe Sjø. Under Inspire temaet "hydrography" som vi har delt i to.</td>
      <td></td>
    </tr>
    <tr>
      <td>bebyggelse</td>
      <td>Alle grupper som er relevante under hovedgruppe bebyggelse. Tilsvarer Inspire temaet "building" og "populatedPlace".</td>
      <td></td>
    </tr>
    <tr>
      <td>infrastruktur</td>
      <td>Alle grupper som er relevante under hovedgruppe infrastruktur. Tilsvarer Inspire temaet "transportNetwork".</td>
      <td></td>
    </tr>
    <tr>
      <td>offentligAdministrasjon</td>
      <td>Alle grupper som er relevante under hovedgruppe offentlig administrasjon. Tilsvarer Inspire temaet "administrativUnit".</td>
      <td></td>
    </tr>
    <tr>
      <td>kultur</td>
      <td>Alle grupper som er relevante under hovedgruppe Kultur.
Tilsvarer Inspire temaet "protctedSite".</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-navneobjektgruppe"></a>«CodeList» Navneobjektgruppe

**Definisjon:** gruppering av navneobjekttypene i kategorier under hver hovedgruppe.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjektgruppe">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjektgruppe</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>terrengområder</td>
      <td>Samlegruppe for objekttyper som beskriver terrengoverflate over større områder.</td>
      <td></td>
    </tr>
    <tr>
      <td>høyder</td>
      <td>Samlegruppe for objekttyper som er høyere enn andre objektyper i samme område.</td>
      <td></td>
    </tr>
    <tr>
      <td>senkninger</td>
      <td>Samlegruppe for objekttyper som er senket ned i forhold til andre objekttyper i samme område.</td>
      <td></td>
    </tr>
    <tr>
      <td>flater</td>
      <td>Samlegruppe for objekttyper som flate terrengområder.</td>
      <td></td>
    </tr>
    <tr>
      <td>skråninger</td>
      <td>Samlegruppe for objekttyper som beskriver hellende terreng.</td>
      <td></td>
    </tr>
    <tr>
      <td>terrengdetaljer</td>
      <td>Samlegruppe for objekttyper som beskriver spesielle terrengdetaljer.</td>
      <td></td>
    </tr>
    <tr>
      <td>bartFjell</td>
      <td>Samlegruppe for objekttyper som beskriver overflater av bart fjell.</td>
      <td></td>
    </tr>
    <tr>
      <td>løsmasseavsetninger</td>
      <td>Samlegruppe for objekttyper som beskriver avsetting av løse masser.</td>
      <td></td>
    </tr>
    <tr>
      <td>vegetasjon</td>
      <td>Samlegruppe for objekttyper som beskriver vegetasjonen.</td>
      <td></td>
    </tr>
    <tr>
      <td>våtmark</td>
      <td>Samlegruppe for objekttyper som beskriver våt/fuktig mark.</td>
      <td></td>
    </tr>
    <tr>
      <td>dyrkamark</td>
      <td>Samlegruppe for objekttyper som beskriver ulike typer dyrket mark.</td>
      <td></td>
    </tr>
    <tr>
      <td>isOgPermafrost</td>
      <td>Samlegruppe for objekttyper som er fryst.</td>
      <td></td>
    </tr>
    <tr>
      <td>uttakOgDeponi</td>
      <td>Samlegruppe for objekttyper av menneskeskapte uttak eller fyllinger.</td>
      <td></td>
    </tr>
    <tr>
      <td>stilleståendeVann</td>
      <td>Samlegruppe for objekttyper av ferskvann som ser ut til å stå stille.</td>
      <td></td>
    </tr>
    <tr>
      <td>ferskvannskontur</td>
      <td>Samlegruppe for objekttyper som beskriver omrisset av objekter med ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>grunnerIFerskvann</td>
      <td>Samlegruppe for objekttyper under vannflaten som stikker høyere opp enn resten av området, men ikke vesentlig over vannflaten.</td>
      <td></td>
    </tr>
    <tr>
      <td>rennendeVann</td>
      <td>Samlegruppe for objekttyper som beskriver rennenede ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>detaljerIFerskvann</td>
      <td>Samlegruppe for objekttyper som beskriver detaljer i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>farvann</td>
      <td>Samlegruppe for objekttyper som beskriver større områder av sjø.</td>
      <td></td>
    </tr>
    <tr>
      <td>kystkontur</td>
      <td>Samlegruppe for objekttyper som beskriver grensa mellom sjø og tørt land.</td>
      <td></td>
    </tr>
    <tr>
      <td>grunnerISjø</td>
      <td>Samlegruppe for objekttyper under havflaten som stikker høyere opp enn resten av området, men ikke vesentlig over vannflaten.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjøbunn</td>
      <td>Samlegruppe for objekttyper som beskriver sjøbunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>detaljISjø</td>
      <td>Samlegruppe for objekttyper som beskriver detaljer i sjøen.</td>
      <td></td>
    </tr>
    <tr>
      <td>bebyggelsesområder</td>
      <td>Samlegruppe for objekttyper som beskriver områder med flere bygninger samlet innenfor et begrenset område.</td>
      <td></td>
    </tr>
    <tr>
      <td>gardsbebyggelse</td>
      <td>Samlegruppe for objekttyper som beskriver områder med samling av bebyggelse som hovedsakelig er knyttet til landbruk.</td>
      <td></td>
    </tr>
    <tr>
      <td>bolighus</td>
      <td>Samlegruppe for objekttyper som beskriver enkeltbygninger til boligformål som er bebodd midlertidig eller permanent.</td>
      <td></td>
    </tr>
    <tr>
      <td>næring</td>
      <td>Samlegruppe for objekttyper som beskriver enkeltbygninger til næringsformål.</td>
      <td></td>
    </tr>
    <tr>
      <td>institusjoner</td>
      <td>Samlegruppe for objekttyper som beskriver enkeltbygninger eller mindre samlinger av bygninger av institusjonell karakter.</td>
      <td></td>
    </tr>
    <tr>
      <td>fritidsanlegg</td>
      <td>Samlegruppe for objekttyper som beskriver bygningsmessige og naturlige anlegg for rekreasjon og fritidsaktiviteter.</td>
      <td></td>
    </tr>
    <tr>
      <td>veg</td>
      <td>Samlegruppe for objekttyper som beskriver objekter som brukes til ferdsel, både motorisert og til fots.</td>
      <td></td>
    </tr>
    <tr>
      <td>bane</td>
      <td>Samlegruppe for objekttyper som beskriver funksjoner knyttet til skinnegående kjøretøy.</td>
      <td></td>
    </tr>
    <tr>
      <td>luftfart</td>
      <td>Samlegruppe for objekttyper som beskriver anlegg hvor luftfartøy lander og tar av.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjøfart</td>
      <td>Samlegruppe for objekttyper som beskriver anlegg som har tilknytning til sjøfart.</td>
      <td></td>
    </tr>
    <tr>
      <td>navigasjon</td>
      <td>Samlegruppe for objekttyper som beskriver navigasjonshjelpemidler for skipsfart.</td>
      <td></td>
    </tr>
    <tr>
      <td>samferdselsanlegg</td>
      <td>Samlegruppe for objekttyper som beskriver anlegg som brukes i forbindelse med transport, både for kjøretøy og til fots.</td>
      <td></td>
    </tr>
    <tr>
      <td>energi</td>
      <td>Samlegruppe for objekttyper som beskriver anlegg for energi produksjon og transport.</td>
      <td></td>
    </tr>
    <tr>
      <td>kommunikasjon</td>
      <td>Samlegruppe for objekttyper som beskriver anlegg for radiokommunikasjon.</td>
      <td></td>
    </tr>
    <tr>
      <td>administrativeIndelinger</td>
      <td>Samlegruppe for objekttyper som beskriver alle typer administrative inndelinger.</td>
      <td></td>
    </tr>
    <tr>
      <td>verne-OgBruksområder</td>
      <td>Samlegruppe for objekttyper som regulerer vern og bruksrettigheter.</td>
      <td></td>
    </tr>
    <tr>
      <td>kulturminner</td>
      <td>Samlegruppe for objekttyper som er vernet som kulturminner.</td>
      <td></td>
    </tr>
    <tr>
      <td>kulturinstitusjoner</td>
      <td>Samlegruppe for objekttyper som beskriver institusjoner for kulturell aktivitet.</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-navneobjekttype"></a>«CodeList» Navneobjekttype

**Definisjon:** Detaljert klassifisering av hvilke type fenomen stedsnavnet står til.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>true</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjekttype">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0/Navneobjekttype</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>administrativBydel</td>
      <td>Offisielt navn på bydelsforvaltningen i et angitt område.</td>
      <td></td>
    </tr>
    <tr>
      <td>adressenavn</td>
      <td>Offisielt adressenavn, veg-/gatenavn eller områdenavn, jf. § 2 bokstav e i matrikkelforskriften.</td>
      <td></td>
    </tr>
    <tr>
      <td>adressetilleggsnavn</td>
      <td>Et stedsnavn som er en del av den offisielle (veg-)adressen, jf. § 54 i matrikkelforskriften; vanligvis bruksnavn eller sjeldnere bygnings-/institusjonsnavn.</td>
      <td></td>
    </tr>
    <tr>
      <td>allmenning</td>
      <td>Område hvor rettighetene er regulert og fordelt på flere.</td>
      <td></td>
    </tr>
    <tr>
      <td>alpinanlegg</td>
      <td>Anlegg for slalåm, utfor, snøbrett osv.</td>
      <td></td>
    </tr>
    <tr>
      <td>ankringsplass</td>
      <td>Opplagsplass for store fartøy.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenAdministrativInndeling</td>
      <td>Andre administrative inndelinger som ikke tilhører øvrige navneobjekttyper.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenBygningForReligionsutøvelse</td>
      <td>Synagoge, moské, frikirke, menighetshus, kloster, gravkapell, bårehus, krematorium.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenIndustri-OgLagerbygning</td>
      <td>Mindre industri- og produksjonsbedrift eller lager.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenKulturdetalj</td>
      <td>Alle andre typer kulturdetaljer, f.eks. lekeplass, utkikkstårn, fiskeplass, og lignende.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenTerrengdetalj</td>
      <td>Små detaljer som ikke dekkes av andre navneobjekttyper innenfor kategorien.</td>
      <td></td>
    </tr>
    <tr>
      <td>annenVanndetalj</td>
      <td>Andre navngitte forhold i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>badeplass</td>
      <td>Offentlig eller privat badeplass.</td>
      <td></td>
    </tr>
    <tr>
      <td>bakke</td>
      <td>Terrengskråning, særlig om siden av en ås eller haug.</td>
      <td></td>
    </tr>
    <tr>
      <td>bakkeVeg</td>
      <td>Allment kjent bakke på alle typer veger og gater.</td>
      <td></td>
    </tr>
    <tr>
      <td>bakkeISjø</td>
      <td>Skrånende sjøbunn.</td>
      <td></td>
    </tr>
    <tr>
      <td>bakketoppISjø</td>
      <td>Undersjøisk knaus, kolle eller haug.</td>
      <td></td>
    </tr>
    <tr>
      <td>banestrekning</td>
      <td>Jernbanestrekning, tunnelbane eller trikkelinje/-strekning.</td>
      <td></td>
    </tr>
    <tr>
      <td>banke</td>
      <td>Flatt, større undervannsområde.</td>
      <td></td>
    </tr>
    <tr>
      <td>bankeISjø</td>
      <td>Større grunt område i sjøen med dypere vann omkring; fiskegrunn.</td>
      <td></td>
    </tr>
    <tr>
      <td>barnehage</td>
      <td>Offentlig og privat barnehage.</td>
      <td></td>
    </tr>
    <tr>
      <td>bassengISjø</td>
      <td>Vid, undersjøisk dal.</td>
      <td></td>
    </tr>
    <tr>
      <td>bekk</td>
      <td>Rennende vann i naturlig vannvei, vanligvis smalere enn 3 meter.</td>
      <td></td>
    </tr>
    <tr>
      <td>berg</td>
      <td>Markert eller avrunda høyde med stein, steinmasse (med eller uten vegetasjon).</td>
      <td></td>
    </tr>
    <tr>
      <td>bergverk</td>
      <td>Gruve, skjerp og mineraluttak i dagen eller under jorda.</td>
      <td></td>
    </tr>
    <tr>
      <td>boligblokk</td>
      <td>Stort (bolig)hus av mur, betong med over fire boliger som har felles trapp(er) eller heis(er).</td>
      <td></td>
    </tr>
    <tr>
      <td>boligfelt</td>
      <td>Regulert boligområde.</td>
      <td></td>
    </tr>
    <tr>
      <td>bomstasjon</td>
      <td>Større bomanlegg på offentlig veg.</td>
      <td></td>
    </tr>
    <tr>
      <td>borettslag</td>
      <td>Bofellesskap i blokk eller flerbebyggelse.</td>
      <td></td>
    </tr>
    <tr>
      <td>botn</td>
      <td>Innerste del av en dal; rundaktig, bratt dal eller uthulning i fjellet.</td>
      <td></td>
    </tr>
    <tr>
      <td>bru</td>
      <td>Både på veg og jernbane.</td>
      <td></td>
    </tr>
    <tr>
      <td>bruk</td>
      <td>Navn på (landbruks)eiendom med ett eller flere bruksnummer under ett gardsnummer, jf. lov om stadnamn §§ 2 og 8.</td>
      <td></td>
    </tr>
    <tr>
      <td>brygge</td>
      <td>Mindre, fastbygd bryggeanlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>busstopp</td>
      <td>Stoppested for rutegående vegtrafikk.</td>
      <td></td>
    </tr>
    <tr>
      <td>by</td>
      <td>Tettbygd sted som er større og (til dels) innehar viktigere funksjoner enn andre tettbygde steder / tettsteder.</td>
      <td></td>
    </tr>
    <tr>
      <td>bydel</td>
      <td>Kulturmessig del av by.</td>
      <td></td>
    </tr>
    <tr>
      <td>bygdelagBygd</td>
      <td>Stort, uregulert gards- og boligområde.</td>
      <td></td>
    </tr>
    <tr>
      <td>byggForJordbrukFiskeOgFangst</td>
      <td>Til primærnæring, f.eks. naust, uthus, sommerfjøs eller gamme.</td>
      <td></td>
    </tr>
    <tr>
      <td>båe</td>
      <td>Fjell eller stein under vannflaten.</td>
      <td></td>
    </tr>
    <tr>
      <td>båeISjø</td>
      <td>Spiss grunne; blindskjær som sjøen bryter over.</td>
      <td></td>
    </tr>
    <tr>
      <td>båke</td>
      <td>Fast sjømerke. Sprinkelverk bygget i tre eller metall.</td>
      <td></td>
    </tr>
    <tr>
      <td>campingplass</td>
      <td>Alle typer, med/uten campinghytter, campingvogner og telt.</td>
      <td></td>
    </tr>
    <tr>
      <td>dal</td>
      <td>Mellomstor eller liten dal.</td>
      <td></td>
    </tr>
    <tr>
      <td>dalføre</td>
      <td>Stor dal med sidedaler.</td>
      <td></td>
    </tr>
    <tr>
      <td>dam</td>
      <td>Både store reguleringsdammer og små fløtningsdammer. Angi kurve for lange og ett punkt midt på for korte damkroner.</td>
      <td></td>
    </tr>
    <tr>
      <td>delAvInnsjø</td>
      <td>Mindre del av innsjø.</td>
      <td></td>
    </tr>
    <tr>
      <td>eggISjø</td>
      <td>Undersjøisk kant mot havdyp.</td>
      <td></td>
    </tr>
    <tr>
      <td>eid</td>
      <td>Lavt eller smalt parti mellom to vannkanter (elv eller vann).</td>
      <td></td>
    </tr>
    <tr>
      <td>eidISjø</td>
      <td>Landstripe med sjø på begge sider som binder sammen to landområder.</td>
      <td></td>
    </tr>
    <tr>
      <td>eiendom</td>
      <td>Navn på eiendomer som ikke er bruksnavn, ev. felles stedsnavn for flere eiendommer.</td>
      <td></td>
    </tr>
    <tr>
      <td>elv</td>
      <td>Rennende vann i naturlig vannvei, vanligvis bredere enn 3 meter.</td>
      <td></td>
    </tr>
    <tr>
      <td>elvemel</td>
      <td>Bratt sand-/grusskråning langs elv eller vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>elvesving</td>
      <td>Naturlig sving i elv eller bekk.</td>
      <td></td>
    </tr>
    <tr>
      <td>eneboligMindreBoligbygg</td>
      <td>Navn på mindre eiendom for fast bosetting. Hovedsakelig eiendom hvor eier kan bestemme skrivemåten (jf. § 8 i lov om stadnamn og § 54 i matrikkelforskriften). Kan også omfatte eget navn på bygg, eller våningshus/gardsbruk som ikke er gitt eget matrikkelnummer.</td>
      <td></td>
    </tr>
    <tr>
      <td>eng</td>
      <td>Kultivert slåtte-/gressmark.</td>
      <td></td>
    </tr>
    <tr>
      <td>fabrikk</td>
      <td>Større industrivirksomhet.</td>
      <td></td>
    </tr>
    <tr>
      <td>farledSkipslei</td>
      <td>Allment kjent seglingslei/farvannsområde med dybdeforhold passende for skip av en viss størrelse.</td>
      <td></td>
    </tr>
    <tr>
      <td>fengsel</td>
      <td>Bygning der arresterte eller dømte personer soner straff.</td>
      <td></td>
    </tr>
    <tr>
      <td>ferjekai</td>
      <td>Ferjekai i fast regulert ferjesamband.</td>
      <td></td>
    </tr>
    <tr>
      <td>ferjestrekning</td>
      <td>Ferjesamband som inngår i områdets samferdselsnett.</td>
      <td></td>
    </tr>
    <tr>
      <td>fiskeplassISjø</td>
      <td>Navngitt fiskested; fiskemed.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjell</td>
      <td>Høyereliggende område (over tregrensa) med stein og sva og lite vegetasjon som reiser seg over landskapet omkring (med høye berg og nuter).</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellIDagen</td>
      <td>Lite/ingen vegetasjon; sva, svaberg. Erstattes av sva.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellheis</td>
      <td>Gondolbane og trallebane for frakt av folk.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellkant</td>
      <td>Aksel, skulder, nese og bryn.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellkjedeISjø</td>
      <td>Lengre, sammenhengende undersjøisk fjellformasjon.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellområde</td>
      <td>Større område med fjell og fjellandskap.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellside</td>
      <td>Åpent, skrånende terreng i fjellet.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjelltoppISjø</td>
      <td>Undersjøisk fjelltopp.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjord</td>
      <td>Arm av havet inn i fastlandet.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjordmunning</td>
      <td>Område ytterst i en fjord.</td>
      <td></td>
    </tr>
    <tr>
      <td>flyplass</td>
      <td>Offentlig godkjent, avgrenset område med start- og landingsplass for fly.</td>
      <td></td>
    </tr>
    <tr>
      <td>fløtningsanlegg</td>
      <td>Kunstig fløtningsanlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>fonn</td>
      <td>Liten snø- eller isflate som vanligvis ikke smelter om sommeren.</td>
      <td></td>
    </tr>
    <tr>
      <td>fornøyelsespark</td>
      <td>Store, regulerte anlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>forretningsbygg</td>
      <td>Bygning for kontor-, salg- og servicevirksomhet.</td>
      <td></td>
    </tr>
    <tr>
      <td>forsamlingshusKulturhus</td>
      <td>Teater, kino, samfunnshus, grendehus o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>forskningsstasjon</td>
      <td>Bemannet forskningsstasjon eller meteorologisk stasjon med bygningsmasse.</td>
      <td></td>
    </tr>
    <tr>
      <td>foss</td>
      <td>Vann i tilnærmet fritt fall.</td>
      <td></td>
    </tr>
    <tr>
      <td>fritidsbolig</td>
      <td>Eget navn på hytter og hus som ikke er ment for fast bosetting.</td>
      <td></td>
    </tr>
    <tr>
      <td>fylke</td>
      <td>Offisielt navn.</td>
      <td></td>
    </tr>
    <tr>
      <td>fyllplass</td>
      <td>Plass for deponering av masse som stein, jord og søppel.</td>
      <td></td>
    </tr>
    <tr>
      <td>fyrlykt</td>
      <td>Linse og lyskilde anbrakt i hus eller liknende. Ikke flytende.</td>
      <td></td>
    </tr>
    <tr>
      <td>fyrstasjon</td>
      <td>Automatisk og ubemannet. Et fast anlegg hvor linse og lyskilde er anbrakt i hus, tårn eller spesielt bygg. Ikke flytende.</td>
      <td></td>
    </tr>
    <tr>
      <td>gammelBosettingsplass</td>
      <td>Nedlagt bruk, seter, boplass hvor bygningen(e) er borte eller bare tuftene er tilbake.</td>
      <td></td>
    </tr>
    <tr>
      <td>garasjeHangarbygg</td>
      <td>Trikkestall, bussgarasje, flyhangar eller lokomotivstall.</td>
      <td></td>
    </tr>
    <tr>
      <td>gard</td>
      <td>Felles navn for et helt gardsnummer (jf. § 8 i lov om stadnamn).</td>
      <td></td>
    </tr>
    <tr>
      <td>gass-OljefeltISjø</td>
      <td>Navngitt gass- eller oljefelt i havet.</td>
      <td></td>
    </tr>
    <tr>
      <td>geologiskStruktur</td>
      <td>Navngitt struktur/formasjon i berggrunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>gjerde</td>
      <td>Oppsatt stengsel, vern, skille mellom jordstykker, eiendommer eller beiteområder.</td>
      <td></td>
    </tr>
    <tr>
      <td>gravplass</td>
      <td>Alle typer gravlunder, gravplasser.</td>
      <td></td>
    </tr>
    <tr>
      <td>grend</td>
      <td>Mindre uregulert gards- og boligområde.</td>
      <td></td>
    </tr>
    <tr>
      <td>grensemerke</td>
      <td>Offisielt grensemerke: Varde, tre, stein, bolt, kors o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>grind</td>
      <td>Port i gjerde.</td>
      <td></td>
    </tr>
    <tr>
      <td>grotte</td>
      <td>Naturlig fjellgrotte.</td>
      <td></td>
    </tr>
    <tr>
      <td>grunne</td>
      <td>Lite område under vann som hever seg fra området rundt.</td>
      <td></td>
    </tr>
    <tr>
      <td>grunneISjø</td>
      <td>Markant forhøyning av havbunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>grunnkrets</td>
      <td>Offisielt navn på grunnkrets.</td>
      <td></td>
    </tr>
    <tr>
      <td>gruppeAvTjern</td>
      <td>To eller flere små tjern.</td>
      <td></td>
    </tr>
    <tr>
      <td>gruppeAvVann</td>
      <td>To eller flere vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>grustakSteinbrudd</td>
      <td>Uttaksplass/-område for sand, grus, pukk, skifer eller stein.</td>
      <td></td>
    </tr>
    <tr>
      <td>grøft</td>
      <td>Rennende vann i oppgravd vannvei, f.eks. dreneringsgrøft i myr.</td>
      <td></td>
    </tr>
    <tr>
      <td>halvøy</td>
      <td>Større nes i ferskvann med smalt eid mot fastland.</td>
      <td></td>
    </tr>
    <tr>
      <td>halvøyISjø</td>
      <td>Større nes med smalt eid mot fastland.</td>
      <td></td>
    </tr>
    <tr>
      <td>haug</td>
      <td>Liten, markant forhøynet terrengform.</td>
      <td></td>
    </tr>
    <tr>
      <td>havdyp</td>
      <td>Stort, dypt område i havet.</td>
      <td></td>
    </tr>
    <tr>
      <td>havn</td>
      <td>Sted der fartøy laster, losser eller søker ly for vær og sjø.</td>
      <td></td>
    </tr>
    <tr>
      <td>havnehage</td>
      <td>Inngjerdet beitemark.</td>
      <td></td>
    </tr>
    <tr>
      <td>havområde</td>
      <td>Del av et hav.</td>
      <td></td>
    </tr>
    <tr>
      <td>havstrøm</td>
      <td>Kontinuerlig bevegelse av vann (i havet) på grunn av klimatiske forhold eller tidevann.</td>
      <td></td>
    </tr>
    <tr>
      <td>hei</td>
      <td>Berglendt, høyere beliggende område med beitemark.</td>
      <td></td>
    </tr>
    <tr>
      <td>heller</td>
      <td>Utoverhengende bergvegg eller berghule.</td>
      <td></td>
    </tr>
    <tr>
      <td>helseinstitusjon</td>
      <td>Aldershjem, rekreasjonshjem og lignende.</td>
      <td></td>
    </tr>
    <tr>
      <td>historiskBosetting</td>
      <td>Ubebodd eller forlatt bosetting med bestående bygningsmasse eller ruiner.</td>
      <td></td>
    </tr>
    <tr>
      <td>holdeplass</td>
      <td>Ubetjent stoppested for jernbane, tunnelbane og/eller trikk.</td>
      <td></td>
    </tr>
    <tr>
      <td>holme</td>
      <td>Liten øy i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>holmeISjø</td>
      <td>Liten øy.</td>
      <td></td>
    </tr>
    <tr>
      <td>holmegruppeISjø</td>
      <td>To eller flere små øyer.</td>
      <td></td>
    </tr>
    <tr>
      <td>hotell</td>
      <td>Større, offentlig godkjent overnattingssted.</td>
      <td></td>
    </tr>
    <tr>
      <td>hylle</td>
      <td>Flatt, tilnærmet vannrett område i fjellside.</td>
      <td></td>
    </tr>
    <tr>
      <td>hylleISjø</td>
      <td>Undersjøisk benk; klippeavsats, kant, fremspring, avsats.</td>
      <td></td>
    </tr>
    <tr>
      <td>hyttefelt</td>
      <td>Offentlig eller privat hyttefelt. Regulert område med høy utnyttelsesgrad.</td>
      <td></td>
    </tr>
    <tr>
      <td>høl</td>
      <td>Dyp elvebunn under foss eller etter et stryk.</td>
      <td></td>
    </tr>
    <tr>
      <td>høyde</td>
      <td>Høyereliggende terrengform, mindre omfattende enn ås og større enn haug.</td>
      <td></td>
    </tr>
    <tr>
      <td>idrettsanlegg</td>
      <td>Alle typer utendørsanlegg for idrett.</td>
      <td></td>
    </tr>
    <tr>
      <td>idrettshall</td>
      <td>Alle typer innendørsanlegg, f.eks. ishall, svømmehall, idrettshall og ridehall.</td>
      <td></td>
    </tr>
    <tr>
      <td>industriområde</td>
      <td>Større, sammenhengende område til industri- og næringsformål.</td>
      <td></td>
    </tr>
    <tr>
      <td>innsjø</td>
      <td>Stort vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>isbre</td>
      <td>Større sammenhengende snø- eller isområde som ikke smelter i løpet av sommeren.</td>
      <td></td>
    </tr>
    <tr>
      <td>iskuppel</td>
      <td>Konveks ismasse av en viss tykkelse i større bre eller innlandsis.</td>
      <td></td>
    </tr>
    <tr>
      <td>jernstang</td>
      <td>Fast sjømerke av typen jernstang eller jernsøyle.</td>
      <td></td>
    </tr>
    <tr>
      <td>jorde</td>
      <td>Kultivert dyrkningsmark.</td>
      <td></td>
    </tr>
    <tr>
      <td>juv</td>
      <td>Kløftlignende dal eller canyon.</td>
      <td></td>
    </tr>
    <tr>
      <td>kabel</td>
      <td>Alle typer kabler i sjø eller i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>kai</td>
      <td>Større, fastbygd bryggeanlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>kanal</td>
      <td>Kunstig eller naturlig vannvei eller gjennomseiling.</td>
      <td></td>
    </tr>
    <tr>
      <td>kilde</td>
      <td>Oppkomme, olle, kildeutspring, osv.</td>
      <td></td>
    </tr>
    <tr>
      <td>kirke</td>
      <td>Kirke, kapell, arbeidskirke o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>klakkISjø</td>
      <td>Fjellknatt på sjøbunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>klopp</td>
      <td>Liten gangbru av stokker og/eller stein over bekker og elver, i myr eller i fjæra.</td>
      <td></td>
    </tr>
    <tr>
      <td>kommune</td>
      <td>Offisielt navn.</td>
      <td></td>
    </tr>
    <tr>
      <td>kontinentalsokkel</td>
      <td>Område med grunt hav rundt kontinentene. Ofte brukt om et lands økonomiske interessesone til sjøs.</td>
      <td></td>
    </tr>
    <tr>
      <td>korallrev</td>
      <td>Rev som er dannet av koraller.</td>
      <td></td>
    </tr>
    <tr>
      <td>kraftgateRørgate</td>
      <td>Store tilførselsrør for kraftanlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>kraftledning</td>
      <td>Stor strømoverføringsledning.</td>
      <td></td>
    </tr>
    <tr>
      <td>kraftstasjon</td>
      <td>Alle typer / alle størrelser til energiproduksjon (f.eks. el. og varme).</td>
      <td></td>
    </tr>
    <tr>
      <td>krater</td>
      <td>Skål- eller traktformet senkning i jordoverflaten forårsaket av vulkansk aktivitet eller av meteorittnedslag.</td>
      <td></td>
    </tr>
    <tr>
      <td>landingsplass</td>
      <td>Landingsplass for privatfly.</td>
      <td></td>
    </tr>
    <tr>
      <td>landskapsområde</td>
      <td>Område der drag i landskapet, naturforhold, arealbruk og bosetting er samlende og skiller seg fra tilgrensende områder.</td>
      <td></td>
    </tr>
    <tr>
      <td>lanterne</td>
      <td>En innretning hvor linsen med eller uten beskyttelsesglass utgjør en del av den bærende del av konstruksjonen. Ikke flytende.</td>
      <td></td>
    </tr>
    <tr>
      <td>li</td>
      <td>Skrånende terreng.</td>
      <td></td>
    </tr>
    <tr>
      <td>lon</td>
      <td>Utbuktning i elv eller bekk der vannet renner stille.</td>
      <td></td>
    </tr>
    <tr>
      <td>lysbøye</td>
      <td>Flytende innretning for farvannsmerking med en lanterne som lyskilde.</td>
      <td></td>
    </tr>
    <tr>
      <td>matrikkeladressenavn</td>
      <td>Et stedsnavn som inngår i den offiselle adressen ved matrikkeladresser, jf. § 55 tredje ledd i matrikkelforskriften.</td>
      <td></td>
    </tr>
    <tr>
      <td>melkeplass</td>
      <td>Seterplass uten hus (ev. med enkelt skur) brukt til melking av husdyr.</td>
      <td></td>
    </tr>
    <tr>
      <td>militærtByggAnlegg</td>
      <td>Militærleir.</td>
      <td></td>
    </tr>
    <tr>
      <td>mo</td>
      <td>Større, flatt landområde (ofte skogkledd).</td>
      <td></td>
    </tr>
    <tr>
      <td>molo</td>
      <td>Fast byggverk, utstikkende voll i sjøen.</td>
      <td></td>
    </tr>
    <tr>
      <td>moreneryggISjø</td>
      <td>Marin israndavsetning.</td>
      <td></td>
    </tr>
    <tr>
      <td>museumGalleriBibliotek</td>
      <td>Alle typer museum, galleri og bibliotek.</td>
      <td></td>
    </tr>
    <tr>
      <td>myr</td>
      <td>Alle typer fra åpen gressmyr til våt moldjord dekket med kjerr.</td>
      <td></td>
    </tr>
    <tr>
      <td>nasjon</td>
      <td>Offisielt navn på selvstendig stat eller land.</td>
      <td></td>
    </tr>
    <tr>
      <td>navnegard</td>
      <td>Opprinnelig navn fra før garden ble oppdelt i gards- og bruksenheter. Navnegardens utbredelse kan omfatte flere enn ett gardsnummer.</td>
      <td></td>
    </tr>
    <tr>
      <td>nes</td>
      <td>Landområde stikkende ut i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>nesISjø</td>
      <td>Landområde stikkende ut i sjø.</td>
      <td></td>
    </tr>
    <tr>
      <td>nesVedElver</td>
      <td>Landet mellom to møtende elver.</td>
      <td></td>
    </tr>
    <tr>
      <td>offersted</td>
      <td>Alle typer offersted.</td>
      <td></td>
    </tr>
    <tr>
      <td>oljeinstallasjon</td>
      <td>Stasjonær olje- og gassinstallasjon (fast eller flytende).</td>
      <td></td>
    </tr>
    <tr>
      <td>oppdrettsanlegg</td>
      <td>Anlegg for foring og stell av husdyr til de kan settes i produksjon eller slaktes; oppforing av fisk (og andre sjødyr) i fangenskap.</td>
      <td></td>
    </tr>
    <tr>
      <td>os</td>
      <td>Innløp eller utløp av elv eller bekk i innsjø/vann/tjern eller sjø (saltvann).</td>
      <td></td>
    </tr>
    <tr>
      <td>overett</td>
      <td>To sjømerker, med eller uten lys, som, når de peiles på linje, viser kurs for gjennomseiling.</td>
      <td></td>
    </tr>
    <tr>
      <td>park</td>
      <td>Kultivert grøntområde i by/tettsted.</td>
      <td></td>
    </tr>
    <tr>
      <td>parkeringsplass</td>
      <td>Tomt (eller bygning) for parkering av biler.</td>
      <td></td>
    </tr>
    <tr>
      <td>pensjonat</td>
      <td>Mindre, offentlig godkjent overnattingssted.</td>
      <td></td>
    </tr>
    <tr>
      <td>platåISjø</td>
      <td>Stor, flat forhøyning som skiller seg fra havbunnen omkring.</td>
      <td></td>
    </tr>
    <tr>
      <td>poststed</td>
      <td>Offisielt poststed/postnummerområde.</td>
      <td></td>
    </tr>
    <tr>
      <td>pytt</td>
      <td>Lite vannhull (mindre enn tjern).</td>
      <td></td>
    </tr>
    <tr>
      <td>rasISjø</td>
      <td>Undersjøisk rasområde med stein, jord, sand eller leire.</td>
      <td></td>
    </tr>
    <tr>
      <td>rasteplass</td>
      <td>Rasteplass definert og lagt til rette av Statens vegvesen eller annen offentlig myndighet.</td>
      <td></td>
    </tr>
    <tr>
      <td>renneKløftISjø</td>
      <td>Undersjøisk dal, kanal, senkning, ravine, fure, spor, rille o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>revISjø</td>
      <td>Grunne, banke av stein/fjell (som strekker seg ut fra en kyst).</td>
      <td></td>
    </tr>
    <tr>
      <td>rygg</td>
      <td>Langstrakt terrengform.</td>
      <td></td>
    </tr>
    <tr>
      <td>ryggISjø</td>
      <td>Undersjøisk ås, åskam eller fjellrygg.</td>
      <td></td>
    </tr>
    <tr>
      <td>rørledning</td>
      <td>Alle typer rørledninger: Olje, gass, vann o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>rådhus</td>
      <td>Administrasjonssenteret i den administrative enheten, f.eks. stat, fylke, kommune.</td>
      <td></td>
    </tr>
    <tr>
      <td>sadelISjø</td>
      <td>Undersjøisk skar mellom to høyere topper/rygger.</td>
      <td></td>
    </tr>
    <tr>
      <td>sand</td>
      <td>Finkornede avsetninger (sand og/eller grus).</td>
      <td></td>
    </tr>
    <tr>
      <td>senkning</td>
      <td>Flat forsenkning, dalsenkning.</td>
      <td></td>
    </tr>
    <tr>
      <td>serveringssted</td>
      <td>Serveringssted uten overnatting.</td>
      <td></td>
    </tr>
    <tr>
      <td>seterStøl</td>
      <td>Enklere landbruksbebyggelse med hus. Kan ha periodisk fast bosetting, vanligvis sommerstid.</td>
      <td></td>
    </tr>
    <tr>
      <td>setervoll</td>
      <td>Ryddet, gressbevokst område på seter uten hus.</td>
      <td></td>
    </tr>
    <tr>
      <td>severdighet</td>
      <td>Minnesmerke, arkeologiske funn o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjødetalj</td>
      <td>Detalj som ikke dekkes av andre sjø-navneobjekttyper.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjøvarde</td>
      <td>Varde av stein eller betong primært for navigering til sjøs.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjøstykke</td>
      <td>Stykke av sjøen utanfor land, vanligvis innaskjærs eller i kystnære farvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>skar</td>
      <td>Markant senkning i fjell eller berg.</td>
      <td></td>
    </tr>
    <tr>
      <td>skiheis</td>
      <td>Skitrekk og stolheis i skianlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>skjær</td>
      <td>Fjell eller stein i vannflaten.</td>
      <td></td>
    </tr>
    <tr>
      <td>skjærISjø</td>
      <td>Bergrunn nær eller rett over vannflaten.</td>
      <td></td>
    </tr>
    <tr>
      <td>skog</td>
      <td>Alle typer fra stor barskog til og med vierkratt i Finnmark.</td>
      <td></td>
    </tr>
    <tr>
      <td>skogholt</td>
      <td>Mindre samling av trær.</td>
      <td></td>
    </tr>
    <tr>
      <td>skogområde</td>
      <td>Større område med skog og mark.</td>
      <td></td>
    </tr>
    <tr>
      <td>skole</td>
      <td>Offentlig og privat skole.</td>
      <td></td>
    </tr>
    <tr>
      <td>skolekrets</td>
      <td>Skolekrets definert av kommunen.</td>
      <td></td>
    </tr>
    <tr>
      <td>skredområde</td>
      <td>Område der det går eller har gått skred.</td>
      <td></td>
    </tr>
    <tr>
      <td>skytebane</td>
      <td>Bane for øvelse el. konkurranse i skyting.</td>
      <td></td>
    </tr>
    <tr>
      <td>skytefelt</td>
      <td>Militært sprengingsfelt, bombe- og skytefelt, både på land og sjø.</td>
      <td></td>
    </tr>
    <tr>
      <td>slette</td>
      <td>Åpent, flatt område.</td>
      <td></td>
    </tr>
    <tr>
      <td>sluse</td>
      <td>Kunstig løfteanretning for båter i vassdrag.</td>
      <td></td>
    </tr>
    <tr>
      <td>småbåthavn</td>
      <td>Regulert havneanlegg for småbåter.</td>
      <td></td>
    </tr>
    <tr>
      <td>sokkelISjø</td>
      <td>Undersjøisk fjellfot.</td>
      <td></td>
    </tr>
    <tr>
      <td>sokn</td>
      <td>Kirkesokn i Den norske kirke.</td>
      <td></td>
    </tr>
    <tr>
      <td>soneinndelingTilHavs</td>
      <td>Fiskerisone, havrettssone og lignende.</td>
      <td></td>
    </tr>
    <tr>
      <td>stake</td>
      <td>Flytende sjømerke. Ofte kalt bøyestake, stakebøye, kubbestake.</td>
      <td></td>
    </tr>
    <tr>
      <td>stasjon</td>
      <td>Stoppested for jernbane, tunnelbane og/eller trikk. Som regel betjent.</td>
      <td></td>
    </tr>
    <tr>
      <td>statistiskTettsted</td>
      <td>Tettsted etter Statistisk sentralbyrås klassifisering som brukes for å lage statistikk over befolkning og tettsteder.</td>
      <td></td>
    </tr>
    <tr>
      <td>stein</td>
      <td>Frittliggende steinblokk.</td>
      <td></td>
    </tr>
    <tr>
      <td>sti</td>
      <td>Stistrekning, råk, slepe (gammel drifteveg), reindriftsveg.</td>
      <td></td>
    </tr>
    <tr>
      <td>strand</td>
      <td>Sand-, grus- eller steindekket område i vannkanten ved elv eller vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>strandISjø</td>
      <td>Sand-, grus- eller steindekket område i sjøkanten.</td>
      <td></td>
    </tr>
    <tr>
      <td>stryk</td>
      <td>Del av elv, bekk der vannet går i stryk (og skiller seg tydelig fra resten av elva/bekken).</td>
      <td></td>
    </tr>
    <tr>
      <td>stup</td>
      <td>Loddrett, svært bratt berg.</td>
      <td></td>
    </tr>
    <tr>
      <td>stø</td>
      <td>Båtplass i vannkanten uten naust.</td>
      <td></td>
    </tr>
    <tr>
      <td>sund</td>
      <td>Innsnevret område i vann eller vassdrag.</td>
      <td></td>
    </tr>
    <tr>
      <td>sundISjø</td>
      <td>Innsnevret område mellom øyer eller fastland.</td>
      <td></td>
    </tr>
    <tr>
      <td>sykehus</td>
      <td>Offentlig og privat sykehus.</td>
      <td></td>
    </tr>
    <tr>
      <td>søkk</td>
      <td>Mindre markant, begrenset fordypning.</td>
      <td></td>
    </tr>
    <tr>
      <td>søkkISjø</td>
      <td>Stor eller liten grop på sjøbunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>taubane</td>
      <td>Heis til frakt av gods/høy, ikke persontrafikk.</td>
      <td></td>
    </tr>
    <tr>
      <td>tettbebyggelse</td>
      <td>Bebygd område uten sentrumskarakter.</td>
      <td></td>
    </tr>
    <tr>
      <td>tettsted</td>
      <td>Mindre, bymessig bebygd område med sentrumskarakter.</td>
      <td></td>
    </tr>
    <tr>
      <td>tettsteddel</td>
      <td>Kulturmessig del av tettsted.</td>
      <td></td>
    </tr>
    <tr>
      <td>tjern</td>
      <td>Lite vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>topp</td>
      <td>Tind, markant topp på fjell, berg, ås osv.</td>
      <td></td>
    </tr>
    <tr>
      <td>torg</td>
      <td>Stor, åpen plass i en by.</td>
      <td></td>
    </tr>
    <tr>
      <td>torvtak</td>
      <td>Sted for uttak av myrtorv, brenntorv eller veksttorv.</td>
      <td></td>
    </tr>
    <tr>
      <td>traktorveg</td>
      <td>Driftsveg anlagt for traktorbruk. Ikke fremkommelig med vanlig personbil.</td>
      <td></td>
    </tr>
    <tr>
      <td>tunnel</td>
      <td>Vanlig tunnel på veg. Bruk kurve/linje for tunnelstrekning eller punkt for navn på tunnelåpning.</td>
      <td></td>
    </tr>
    <tr>
      <td>turisthytte</td>
      <td>Overnattingssted utenfor tettbygd område.</td>
      <td></td>
    </tr>
    <tr>
      <td>tV-Radio-EllerMobiltelefontårn</td>
      <td>Alle typer bakkebasert telekommunikasjon.</td>
      <td></td>
    </tr>
    <tr>
      <td>tømmervelte</td>
      <td>Midlertidig lagringsplass for tømmer.</td>
      <td></td>
    </tr>
    <tr>
      <td>undersjøiskVegg</td>
      <td>Fjellside i havet.</td>
      <td></td>
    </tr>
    <tr>
      <td>universitetHøgskole</td>
      <td>Offentlig og privat høgskole og universitet.</td>
      <td></td>
    </tr>
    <tr>
      <td>ur</td>
      <td>Steinområde, steinrøys eller steinur.</td>
      <td></td>
    </tr>
    <tr>
      <td>utmark</td>
      <td>Beitemark i skog og mark vekk fra garden (og innmarka).</td>
      <td></td>
    </tr>
    <tr>
      <td>utsiktspunkt</td>
      <td>Både fra tårn og på bakken.</td>
      <td></td>
    </tr>
    <tr>
      <td>utstikker</td>
      <td>Flytende bryggeanlegg.</td>
      <td></td>
    </tr>
    <tr>
      <td>vad</td>
      <td>Vadested, vanligvis der en stistrekning krysser elv, bekk eller vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>vaktstasjonBeredsskapsbygning</td>
      <td>Bygning for politi/brann/los/toll/ambulanse/fly- og skipsovervåkning.</td>
      <td></td>
    </tr>
    <tr>
      <td>valgkrets</td>
      <td>Valgkrets definert av kommunen.</td>
      <td></td>
    </tr>
    <tr>
      <td>vann</td>
      <td>Middels stort vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>varde</td>
      <td>(Som oftest) oppstablet stein som skal markere sti, grensemerke, trigonometrisk punkt o.l.</td>
      <td></td>
    </tr>
    <tr>
      <td>vegbom</td>
      <td>Mindre bomanlegg på privat veg.</td>
      <td></td>
    </tr>
    <tr>
      <td>vegkryss</td>
      <td>Allment kjent vegkryss i alle typer veger og gater.</td>
      <td></td>
    </tr>
    <tr>
      <td>vegstrekning</td>
      <td>Navn på vegstrekning som ikke nødvendigvis har et formelt vedtak, og ikke er det samme som adressenavnet. Det kan være f.eks. turistrekninger og ringveger rundt en by.</td>
      <td></td>
    </tr>
    <tr>
      <td>vegsving</td>
      <td>Allment kjent sving på alle typer veger og gater.</td>
      <td></td>
    </tr>
    <tr>
      <td>verneområde</td>
      <td>Et område med spesiell natur- og/eller kulturverdi som er formelt vedtatt vernet etter offentlig regelverk. Alle typer, både på sjø og land.</td>
      <td></td>
    </tr>
    <tr>
      <td>vidde</td>
      <td>Høyereliggende (fjell)område med lite høydevariasjoner innenfor området, som regel over tregrensa.</td>
      <td></td>
    </tr>
    <tr>
      <td>vik</td>
      <td>Kil eller bukt i vann eller vassdrag.</td>
      <td></td>
    </tr>
    <tr>
      <td>vikISjø</td>
      <td>Kil, bukt.</td>
      <td></td>
    </tr>
    <tr>
      <td>vulkanISjø</td>
      <td>Vulkan eller slamvulkan på havbunnen.</td>
      <td></td>
    </tr>
    <tr>
      <td>vågISjø</td>
      <td>Fjordarm, større vik.</td>
      <td></td>
    </tr>
    <tr>
      <td>øy</td>
      <td>Tørt landområde i ferskvann atskilt fra fastlandet.</td>
      <td></td>
    </tr>
    <tr>
      <td>øyISjø</td>
      <td>Tørt landområde atskilt fra fastlandet.</td>
      <td></td>
    </tr>
    <tr>
      <td>øygruppe</td>
      <td>To eller flere øyer i ferskvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>øygruppeISjø</td>
      <td>To eller flere øyer.</td>
      <td></td>
    </tr>
    <tr>
      <td>øyr</td>
      <td>Sand-/grusområde i elvemunning, elvedelta både mot innsjø/vann og saltvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>ås</td>
      <td>Langstrakt høydedrag.</td>
      <td></td>
    </tr>
    <tr>
      <td>eiendomsteig</td>
      <td>Et stykke eiendom som ikke henger sammen med resten av eiendommen.</td>
      <td></td>
    </tr>
    <tr>
      <td>våtmarksområde</td>
      <td>Sump, område med våtmark.</td>
      <td></td>
    </tr>
    <tr>
      <td>busstasjon</td>
      <td>Større busstopp der flere busslinjer kobles, knutepunkt.</td>
      <td></td>
    </tr>
    <tr>
      <td>vannstandsmåler</td>
      <td>Innretning for å måle vann eller tidevannsnivå.</td>
      <td></td>
    </tr>
    <tr>
      <td>friluftsområde</td>
      <td>Et område som er avsatt for friluftsliv.</td>
      <td></td>
    </tr>
    <tr>
      <td>sjømerkeMedIndirekteBelysning</td>
      <td>Sjømerke med indirekte belyst struktur, skilt, fundament eller plasseringspunkt.</td>
      <td></td>
    </tr>
    <tr>
      <td>reinbeitedistrikt</td>
      <td>Reinbeitedistrikt.</td>
      <td></td>
    </tr>
    <tr>
      <td>boinstitusjon</td>
      <td>Dekker både tilrettelagte boliger og asyl-/flykningmottak.</td>
      <td></td>
    </tr>
    <tr>
      <td>egg</td>
      <td>Skarp fjellegg der det går bratt ned på begge sider.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellvegg</td>
      <td>Tilnærmet loddrett vegg i fjellside.</td>
      <td></td>
    </tr>
    <tr>
      <td>delAvVann</td>
      <td>Mindre del av vann.</td>
      <td></td>
    </tr>
    <tr>
      <td>jernbanebru</td>
      <td>Bru for jernbane.</td>
      <td></td>
    </tr>
    <tr>
      <td>jernbanetunnel</td>
      <td>Tunnel for jernbane. Bruk kurve/linje for tunnelstrekning på jerbane eller punkt for navn på tunnelåpning/kort tunnel.</td>
      <td></td>
    </tr>
    <tr>
      <td>helikopterlandingsplass</td>
      <td>Landingsplass for helikopter.</td>
      <td></td>
    </tr>
    <tr>
      <td>kulturMessehall</td>
      <td>Stort anlegg/hall til flerbruk - varemesse, konserter, idrettsarrangement.</td>
      <td></td>
    </tr>
    <tr>
      <td>overbygg</td>
      <td>Overbygg over veg eller jernbane for beskyttelse mot ras, for å gjemme f.eks. veg i bebyggelseområde eller som viltoverganger.</td>
      <td></td>
    </tr>
    <tr>
      <td>mindreBrukonstruksjon</td>
      <td>Korte bruer eller kulverter hvor navnet er av liten allmenn interresse eller av teknisk art.</td>
      <td></td>
    </tr>
    <tr>
      <td>stølsSetereiendom</td>
      <td>Matrikulert seternavn eller enkeltseter innenfor et seterområde</td>
      <td></td>
    </tr>
    <tr>
      <td>tuft</td>
      <td>Sted som har hatt bebyggelse, men som antagelig ikke har vært bebodd. Ruin.</td>
      <td></td>
    </tr>
    <tr>
      <td>vannverk</td>
      <td>Inntak for drikkevann/vanningsvann.</td>
      <td></td>
    </tr>
    <tr>
      <td>hammar</td>
      <td>Utoverhengende berg.</td>
      <td></td>
    </tr>
    <tr>
      <td>fjellovergang</td>
      <td>Vegstrekning som krysser værutsatt fjellparti.</td>
      <td></td>
    </tr>
    <tr>
      <td>sva</td>
      <td>Bart, avrundet glatt fjell</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-sortering1kode"></a>«CodeList» Sortering1Kode

**Definisjon:** Alle store bokstaver fra og med A til og med N.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/Sortering1Kode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/Sortering1Kode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>A</td>
      <td>Minst viktige objekt tegnes til slutt vanligvis i små målestokker.</td>
      <td></td>
    </tr>
    <tr>
      <td>B</td>
      <td>Viktigere enn A</td>
      <td></td>
    </tr>
    <tr>
      <td>C</td>
      <td>Viktigere enn A og B</td>
      <td></td>
    </tr>
    <tr>
      <td>D</td>
      <td>Viktigere enn C men mindre viktig enn E</td>
      <td></td>
    </tr>
    <tr>
      <td>E</td>
      <td>Viktigere enn D men mindre viktig enn F</td>
      <td></td>
    </tr>
    <tr>
      <td>F</td>
      <td>Viktigere enn E men mindre viktig enn G</td>
      <td></td>
    </tr>
    <tr>
      <td>G</td>
      <td>Viktigere enn F men mindre viktig enn H</td>
      <td></td>
    </tr>
    <tr>
      <td>H</td>
      <td>Viktigere enn G men mindre viktig enn I</td>
      <td></td>
    </tr>
    <tr>
      <td>I</td>
      <td>Viktigere enn H men mindre viktig enn J</td>
      <td></td>
    </tr>
    <tr>
      <td>J</td>
      <td>Viktigere enn I men mindre viktig enn K</td>
      <td></td>
    </tr>
    <tr>
      <td>K</td>
      <td>Viktigere enn J men mindre viktig enn L</td>
      <td></td>
    </tr>
    <tr>
      <td>L</td>
      <td>Viktigere enn K men mindre viktig enn M</td>
      <td></td>
    </tr>
    <tr>
      <td>M</td>
      <td>Viktigere enn L men mindre viktig enn N</td>
      <td></td>
    </tr>
    <tr>
      <td>N</td>
      <td>Høyest prioritet, de viktigste navnene, tegnes vanligvis fra små målestokker.</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-sortering2kode"></a>«CodeList» Sortering2Kode

**Definisjon:** Tall fra og med 01 til og med 99.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/Sortering2Kode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/Sortering2Kode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
      <td>Minst viktig av de navnene med samme sorteringsbokstav.</td>
      <td>01</td>
    </tr>
    <tr>
      <td></td>
      <td>Viktigere enn de med 01 under samme bokstav.</td>
      <td>02</td>
    </tr>
    <tr>
      <td></td>
      <td>Viktigere enn de med 02 under samme bokstav.</td>
      <td>03</td>
    </tr>
    <tr>
      <td></td>
      <td>Viktigere enn de med lavere nummer under samme bokstav.</td>
      <td>04</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>05</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>06</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>07</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>08</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>09</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>10</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>11</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>12</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>13</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>14</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>15</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>16</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>17</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>18</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>19</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>20</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>21</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>22</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>23</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>24</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>25</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>26</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>27</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>28</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>29</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>30</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>31</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>32</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>33</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>34</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>35</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>36</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>37</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>38</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>39</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>40</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>41</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>42</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>43</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>44</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>45</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>46</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>47</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>48</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>49</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>50</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>51</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>52</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>53</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>54</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>55</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>56</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>57</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>58</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>59</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>60</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>61</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>62</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>63</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>64</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>65</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>66</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>67</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>68</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>69</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>70</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>71</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>72</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>73</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>74</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>75</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>76</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>77</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>78</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>79</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>80</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>81</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>82</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>83</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>84</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>85</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>86</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>87</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>88</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>89</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>90</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>91</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>92</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>93</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>94</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>95</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>96</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>97</td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td>98</td>
    </tr>
    <tr>
      <td></td>
      <td>Viktigtse navn av de med samme sorteringsbokstav, har høyest prioritet.</td>
      <td>99</td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-stedstatuskode"></a>«CodeList» StedstatusKode

**Definisjon:** Kodeliste som gir status til Sted. Om det er f.eks. aktiv, relikt eller planlagt.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/StedstatusKode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/StedstatusKode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>aktiv</td>
      <td>Objektet eksisterer.</td>
      <td></td>
    </tr>
    <tr>
      <td>relikt</td>
      <td>Objektet eksisterer ikke lengre, men stedsnavnet kan fortsatt være i bruk.</td>
      <td></td>
    </tr>
    <tr>
      <td>planlagt</td>
      <td>Objektet eksisterer ikke ennå, men er planlagt. Denne statusen vil være aktuell ved for eksempel registrering av adressenavn for planlagte veier.</td>
      <td></td>
    </tr>
    <tr>
      <td>feilført</td>
      <td>Objektet er feilaktig registrert.</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-språkprioriteringkode"></a>«CodeList» SpråkprioriteringKode

**Definisjon:** Kodeliste som angir visningsrekkefølgen til stedsnavn på forskjellig språk.

&lt;b&gt;Det er de første fem verdiene i kodene (de norske språkene) som varierer mellom kodene&lt;/b&gt;, ellers er det lik (alfabetisk i forhold til ISO-kodeverdien) rekkefølge på språkene som ikke er aktuelle for behandling etter lov om stadnamn.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/SpråkprioriteringKode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/SpråkprioriteringKode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>lulesamisk-nordsamisk-sørsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, lulesamisk område der nordsamisk kan forekomme.</td>
      <td></td>
    </tr>
    <tr>
      <td>lulesamisk-sørsamisk-nordsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, lulesamisk område der sørsamisk kan forekomme.</td>
      <td></td>
    </tr>
    <tr>
      <td>nordsamisk-lulesamisk-sørsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, nordsamisk område.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-lulesamisk-nordsamisk-sørsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, lulesamisk område der nordsamisk kan forekomme sammen med lulesamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-lulesamisk-sørsamisk-nordsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, lulesamisk område der sørdsamisk kan forekomme sammen med lulesamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-nordsamisk-lulesamisk-sørsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, nordsamisk område der lulesamisk kan forekomme sammen med nordsamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-sørsamisk-lulesamisk-nordsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, sørsamisk område der lulesamisk kan forekomme sammen med sørsamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>sørsamisk-lulesamisk-nordsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, sørdsamisk område.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-nordsamisk-lulesamisk-sørsamisk-norsk</td>
      <td>Brukes i samisk forvaltningsområde, dersom kvensk skal prioriteres over samisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-norsk-nordsamisk-lulesamisk-sørsamisk</td>
      <td>Brukes i norsk forvaltningsområde dersom kvensk skal prioriteres over norsk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-nordsamisk-skoltesamisk-lulesamisk-sørsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, nordsamisk område der skoltesamisk kan forekomme sammen med nordsamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-skoltesamisk-nordsamisk-lulesamisk-sørsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, skoltesamisk område der nordsamisk kan forekomme sammen med skoltesamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-lulesamisk-nordsamisk-skoltesamisk-sørsamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, lulesamisk område der nordsamisk kan forekomme sammen med lulesamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-lulesamisk-sørsamisk-nordsamisk-skoltesamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, lulesamisk område der sørsamisk kan forekomme sammen med lulesamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>norsk-sørsamisk-lulesamisk-nordsamisk-skoltesamisk-kvensk</td>
      <td>Brukes i norsk forvaltingsområde, sørsamisk område der lulesamisk kan forekomme sammen med sørsamisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>nordsamisk-skoltesamisk-lulesamisk-sørsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, nordsamisk område.</td>
      <td></td>
    </tr>
    <tr>
      <td>skoltesamisk-nordsamisk-lulesamisk-sørsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, skoltesamisk område.</td>
      <td></td>
    </tr>
    <tr>
      <td>lulesamisk-nordsamisk-skoltesamisk-sørsamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, lulesamisk område der nordsamisk kan forekomme.</td>
      <td></td>
    </tr>
    <tr>
      <td>lulesamisk-sørsamisk-nordsamisk-skoltesamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, lulesamisk område der sørsamisk kan forekomme.</td>
      <td></td>
    </tr>
    <tr>
      <td>sørsamisk-lulesamisk-nordsamisk-skoltesamisk-norsk-kvensk</td>
      <td>Brukes i samisk forvaltningsområde, sørsamisk område.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-nordsamisk-skoltesamisk-lulesamisk-sørsamisk-norsk</td>
      <td>Brukes i samisk forvaltningsområde, nordsamisk område, dersom kvensk skal prioriteres over samisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-skoltesamisk-nordsamisk-lulesamisk-sørsamisk-norsk</td>
      <td>Brukes i samisk forvaltningsområde, skoltesamisk område, dersom kvensk skal prioriteres over samisk.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-norsk-nordsamisk-skoltesamisk-lulesamisk-sørsamisk</td>
      <td>Brukes i norsk forvaltningsområde dersom kvensk skal prioriteres over norsk, men nordsamisk kan forekomme.</td>
      <td></td>
    </tr>
    <tr>
      <td>kvensk-norsk-skoltesamisk-nordsamisk-lulesamisk-sørsamisk</td>
      <td>Brukes i norsk forvaltningsområde dersom kvensk skal prioriteres over norsk, men skoltesamisk kan forekomme.</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-tilleggsopplysningtypekode"></a>«CodeList» TilleggsopplysningtypeKode

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/TilleggsopplysningtypeKode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/TilleggsopplysningtypeKode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>språkfaglig</td>
      <td>Informasjon av språkfaglig karakter som tileggsopplysning til stedsnavnet.</td>
      <td></td>
    </tr>
    <tr>
      <td>historisk</td>
      <td>Informasjom om historien til stedsnavnet eller stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>lokalitet</td>
      <td>Tilleggsinformasjon om lokalitetenen som har betydning for stedsnavn.</td>
      <td></td>
    </tr>
    <tr>
      <td>matrikkelnummerFraSSR</td>
      <td>Denne er brukt under konverteringen fra gammelt SSR for å overføre gnr/bnr/fnr for et utvalg av navneenhetene, basert på navneobjekttyper</td>
      <td></td>
    </tr>
    <tr>
      <td>adressinformasjonFraSSR</td>
      <td>Denne er brukt under konverteringen fra gammelt SSR for å overføre gateident fra SSR for navneenheter med navne(objekttype)kode "Adressenavn".</td>
      <td></td>
    </tr>
    <tr>
      <td>navnesak</td>
      <td>Navnesak</td>
      <td></td>
    </tr>
    <tr>
      <td>merknadFraSSR</td>
      <td>Merknadstekst konvertert fra SSR. Det er ikke mulig å registrere denne typen tilleggsopplysning i ny SSR.</td>
      <td></td>
    </tr>
    <tr>
      <td>adressekode</td>
      <td>Felt for å registrere adressekoden fra matrikkelen.</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-vedtaksmyndighetkode"></a>«CodeList» VedtaksmyndighetKode

**Definisjon:** Liste over vedtaksmyndigheter for skrivemåten.

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">asDictionary</th>
      <td>false</td>
    </tr>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/VedtaksmyndighetKode">http://skjema.geonorge.no/SOSI/produktspesifikasjon/Stedsnavn/5.0Utkast/2016-03-30/VedtaksmyndighetKode</a></td>
    </tr>
  </tbody>
</table>

Koder

<table class="code-list-table">
  <thead>
    <tr>
      <th>Kodenavn:</th>
      <th>Definisjon:</th>
      <th>Kodeverdi:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Avinor</td>
      <td>Avinor er vedtaksmyndighet for stedsnavnet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Bispedømmerådet</td>
      <td>Bispedømmerådet er vedtaksmyndighet for stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Direktoratet_for_naturforvaltning</td>
      <td>Direktoratet for naturforvaltning var vedtaksmyndighet for stedsnavnet før lovens endring i 2006.</td>
      <td></td>
    </tr>
    <tr>
      <td>Fylkeskommune</td>
      <td>Fylkeskommunen er vedtaksmyndighet for stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Jernbaneverket</td>
      <td>Jernbaneverket var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Klagenemnda_for_stedsnavnsaker</td>
      <td>Klagenemnda for stedsnavnsaker</td>
      <td></td>
    </tr>
    <tr>
      <td>Kommune</td>
      <td>Kommunen er vedtaksmyndighet for stedsnavnet på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Kongen_i_statsråd</td>
      <td>Kongen i statsråd har vedtatt stedsnavnet på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Kystverket</td>
      <td>Kystverket var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Norges_geologiske_undersøkelse</td>
      <td>Norges geologiske undersøkelse var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Polarinstituttet</td>
      <td>Polarinstituttet er vedtaksmyndighet for stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Posten_Norge_AS</td>
      <td>Posten var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Privat_eier</td>
      <td>Privat eier kan selv bestemme stedsnavnet på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Reindriftsforvaltningen</td>
      <td>Reindriftsforvaltningen var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Statens_kartverk</td>
      <td>Kartverket er vedtaksmyndighet for stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Statens_vegvesen</td>
      <td>Statens vegvesen var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>Statskog</td>
      <td>Statskog var vedtaksmyndighet når stedsnavnet ble vedtatt. Etter lovendring i 2006 har Kartverket vedtaksmyndighet på stedsnavn på stedet.</td>
      <td></td>
    </tr>
    <tr>
      <td>utenforLovensVirkeområde</td>
      <td>Utenfor lovens virkeområde</td>
      <td></td>
    </tr>
  </tbody>
</table>

#### <a id="kodeliste-kommunenummer"></a>«CodeList» Kommunenummer

Profilparametre i tagged values

<table class="feature-attribute-table">
  <colgroup>
    <col style="width: 35%;" />
    <col style="width: 65%;" />
  </colgroup>
  <tbody>
    <tr>
      <th scope="row">codeList</th>
      <td><a href="http://skjema.geonorge.no/SOSI/kodeliste/AdmEnheter/Kommunenummer">http://skjema.geonorge.no/SOSI/kodeliste/AdmEnheter/Kommunenummer</a></td>
    </tr>
  </tbody>
</table>
