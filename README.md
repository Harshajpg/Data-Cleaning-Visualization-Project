import pandas as pd
import matplotlib.pyplot as plt

data = {
    "Player": [
        "Virat Kohli",
        "Shubman Gill",
        "Jasprit Bumrah",
        "Yuzvendra Chahal",
        "KL Rahul",
        "Hardik Pandya"
    ],
    "Runs": [741, 890, 20, 15, 620, 350],
    "Wickets": [0, 0, 24, 27, 0, 12],
    "Matches": [15, 17, 14, 15, 14, 13]
}

df = pd.DataFrame(data)

print(df)

plt.figure(figsize=(8,5))
plt.bar(df["Player"], df["Runs"])
plt.title("IPL Runs Analysis")
plt.xticks(rotation=45)
plt.show()

plt.figure(figsize=(8,5))
plt.bar(df["Player"], df["Wickets"])
plt.title("IPL Wickets Analysis")
plt.xticks(rotation=45)
plt.show()

print("\nStatistics:")
print(df.describe())
