# Menstrual Cycle Tracker - Blueprints

Notification blueprints for the [Menstrual Cycle Tracker](https://github.com/sjfehlen/flow-meter) Home Assistant integration.

## Prerequisites

Install the integration first:
- HACS → Integrations → Custom Repositories → `https://github.com/sjfehlen/flow-meter` → Integration

---

## Blueprints

### Menstrual Cycle Tracker - Notifications

Sends notifications for all cycle events with individual toggles for each type.

**Import via HA:**

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fsjfehlen%2Fcycle-tracker-blueprints%2Fblob%2Fmain%2Fblueprints%2Fautomation%2Fmenstrual_cycle_notifications.yaml)

Or manually: Settings → Blueprints → Import Blueprint → paste this URL:
```
https://github.com/sjfehlen/cycle-tracker-blueprints/blob/main/blueprints/automation/menstrual_cycle_notifications.yaml
```

**Notifications included:**

| Event | Default |
|---|---|
| Period Started | On |
| Period Ended | On |
| Period Due Soon (configurable days warning) | On |
| PMS Window (daily during 5-day window) | On |
| Fertile Window Started | On |
| Ovulation Phase Started | Off |
| Period Start Reminder with "Log it now" button | On |

**Pronoun / name customisation:**

Set `Subject` and `Possessive` to personalise messages:

| Person | Subject | Possessive |
|---|---|---|
| Yourself | `You` | `Your` |
| Named person | `Alex` | `Alex's` |
| She/her | `She` | `Her` |
| They/them | `They` | `Their` |

**Period Start Reminder:**

On the predicted period start day, a notification is sent with a **"Log it now"** button.
If the period is not logged, the reminder repeats daily (showing how many days late)
until it is confirmed. Tapping the button automatically calls `log_period_start`.

---

## HACS

To add via HACS:
1. HACS → Automation → Custom Repositories
2. URL: `https://github.com/sjfehlen/cycle-tracker-blueprints`
3. Category: **Blueprint**
4. Install "Menstrual Cycle Tracker - Notifications"
