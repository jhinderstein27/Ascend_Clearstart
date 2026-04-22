# Ascend Healthcare — FQHC Account Scoring

**Purpose:** Rank the FQHCs/Look-Alikes represented in our enriched NACHC + NatCon contact base, so Ascend's outbound team can work warmest accounts first.

**Source data:**
- 1,527 U.S. FQHCs/LALs (HRSA site roster, pulled 2026-04-22)
- 1,888 unique enriched contacts (NACHC Workforce attendees + NatCon 2026 attendees, Apollo-matched)
- 258 of those contacts (14%) confirmed at actual FQHCs, covering 141 unique organizations

**Output:** [`FQHC_scored.csv`](./FQHC_scored.csv) — 141 ranked accounts

---

## The scoring framework

Each FQHC gets a score out of 12 across 7 factors. All factors use free public data (HRSA) + the conference attendee match we built.

| # | Factor | Points | Rationale |
|---|---|---|---|
| 1 | **State priority** | Core (AZ/MD/NC/TX/UT) = 3<br>Adjacent = 2<br>Other = 1 | Ascend builds state density before crossing borders; core states have existing clinical licensing + Medicaid contracts |
| 2 | **Size (delivery sites)** | 2–10 sites = 2<br>1 or 11–20 = 1<br>21+ or 0 = 0 | Sweet spot for encounter-based economics. Too small can't support onboarding cost; too large often has in-house BH infrastructure |
| 3 | **FQHC (not Look-Alike)** | Yes = 1 | LALs are smaller/newer, less mature revenue cycle |
| 4 | **501(c)(3) corporate entity** | Yes = 1 | Filters out govt/tribal operators, who often have separate contracting workflows |
| 5 | **Multiple warm contacts** | 3+ = 2<br>2 = 1 | Density of conference attendees = the org invests in BH topics; gives us multiple intro paths |
| 6 | **Exec contact on our list** | Yes = 1 | CEO/CMO/VP/Director on our list = direct decision-maker path |
| 7 | **BH-titled contact on our list** | Yes = 1 | Behavioral-health-specific role = champion or budget owner for the exact service Ascend sells |

### Tier cutoffs

| Tier | Score | Action | Count |
|---|---|---|---|
| 🔥 **A** | 8–12 | Direct exec outreach from Ascend VP Growth / CEO. Custom 1:1 sequence. | 14 |
| 🎯 **B** | 5–7 | SDR-led outbound, 6-touch multi-channel (email + LinkedIn). | 99 |
| ❄️ **C** | <5 | Low-touch nurture. Re-score on trigger event. | 28 |

---

## Tier A — Top 14 accounts

These are the immediate outreach targets. Each has strong state fit, workable size, real FQHC status, and multiple warm connections in our contact base.

| Rank | Score | State | FQHC | Sites | Contacts | Execs | BH titles | Source |
|---|---|---|---|---|---|---|---|---|
| 1 | 11 | TX | GULF COAST HEALTH CENTER, INC | 10 | 6 | 6 | 3 | NatCon |
| 2 | 10 | NC | TRIAD ADULT & PEDIATRIC MEDICINE, INC. | 6 | 2 | 1 | 1 | NatCon |
| 3 | 9 | VA | HORIZON HEALTH SERVICES INC | 6 | 9 | 9 | 0 | NatCon |
| 4 | 9 | NV | COMMUNITY HEALTH ALLIANCE | 10 | 6 | 6 | 0 | NACHC+NatCon |
| 5 | 8 | IA | EASTERN IOWA HEALTH CENTER | 6 | 4 | 2 | 0 | NACHC |
| 6 | 8 | GA | FAMILY HEALTH CENTERS OF GEORGIA, INC., THE | 14 | 4 | 3 | 0 | NACHC |
| 7 | 8 | PR | MOROVIS COMMUNITY HEALTH CENTER INC | 7 | 4 | 1 | 0 | NACHC |
| 8 | 8 | CA | BEHAVIORAL HEALTH SERVICES, INC. | 9 | 4 | 3 | 0 | NatCon |
| 9 | 8 | MI | DETROIT COMMUNITY HEALTH CONNECTION | 7 | 3 | 3 | 0 | NACHC |
| 10 | 8 | MI | WESTERN WAYNE FAMILY HEALTH CENTERS | 6 | 3 | 2 | 0 | NACHC |
| 11 | 8 | CA | SOUTHLAND INTEGRATED SERVICES INC | 2 | 3 | 1 | 0 | NatCon |
| 12 | 8 | MI | GENESEE HEALTH SYSTEM | 5 | 3 | 2 | 1 | NatCon |
| 13 | 8 | LA | RAPIDES PRIMARY HEALTH CARE CENTER INCORPORATE… | 5 | 2 | 2 | 0 | NACHC |
| 14 | 8 | NC | ROANOKE CHOWAN COMMUNITY HEALTH CENTERS, INC. | 10 | 1 | 1 | 0 | NACHC |


