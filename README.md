# football-betting-model-SERIE-A-
🏟️ The "Pitch-First" Football Outlook & Execution Model
Most betting models are obsessed with "Market Value"—hunting for discrepancies between a bookmaker's price and a mathematical probability. This model ignores the books.

This tool is designed to identify the Ground Truth of a match. It focuses on how teams actually behave on the grass, specifically isolating Home Offensive Power against Away Defensive Vulnerability, while quantifying the "missing teeth" of a squad through Scorer Dependency. It provides both a tactical narrative and actionable betting picks based on the most probable on-pitch outcome, regardless of what the market says.

🧠 The Philosophy: Reality > Odds
While bookmakers adjust prices based on market sentiment and liability, this model focuses on three immutable factors:

The Home/Away Matrix: It doesn't just look at "form"; it specifically pits the Home Team's scoring rate at their own stadium against the Away Team's performance on the road.

The Dependency: If a team loses its primary scorer, their historical average is a lie. This model calculates the Absence Impact to show exactly how much of a team's "threat" is sitting in the stands.

The Execution: It translates these realities into specific bets (Totals, Results, or BTTS) based on the most likely physical outcome of the 90 minutes.

🚀 Key Features
🏠 Home/Away Split Analysis: Evaluates a team’s specific performance profile (Goals/Shots) in their current environment (Home vs. Road).

🎯 On-Pitch Dependency Rating: Calculates the Dep %—the exact percentage of a team's total season goals attributed to specific players.

🚨 Absence Impact Analysis: A "Real-World" adjustment that flags how much offensive threat is lost when key players are sidelined.

💰 Actionable Betting Outputs: Moves beyond data to provide specific betting suggestions based on the statistical "path of least resistance."

📁 Data Requirements
To run this model, you need two CSV files in the root directory:

1) I1.csv: Match history (Standard football-data.co.uk format) containing HomeTeam, AwayTeam, FTHG, FTAG, and FTR.

2) players stats.csv: An FBref-style export containing player names, squads, and goal totals.



🛠️ Usage
Modify the __main__ block to include the teams and any confirmed absences. The model will handle the baseline comparison and the dependency math:
report = get_match_summary(
    home_team="Sassuolo", 
    away_team="Verona", 
    missing_away=["Gift Orban"] # The model subtracts his 'Pitch Impact' from the Away threat
)
print(report)
