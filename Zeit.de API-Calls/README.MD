# Saved Responses from Zeit.de API

## GraphQL Queries

### Germany whole

```http
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