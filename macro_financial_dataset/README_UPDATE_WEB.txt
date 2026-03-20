MACRO-FINANCIAL DATASET (QUARTERLY SINCE 1950)

Reference:
  Camous, A., Monnet, E. and Puy, D. (2025),
  "World Cycles Revisited: Diverging Trends in Prices and Quantities",
  Banque de France Working Paper No. 592, September 2025.
  https://www.banque-france.fr/en/publications-and-statistics/publications/world-cycles-revisited-diverging-trends-prices-and-quantities

Please cite the above paper when using this dataset.


UPDATE — Extension to 2025Q3/Q4 (March 2026)

The dataset has been extended from 2019Q4 to 2025Q3/Q4 using data from the
IMF SDMX API (api.imf.org) as primary source, supplemented by OECD data
via FRED (fred.stlouisfed.org) for government bond yields and share prices.
Historical data (1950–2019) are unchanged.

Primary Source — IMF SDMX API:

  Variable          IMF Dataset             Indicator
  Consumer prices   CPI (v5.0.0)            CPI._T.IX.Q
  Real GDP          QNEA (v7.0.0)          B1GQ.Q.SA.XDC.Q
  Domestic credit   MFS_DC (v8.0.0)        ODCORP_A_ACO_PS..Q
  Share prices      MFS_FMP (v3.0.0)       EQTS / PA_IX / Q
  Bond yields       MFS_IR (v8.0.1)        S13BOND_RT_PT_A_PT.Q

Secondary Source — OECD via FRED (fills gaps where IMF stopped reporting):

  Variable          FRED series pattern     Countries
  Bond yields       IRLTLT01{CC}Q156N       12 countries (post-2017 IMF gap)
  Share prices      SPASTT01{CC}Q661N       15 countries (post-2017 IMF gap)

Extended Coverage (2020+):

  Consumer prices    47 of 48 countries (missing: TWN)
  Real GDP           34 of 37 countries
  Domestic credit    40 of 46 countries
  Bond yields        17 of 18 countries  ← improved from 5 (IMF only)
  Share prices       23 of 26 countries  ← improved from 8 (IMF only)

Bond Yield Coverage by Source (17 countries):
  IMF:  DNK ITA NZL USA ZAF
  FRED: AUS BEL CHE DEU FRA GBR IRL JPN NLD NOR PRT SWE
  (CAN unavailable — FRED uses a different benchmark bond, incompatible)

Share Price Coverage by Source (23 countries):
  IMF:  CHL DNK ESP ITA MEX NZL PER PHL
  FRED: AUT BEL CAN CHE DEU FIN FRA GBR IND IRL ISR JPN NOR SWE USA
  (PER and PHL not on FRED; covered by IMF)

Known Remaining Gaps:

Bond yields: CAN bond yield unavailable for 2020+ (FRED uses a different
Canadian benchmark instrument, causing a systematic +0.45pp offset — not
suitable for seamless extension).

Share prices: PER and PHL covered by IMF only (non-OECD members, not on FRED).

All other gaps (credit, GDP, prices) are unchanged from the IMF-only version.
