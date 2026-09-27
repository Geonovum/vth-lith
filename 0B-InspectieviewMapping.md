# Mapping van aanlevering Inspectieview

Data van [[BaselineCSV]] wordt vertaald volgens de volgende mappings:


## CSV bestanden in BaselineCSV

De volgende bestanden worden op de volgende klasses in lith gemapped:

| csv bestand                | mapping           |
| -------------------------- | ----------------- |
| inspectieobject.csv        |                   |
| vestiging.csv              |                   |
| binnenschip.csv            |                   |
| omgevingsobject.csv        |                   |
| natuurlijkpersoon.csv      | NatuurlijkPersoon |
| niet-natuurlijkpersoon.csv |                   |
| signaal.csv                |                   |
| inspectie.csv              |                   |
| bevinding.csv              |                   |
| overtreding.csv            |                   |
| inspectiedocument.csv      |                   |
| toestemming.csv            |                   |
| activiteituitvoering.csv   |                   |
| afvalmelding.csv           |                   |
| bodemmelding.csv           |                   |
| vuurwerkmelding.csv        |                   |
| astbestmelding.csv         |                   |
| notitie.csv                |                   |
| betrokkenpartij.csv        |                   |
| betrokkenovertreders.csv   |                   |
| certificaat.csv            | geen mapping     |
| certificaatoudnieuw.csv    | geen mapping      |
|                            |                   |


## Vertaling van `natuurlijkpersoon.csv`

Beslispunten:
- voornaam, voorletters, tussenvoegsels, achternaam zouden met een transformatie op naam gemapped kunnen worden

Bijzonderheden:
- wanneer `wa_landcode` = `NL` dan adresBinnenland anders adresBuitenland.


| natuurlijkpersoon.csv | lith                                 |
| --------------------- | ------------------------------------ |
| bsn                   | burgerservicenummer                  |
| voornaam              |                                      |
| voorletters           |                                      |
| tussenvoegsel         |                                      |
| achternaam            |                                      |
| geboortedatum         |                                      |
| geslachtsaanduiding   | geslachtsaanduiding                  |
| geboorteplaats        |                                      |
| geboorteland_code     |                                      |
| nationaliteit         |                                      |
| documentnummer_id     |                                      |
| wa_straatnaam         | adresBinnenland.straatnaam           |
| wa_huisnummer         | adresBinnenland.huisnummer           |
| wa_huisnr_toevoeging  | adresBinnenland.huisnummertoevoeging |
| wa_postcode_nl        | adresBinnenland.postcode             |
| wa_plaatsnaam         | adresBinnenland.naamWoonplaats       |
| wa_gemeente           | adresBinnenland.gemeente             |
| wa_landcode           | adresBuitenland.land                 |
| wa_adresaanduiding    | adresBinnenland.adresaanduiding      |
|                       |                                      |