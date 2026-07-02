# Uber-Data-Analysis-project


NAME: VASUDEVA REDDY

NO.OF WEEKS: 4

PROJECT NAME :Email-Spam-Classifier

PROJECT SCOPE:

This project demonstrates a complete ETL (Extract, Transform, Load) pipeline for Uber trip data. It begins by extracting raw trip records, transforms them into a structured star schema, stores the processed data in a SQLite database, and performs SQL-based analytics. Finally.


source code:

# Convert datetime columns to datetime data types
df['tpep_pickup_datetime'] = pd.to_datetime(df['tpep_pickup_datetime'])
df['tpep_dropoff_datetime'] = pd.to_datetime(df['tpep_dropoff_datetime'])

# Remove duplicates and reset the index to assign a unique trip_id
df = df.drop_duplicates().reset_index(drop=True)
df['trip_id'] = df.index

print(f"Cleaned dataset shape: {df.shape}")


