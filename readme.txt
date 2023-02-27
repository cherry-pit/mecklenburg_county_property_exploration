## Original Data Sources
- Historical tax data can be found for Mecklenburg County here: https://mecklenburgcounty.exavault.com/share/view/mg5f-3uke3hyw
- Parcel sale information can be found here: http://maps.co.mecklenburg.nc.us/opendata/Parcel_SalesData.zip
- Rental data was pulled from here: https://www.apartments.com/houses/1/?sk=528d8aef8b5a3a582f429474b0bb3191&bb=zv026oh92Hs6xxo3V
- Retnal data was pulled from here as well: https://www.zillow.com/mecklenburg-county-nc/rent-houses/

## Files included

raw_data.7z --v
	2009_2021_taxassements.parquet    |    Parcel tax assement data that was used and originally sourced from mecklenburg county, this is for year 2009 to 2021
	2009_2023_salesdata.parquet    |    Parcel transaction data that was used and originally sourced from mecklenburg county, this is for all years up to 2023
mecklenburgcounty_property_transactions_export.csv    |    Large csv of property sales that occurered with tax assments for the year of sale joined on. Rent prices at the time of scrape are also joined on for the properties that have rental information. Since this is dependant on tax assement data it only goes to 2021. This also only uncludes data for parcels with a type of Single-Family home
mecklenburgcounty_rental_information_export.csv    |   Large csv of all rental information gathered from Zillow and Apartments.com

## Notes

Some sales were unable to be matched to tax records, these occurences were omited from the mecklenburgcounty_property_transactions_export.csv.

The vast majority of values in the rent field are null, this is expected. Records included for any property sale. Most are not for rent. Provided is the raw scraped rental data as well for any needs.
