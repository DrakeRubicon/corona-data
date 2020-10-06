# Saved Responses from Zeit.de API

## GraphQL Queries

### Germany whole

```graphql
POST https://interactive-api.zeit.de/v1/graphql?Content-Type=application/graphql
Host: Zeit.de
Content-Type: application/graphql

query InitialQuery {
	germany: intensivregister_csvimport_deutschland_historisch {
		date: day
		covid19: faelle_covid_aktuell
		bedsFree: betten_frei
		bedsOccupied: betten_belegt
		clinicCount: anzahl_standorte
		}
	kreise: intensivregister_csvimport_kreise_aktuell {
		date: day
		covid19: faelle_covid_aktuell
		bedsFree: betten_frei
		bedsOccupied: betten_belegt
		clinicCount: anzahl_standorte
		ags
		}
	clinics: intensivregister_ampel_klinik_aktuell {
	id
	name: bezeichnung
	ags
	date: meldezeitpunkt
	highcare: statushighcare
	lowcare: statuslowcare
	ecmo: statusecmo
	ort
	}
}
```

### Landkreise

```graphql
POST https://interactive-api.zeit.de/v1/graphql?Content-Type=application/graphql
Host: Zeit.de
Content-Type: application/graphql

query KreisDetail($ags: String!) {
    days: intensivregister_csvimport_kreise_historisch(where: {ags: {_eq: $ags}}) {
        date: day
        covid19: faelle_covid_aktuell
        bedsFree: betten_frei
        bedsOccupied: betten_belegt
        clinicCount: anzahl_standorte
        }
    }
```

Use AGS for AGS-Variable i.e.:

```graphql
{
	"ags" : "14612"
}
```

| AGS	| Landkreis						   |
|:-----:| -------------------------------- |
| 14511 | Chemnitz						   |
| 14612 | Dresden						   |
| 14713 | Leipzig						   |
| 14521 | Erzgebirgskreis				   |
| 14522 | Mittelsachsen					   |
| 14523 | Vogtlandkreis					   |
| 14524 | Zwickau						   |
| 14625 | Bautzen						   |
| 14626 | Görlitz						   |
| 14627 | Meißen						   |
| 14628 | Sächsische Schweiz-Osterzgebirge |
| 14729 | Landkreis Leipzig				   |
| 14730 | Nordsachsen 					   |