## Tier B — 99 accounts (SDR cadence)

Sound candidates with two or more positive signals. Ranked by score and contact density — work the top half first.

| Rank | Score | State | FQHC | Sites | Contacts | Execs | BH titles | Source |
|---|---|---|---|---|---|---|---|---|
| 1 | 7 | NY | LIBERTY RESOURCES INC | 3 | 6 | 6 | 1 | NatCon |
| 2 | 7 | MS | G.A. CARMICHAEL FAMILY HEALTH CENTER, INC | 17 | 5 | 4 | 0 | NACHC |
| 3 | 7 | IN | Jane Pauley Community Health Center, Inc. | 22 | 5 | 5 | 2 | NACHC+NatCon |
| 4 | 7 | MS | NORTH MS PRIMARY HEALTH CARE INC | 19 | 4 | 1 | 0 | NACHC |
| 5 | 7 | AL | RURAL HEALTH MEDICAL PROGRAM INC | 11 | 4 | 2 | 0 | NACHC |
| 6 | 7 | CA | WATTS HEALTHCARE CORP | 3 | 3 | 0 | 0 | NACHC |
| 7 | 7 | OH | COMMUNITY ACTION COMMITTEE OF PIKE COUNTY | 12 | 3 | 3 | 0 | NACHC |
| 8 | 7 | NC | Mountain Area Health Education Center, INC. | 61 | 3 | 2 | 1 | NatCon |
| 9 | 7 | NY | SUN RIVER HEALTH, INC. | 85 | 3 | 3 | 1 | NatCon |
| 10 | 7 | TN | CHRIST COMMUNITY HEALTH SERVICES INC | 15 | 2 | 1 | 0 | NACHC |
| 11 | 7 | PA | DELAWARE VALLEY COMMUNITY HEALTH, INC. | 11 | 2 | 2 | 0 | NACHC |
| 12 | 7 | TX | EL CENTRO DEL BARRIO | 26 | 2 | 2 | 0 | NACHC |
| 13 | 7 | OK | GREAT SALT PLAINS HEALTH CENTER | 11 | 2 | 1 | 0 | NACHC |
| 14 | 7 | MO | HCC NETWORK | 10 | 2 | 2 | 0 | NACHC |
| 15 | 7 | MA | MASSACHUSETTS LEAGUE OF COMMUNITY HEALTH CENTE… | 6 | 2 | 2 | 0 | NACHC |
| 16 | 7 | LA | SWLA CENTER FOR HEALTH SERVICES | 6 | 2 | 0 | 0 | NACHC |
| 17 | 7 | VI | FREDERIKSTED HEALTH CARE INC | 5 | 2 | 2 | 0 | NACHC |
| 18 | 7 | NM | PRESBYTERIAN MEDICAL SERVICES | 76 | 2 | 1 | 2 | NatCon |
| 19 | 7 | WA | INTERNATIONAL COMMUNITY HEALTH SERVICES | 12 | 2 | 2 | 1 | NatCon |
| 20 | 7 | AZ | VALLE DEL SOL, INC | 36 | 2 | 2 | 0 | NatCon |
| 21 | 7 | NM | LA CLINICA DE FAMILIA INC | 28 | 2 | 1 | 1 | NatCon |
| 22 | 7 | NC | APPALACHIAN MOUNTAIN COMMUNITY HEALTH CENTERS | 12 | 1 | 1 | 0 | NACHC |
| 23 | 7 | GA | CHRIST COMMUNITY HEALTH SERVICES AUGUSTA, INC | 5 | 1 | 1 | 0 | NACHC |
| 24 | 7 | PA | FAMILY FIRST HEALTH CORPORATION | 10 | 1 | 1 | 0 | NACHC |
| 25 | 7 | PA | HAMILTON HEALTH CENTER INC | 6 | 1 | 1 | 0 | NACHC |
| 26 | 7 | NC | PIEDMONT HEALTH SERVICES INC | 18 | 1 | 1 | 0 | NACHC |
| 27 | 7 | NC | ROBESON HEALTH CARE CORPORATION | 12 | 1 | 1 | 0 | NACHC |
| 28 | 7 | OK | SHORTGRASS COMMUNITY HEALTH CENTER INC | 4 | 1 | 1 | 0 | NACHC |
| 29 | 7 | GA | PRIMARY CARE OF SOUTHWEST GEORGIA, INC. | 9 | 1 | 1 | 0 | NACHC |
| 30 | 7 | IL | CENTRAL COUNTIES HEALTH CENTERS | 5 | 1 | 1 | 1 | NatCon |
| 31 | 7 | PA | PUBLIC HEALTH MANAGEMENT CORP | 15 | 1 | 1 | 1 | NatCon |
| 32 | 7 | NY | UNION COMMUNITY HEALTH CENTER, INC. | 7 | 1 | 1 | 1 | NatCon |
| 33 | 6 | CA | WELLSPACE HEALTH | 33 | 7 | 5 | 0 | NatCon |
| 34 | 6 | AL | SOUTHEAST ALABAMA RURAL HEALTH ASSOCIATE | 14 | 5 | 5 | 0 | NACHC |
| 35 | 6 | WA | PENINSULA COMMUNITY HEALTH SERVICES | 42 | 4 | 4 | 0 | NACHC |
| 36 | 6 | NY | MORRIS HEIGHTS HEALTH CENTER INC | 34 | 4 | 3 | 0 | NACHC |
| 37 | 6 | CA | CLINICA SIERRA VISTA | 39 | 3 | 2 | 0 | NACHC |
| 38 | 6 | AL | QUALITY OF LIFE HEALTH SERVICES, INC. | 25 | 3 | 3 | 0 | NACHC |
| 39 | 6 | CT | WHEELER CLINIC INC | 26 | 3 | 3 | 0 | NACHC+NatCon |
| 40 | 6 | MO | COMPASS HEALTH, INC | 71 | 3 | 2 | 0 | NatCon |
| 41 | 6 | RI | THE PROVIDENCE COMMUNITY HEALTH CENTERS, INC. | 14 | 2 | 2 | 0 | NACHC |
| 42 | 6 | WV | RAINELLE MEDICAL CENTER | 32 | 2 | 2 | 1 | NatCon |
| 43 | 6 | OH | MERIDIAN HEALTHCARE | 4 | 2 | 1 | 1 | NatCon |
| 44 | 6 | OH | FAMILY HEALTH CARE OF NORTHWEST OHIO INC | 1 | 2 | 2 | 0 | NatCon |
| 45 | 6 | NJ | RUTGERS THE STATE UNIVERSITY OF NEW JERSEY | 3 | 2 | 0 | 0 | NatCon |
| 46 | 6 | AR | 1ST CHOICE HEALTHCARE, INC. | 9 | 1 | 1 | 0 | NACHC |
| 47 | 6 | AZ | ADELANTE HEALTHCARE INC | 15 | 1 | 0 | 0 | NACHC |
| 48 | 6 | NJ | CAMCARE HEALTH CORPORATION | 9 | 1 | 1 | 0 | NACHC |
| 49 | 6 | LA | HIV/AIDS ALLIANCE FOR REGION TWO (HAART), INC. | 18 | 1 | 1 | 0 | NACHC |
| 50 | 6 | OR | NORTHWEST HUMAN SERVICES, INC. | 8 | 1 | 1 | 0 | NACHC |
| 51 | 6 | IL | CHICAGO FAMILY HEALTH CENTER INC | 7 | 1 | 1 | 0 | NACHC |
| 52 | 6 | MI | FAMILY HEALTH CENTER INC | 7 | 1 | 1 | 0 | NACHC |
| 53 | 6 | MA | HARVARD STREET NEIGHBORHOOD HEALTH CENTER INC | 3 | 1 | 1 | 0 | NACHC |
| 54 | 6 | AR | JEFFERSON COMPREHENSIVE CARE SYSTEM INC | 9 | 1 | 1 | 0 | NACHC |
| 55 | 6 | HI | KALIHI PALAMA HEALTH CENTER | 9 | 1 | 1 | 0 | NACHC |
| 56 | 6 | MO | KANSAS CITY CARE CLINIC | 10 | 1 | 1 | 0 | NACHC |
| 57 | 6 | GA | MEDCURA HEALTH INC | 16 | 1 | 1 | 0 | NACHC |
| 58 | 6 | LA | MOREHOUSE COMMUNITY MEDICAL CENTERS INC | 18 | 1 | 1 | 0 | NACHC |
| 59 | 6 | AK | PENINSULA COMMUNITY HEALTH SERVICES OF ALASKA,… | 3 | 1 | 1 | 0 | NACHC |
| 60 | 6 | PR | PRYMED MEDICAL CARE INC. | 3 | 1 | 1 | 0 | NACHC |
| 61 | 6 | CA | RITTER CENTER | 4 | 1 | 1 | 0 | NACHC |
| 62 | 6 | NC | RURAL HEALTH GROUP, INC | 22 | 1 | 1 | 0 | NACHC |
| 63 | 6 | MN | SAWTOOTH MOUNTAIN CLINIC | 4 | 1 | 1 | 0 | NACHC |
| 64 | 6 | HI | WAIMANALO HEALTH CENTER | 5 | 1 | 1 | 0 | NACHC |
| 65 | 6 | WA | COLUMBIA BASIN HEALTH ASSOCIATION | 6 | 1 | 1 | 0 | NACHC |
| 66 | 6 | CA | MENDOCINO COMMUNITY HEALTH CLINIC INC | 10 | 1 | 1 | 0 | NACHC |
| 67 | 6 | AL | ALETHEIA HOUSE INC | 3 | 1 | 1 | 0 | NatCon |
| 68 | 6 | MO | FAMILY CARE HEALTH CENTERS | 4 | 1 | 1 | 0 | NatCon |
| 69 | 6 | IN | VALLEY PROFESSIONALS COMMUNITY HEALTH CENTER I… | 16 | 1 | 1 | 1 | NatCon |
| 70 | 6 | IL | CHESTNUT HEALTH SYSTEMS INC | 8 | 1 | 1 | 0 | NatCon |
| 71 | 6 | AK | MAT-SU HEALTH SERVICES, INC. | 4 | 1 | 0 | 1 | NatCon |
| 72 | 6 | NY | COMMUNITY HEALTH CENTER OF BUFFALO, INC | 6 | 1 | 1 | 0 | NatCon |
| 73 | 6 | NC | NORTH CAROLINA DEPARTMENT OF HEALTH & HUMAN SE… | 14 | 1 | 1 | 0 | NatCon |
| 74 | 6 | AL | ALTAPOINTE HEALTH SYSTEMS INC | 9 | 1 | 1 | 0 | NatCon |
| 75 | 5 | IN | Bowen Health, INC. | 16 | 3 | 3 | 0 | NatCon |
| 76 | 5 | CT | INTERCOMMUNITY INC | 16 | 3 | 2 | 0 | NatCon |
| 77 | 5 | OH | COMMUNITY SUPPORT SERVICES INC | 1 | 3 | 3 | 0 | NatCon |
| 78 | 5 | CA | CASTLE FAMILY HEALTH CENTERS, INC. | 4 | 2 | 2 | 0 | NACHC |
| 79 | 5 | CA | ST. JOHN'S COMMUNITY HEALTH | 29 | 2 | 1 | 0 | NACHC |
| 80 | 5 | PR | MIGRANT HEALTH CENTER WESTERN REGION INC | 26 | 2 | 2 | 0 | NACHC |
| 81 | 5 | CA | APLA HEALTH & WELLNESS | 14 | 1 | 1 | 0 | NACHC |
| 82 | 5 | MA | BROCKTON NEIGHBORHOOD HEALTH CENTER, INC. | 7 | 1 | 0 | 0 | NACHC |
| 83 | 5 | NY | BRONX COMMUNITY HEALTH NETWORK, INC. | 20 | 1 | 1 | 0 | NACHC |
| 84 | 5 | NY | Finger Lakes Community Health, Inc | 15 | 1 | 1 | 0 | NACHC |
| 85 | 5 | CO | SALUD FAMILY HEALTH, INC. | 24 | 1 | 1 | 0 | NACHC |
| 86 | 5 | SC | CARESOUTH CAROLINA INC | 21 | 1 | 1 | 0 | NACHC |
| 87 | 5 | TX | COASTAL GATEWAY HEALTH CENTER | 1 | 1 | 1 | 0 | NACHC |
| 88 | 5 | IL | ERIE FAMILY HEALTH CENTER | 13 | 1 | 1 | 0 | NACHC |
| 89 | 5 | MA | FENWAY COMMUNITY HEALTH CENTER, INC. | 1 | 1 | 1 | 0 | NACHC |
| 90 | 5 | TX | LEGACY COMMUNITY HEALTH SERVICES INC | 64 | 1 | 0 | 0 | NACHC |
| 91 | 5 | DC | MARY'S CENTER FOR MATERNAL AND CHILD CARE INC. | 30 | 1 | 1 | 0 | NACHC |
| 92 | 5 | NY | OAK ORCHARD COMMUNITY HEALTH CENTER, INC. | 14 | 1 | 1 | 0 | NACHC |
| 93 | 5 | IA | PRIMARY HEALTH CARE, INC | 18 | 1 | 1 | 0 | NACHC |
| 94 | 5 | MT | PUREVIEW HEALTH CENTER | 11 | 1 | 1 | 0 | NACHC |
| 95 | 5 | MO | Swope Health Services | 19 | 1 | 1 | 0 | NACHC |
| 96 | 5 | CA | SCHOOL HEALTH CLINICS OF SANTA CLARA COUNTY | 6 | 1 | 1 | 0 | NACHC |
| 97 | 5 | MI | CHERRY STREET SERVICES INC | 25 | 1 | 1 | 1 | NatCon |
| 98 | 5 | PA | GREATER PHILADELPHIA HEALTH ACTION INC | 13 | 1 | 0 | 0 | NatCon |
| 99 | 5 | CT | FIRST CHOICE HEALTH CENTERS, INC. | 13 | 1 | 1 | 0 | NatCon |


