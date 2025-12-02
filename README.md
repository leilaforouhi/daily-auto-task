import datetime
import json
import os

def save_daily_log():
    today = datetime.date.today().isoformat()
    log = {"last_run": today}

    with open("daily_log.json", "w") as f:
        json.dump(log, f, indent=4)

    print(f"Daily log updated for: {today}")

if __name__ == "__main__":
    save_daily_log()
