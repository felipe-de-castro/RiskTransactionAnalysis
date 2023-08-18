### Purpose of the analysis:
- To search for suspicious behaviors based on the available data.
- To conduct an analysis where it is possible to identify fraud patterns for both the payer and the payee.

### Preparing data for analysis:
- CSV file with data was read and a DataFrame was created using Pandas.
- A temporary table as a view for SQL manipulation was created using Spark.

### Business performance metric analysis:
- Average transaction amount (with and without CBK) is R$ 672.33.
- Average transaction amount for transactions with CBK: R$ 1453.58.

### Analysis focused on the quantity and values of Chargeback (CBK):
- Merchants with the highest CBK values.
- Merchants with the highest CBK quantities.
- Payers with the highest CBK values.
- Payers with the highest CBK quantities.

### Distribution of chargebacks per time of day:
When analyzing the distribution of chargebacks by hour of the day, it was possible to identify that the afternoon and nighttime periods have the highest occurrences of fraud. Thus, it can be observed that these periods have a higher intention of fraud and vulnerability.

### Evaluating user_id behavior regarding device alternation:
- In this analysis, the aim is to investigate user behavior per day of use, where it's possible to identify the possibility of switching devices to perform transactions and later dispute them. The idea is that the user_id might be acting in bad faith, believing that by switching devices they are evading fraud detection by crossing with their identifier.

### Assessing risk based on the quantity of used cards:
- Generating a risk validation parameter based on the number of cards used per user and per day of use, regardless of the merchant. Thus, even if someone has made multiple payments to two merchants using 6 cards (3 for each merchant), it would indicate a high insecurity index.
