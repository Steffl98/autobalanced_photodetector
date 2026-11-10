# LT3439 PSU - Datenblaetter

Stand: 2026-10-28. Originaldateien; PDF-Inhalt durch Textextraktion geprueft.
Keine KiCad-Symbol- oder Footprintbibliotheken enthalten.

| Bauteil / Funktion | Datei | Downloadquelle |
|---|---|---|
| LT3439, Gegentakttreiber | ADI_LT3439.pdf | https://www.ic-components.com/files/52/LT3439EFE-TRPBF.pdf |
| LT3045, positiver LDO | ADI_LT3045.pdf | https://www.farnell.com/datasheets/2163219.pdf |
| LT3094, negativer LDO, Rev. 0 | ADI_LT3094_Rev0.pdf | https://media.digikey.com/pdf/Data%20Sheets/Analog%20Devices%20PDFs/LT3094_Rev0_9-5-18.pdf |
| STPS1L60A, D1-D4, Rev. 11 | ST_STPS1L60A.pdf | https://www.farnell.com/datasheets/2816025.pdf |
| VLS5030EX-330M-D, L1/L2 | TDK_VLS5030EX_D.pdf | https://my.avnet.com/wcm/connect/a1c4ee68-9eaa-4934-bb06-fece42b68f64/TDK-VLS5030EX-D-Series-EN-Datasheet.pdf?CACHE=NONE&CVID=oMx2l.U&ContentCache=NONE&MOD=AJPERES |
| UCL1V470MCL1GS, C3/C5 | Nichicon_UCL.pdf | https://www.nichicon.com/getmedia/d1cc9ca9-f3b4-4677-b34b-68b6b2b1caef/e-ucl.pdf |
| CC0603FRNPO9BN681, CT | YAGEO_CC0603FRNPO9BN681.pdf | https://yageogroup.com/download/specsheet/CC0603FRNPO9BN681 |
| MAAST32MSB7226MPNA01, COUT: je 2 parallel pro LDO, 4 insgesamt; 22 uF, 25 V, X7R, +/-20%, 1210 | MAAST32MSB7226MPNA01.pdf | Vom Benutzer abgelegte Hersteller-Kennlinien; https://ds.yuden.co.jp/TYCOMPAS/or/detail?pn=MAAST32MSB7226MPNA01 |
| KGM31AR71E475KU, C1; Serien-Datenblatt | KYOCERA_AVX_KGM_X7R.pdf | https://datasheets.kyocera-avx.com/KGM_X7R.pdf |
| CPF0603F16K9C1, RT/RSL; Serien-Datenblatt | TE_CPF_series.pdf | https://docs.rs-online.com/3ae0/0900766b80cecff9.pdf?download=1 |
| RT0603BRD07120KL, RSET beider LDOs; 120 kohm, +/-0.1%, +/-25 ppm/K, 0.1 W, 0603 | YAGEO_RT0603BRD07120KL.pdf | https://www.yageogroup.com/component-documentation/download/specsheet/RT0603BRD07120KL |
| CR1206AFX-1002EAS, RS (R8 im Architekturplan); 10 kohm, +/-1%, 0.25 W, 1206 | Bourns_CR_A_AS.pdf | https://www.bourns.com/docs/product-datasheets/cr-a-as.pdf?sfvrsn=5f5578f6_21 |

RS: Mindestlast-/Entladewiderstand zwischen positiver und negativer Rohspannung hinter dem Gleichrichter, nicht nach Masse. Bei +/-16 V: 32 V ueber 10 kohm, ca. 0.102 W. KiCad: Device:R, Resistor_SMD:R_1206_3216Metric. Ausgewaehlt am 2026-10-28; CRG1206F1K0/10 (1 kohm) wurde nicht ausgewaehlt.

## Grenzen

- Einige Hersteller-Downloads waren blockiert. Die Spiegelkopien sind teilweise aelter als die aktuellen Herstellerrevisionen. Vor Layoutfreigabe Pinout, Gehaeuse, Grenzwerte und Errata mit der aktuellen Revision vergleichen.
- Aktuelle Herstellerquellen: [LT3439](https://www.analog.com/media/en/technical-documentation/data-sheets/lt3439.pdf), [LT3045](https://www.analog.com/media/en/technical-documentation/data-sheets/LT3045.pdf), [LT3094](https://www.analog.com/media/en/technical-documentation/data-sheets/lt3094.pdf), [STPS1L60](https://www.st.com/resource/en/datasheet/stps1l60.pdf).
- CTX02-16076: kein eigenstaendiges Datenblatt gefunden. Die 12-V-Referenzschaltung im LT3439-Datenblatt nennt diesen Trafo, ersetzt aber keine verbindliche Anschluss- und Gehaeusezeichnung. Diese vor Festlegung des Footprints bei Eaton anfordern.
- C4/C6, LDO-Ausgangs- und SET-Kondensatoren sowie Anschluesse haben noch keine festgelegten Teilenummern.
