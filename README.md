Implementation of Personal Fitness Tracker using Python (P3)

# Connect to SQLite
conn = sqlite3.connect("fitness_tracker.db")
cursor = conn.cursor()

# Create table
cursor.execute('''CREATE TABLE IF NOT EXISTS fitness_log (
                    id INTEGER PRIMARY KEY AUTOINCREMENT,
                    date TEXT,
                    steps INTEGER,
                    calories INTEGER,
                    workout_time INTEGER)''')

conn.commit()
conn.close()
print("Database setup complete!")