## Tier C — 28 accounts (nurture or skip)

Low-fit on current signals. Parked for re-scoring when a trigger event surfaces (new BH job posting, leadership change, recent BH grant). See the full CSV for the list.

---

## What this score doesn't capture yet

The following signals would improve the score materially but weren't available in this build:

| Missing signal | Why it matters | Path to add |
|---|---|---|
| **Medicaid payer share** (UDS Table 4) | Encounter-based billing economics work when Medicaid ≥ 50% | Playwright scrape of HRSA drill-down or FOIA request (2–8 weeks) |
| **Total patients served** (UDS Table 3A) | Confirms org is big enough to justify onboarding but not so big it builds in-house | Same as above |
| **BH encounter ratio** (UDS Table 5) | Low ratio = real capacity gap = need signal | Same as above |
| **Recent HRSA BH supplemental grants** | Indicates active BH budget + intent | TAGGS.hhs.gov manual pull, ~1 hour quarterly |
| **Open psychiatry / therapist job postings** | "Why now" timing signal | Indeed + LinkedIn scrape, requires ongoing monitoring |
| **Leadership transitions** (CEO/CMO/BH Director) | New leader = new initiatives / vendor evaluations | LinkedIn Sales Nav "changed jobs" filter |

**Recommendation:** Start outbound on the Tier A list now. The missing signals are nice-to-have for deeper qualification, not for initial targeting. Layer them in as Ascend scales outbound volume.

---

## Open questions to refine the model

1. **State priority:** Should we weight Ascend's 5 live states exclusively, or is geographic expansion active and we should score adjacent states closer to par?
2. **Look-Alikes:** Any Ascend data on whether LALs have closed at similar rates to full FQHCs? If no meaningful difference, we could drop factor #3 and reallocate the point.
3. **Existing pipeline:** Are any Tier A accounts already in Ascend's CRM as active opportunities? If so, flag them so we don't duplicate outreach.
4. **Conflicting partnerships:** Any FQHC systems that have existing integrated BH contracts with competitors (Array, Brave, Iris)? Those should be deprioritized regardless of score.

---

*Built 2026-04-22 from HRSA public data + NACHC/NatCon conference attendee lists. Full CSV: [`FQHC_scored.csv`](./FQHC_scored.csv). Matched contact detail: [`Combined_with_fqhc_match.csv`](./Combined_with_fqhc_match.csv).*
