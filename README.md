
### Purpose of the analysis:
- To search for suspicious behaviors based on the available data.
- To conduct an analysis where it is possible to identify fraud patterns for both the payer and the payee.
- For better visualization of the graphs and build in graphs made by Databricks plataform, please acess the following link: [Databricks Notebooks](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1007048438137268/2629043615626782/3738436857841248/latest.html)

## Below are the text topic in English, since it was made in portuguese :brazil:. 
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

### Conclusion

### Considerations for improving the analysis:
- User_id geolocation: Enabling location data during a transaction could provide an opportunity to investigate if there's any fraudulent behavior such as account takeover (ATO), mobile theft, or account sharing. This would involve looking at payment patterns and locations.
- Device type: Apple, Android - If possible, including the model and brand of the device. By capturing these original user information, it would be possible to evaluate device-switching behavior or even occurrences of device spoofing (a technique that generates software/hardware to deceive).

### Suggestions:

- Limit the frequency of device switches per day as a preventive measure.
- Conduct an individual analysis of merchants if they receive amounts that deviate from the norm and if they cumulatively receive transactions from user_ids with a high number of card insertions. This could lead to implementing restrictions.
- Restrict the same device from being used by multiple user_ids.
