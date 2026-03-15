# GrassClaw AI 🌱

A fun AI assistant that monitors trading behavior, calculates a "GrassScore", and reminds traders to step away from charts and **touch grass**. 

---

## Features
- Generates random trading behavior stats (trades, loss streak, leverage)
- Calculates a fun **GrassScore**
- Outputs recommendations to **step away from charts**
- Designed for fun, educational, and demo purposes
- Works as a terminal-based AI assistant
- 
How It Works

GrassClaw simulates trading behavior and evaluates whether a trader might benefit from stepping away from the charts.

The assistant analyzes three key indicators of trading activity:

1. Trading Frequency
The number of trades executed within the last hour.
High trading frequency may indicate overtrading or emotional trading.

2. Loss Streak
The number of consecutive losing trades.
A prolonged losing streak can lead to revenge trading and poor decision-making.

3. Leverage Usage
The leverage level used during trades.
Higher leverage increases risk exposure and market stress.

GrassScore Calculation
GrassClaw combines these factors into a single metric called the GrassScore.
Example formula:
GrassScore = Trades in Last Hour + ( Loss Streak × 5) + (Leverage ÷ 2)

This scoring system creates a simple behavioral signal where Higher scores indicate a higher likelihood that the trader may need a break.

Grass Protocol
If the GrassScore exceeds a certain threshold, Grass Protocol activates.
When activated, the assistant recommends stepping away from trading activity.

Example output:

GrassScore: 38    ;   GRASS PROTOCOL ACTIVATED
Recommendation: Step away from charts and touch grass.
This humorous alert encourages healthier trading habits and reminds users to maintain balance.
Demo Behavior

CONCEPT

# grassclaw_demo.py

def calculate_grass_score(trades, loss_streak, leverage):
    score = trades + (loss_streak * 5) + (leverage // 2)
    return score


def analyze_behavior(trades, loss_streak, leverage):
    print("\nBehavior Analysis:")

    if trades > 20:
        print("- High trading frequency detected.")
    else:
        print("- Trading frequency within normal range.")

    if loss_streak >= 3:
        print("- Loss streak detected. Risk of revenge trading.")
    else:
        print("- No significant loss streak.")

    if leverage >= 20:
        print("- High leverage usage increases liquidation risk.")
    else:
        print("- Leverage within moderate levels.")


print("🌱 Welcome to GrassClaw AI")
print("Trading Behavior Check\n")

trades = int(input("Trades in last hour: "))
loss_streak = int(input("Current loss streak: "))
leverage = int(input("Leverage used: "))

score = calculate_grass_score(trades, loss_streak, leverage)

print("\nGrassScore:", score, "🌱")

analyze_behavior(trades, loss_streak, leverage)

print("\nRecommendation:")

if score > 35:
    print("🚨 GRASS PROTOCOL ACTIVATED")
    print("Step away from charts and touch grass.")
elif score > 20:
    print("⚠️ Trading behavior becoming risky.")
    print("Consider taking a short break.")
else:
    print("✅ Trading behavior looks healthy.")

Output example :


🌱 Welcome to GrassClaw AI
Trading Behavior Check

Trades in last hour: 22
Current loss streak: 4
Leverage used: 25

GrassScore: 42 🌱

Behavior Analysis:
- High trading frequency detected.
- Loss streak detected. Risk of revenge trading.
- High leverage usage increases liquidation risk.

Recommendation:
🚨 GRASS PROTOCOL ACTIVATED
Step away from charts and touch grass.
