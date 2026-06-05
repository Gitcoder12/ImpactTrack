# ImpactTrack Data Schema

## Cause
| Field | Type | Description |
|-------|------|-------------|
| id | string | Unique cause ID |
| title | string | Cause name |
| category | string | education / healthcare / infrastructure / environment |
| goal_inr | int | Funding target in INR |
| raised_inr | int | Amount raised so far |
| verified | bool | Admin-verified cause |
| location | string | Geographic location |
| updates | Update[] | Progress updates from organizer |

## Update
| Field | Type | Description |
|-------|------|-------------|
| date | ISO date | Update date |
| text | string | Progress description |

## Donation (planned)
| Field | Type | Description |
|-------|------|-------------|
| id | string | Transaction ID |
| cause_id | string | FK → Cause |
| donor_id | string | FK → User (anonymous optional) |
| amount_inr | int | Amount donated |
| timestamp | datetime | When the donation was made |
