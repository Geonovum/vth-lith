# Mapping van aanlevering Inspectieview

## Naamgevingsconventies

- Een klasse schrijven we met UpperCamelCase
- Een attribuutnaam schrijven we met lowerCamelCase

## Mapping van cim-vth-flo naar lith

| cim-vth-flo        | lith              |
| ------------------ | ----------------- |
| NATUURLIJK PERSOON | NatuurlijkPersoon |
| BETROKKENE         | Betrokkene        |

## Welke CSV bestanden mappen op welke klasse

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
| certificaat.csv            | wordt niet gemapt |
| certificaatoudnieuw.csv    | wordt niet gemapt |


## NatuurlijkPersoon

| cim-vth-flo         | lith                |
| ------------------- | ------------------- |
| Burgerservicenummer | burgerservicenummer |
| Naam                | naam                |
| Geslachtsaanduiding | geslachtsaanduiding |
| Overlijdensdatum    | overlijdensdatum    |

Vertaling van de kenmerken in `natuurlijkpersoon.csv` naar lith:

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