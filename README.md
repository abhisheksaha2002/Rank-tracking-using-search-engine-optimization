#Keyword Ranking Check with Python




Looking for a cost-effective solution to monitor your website's search engine rankings and compare them with your competitors? This Python script offers a convenient way to track rankings for both mobile and desktop platforms. 
The script has been updated to use Beautiful Soup for web scraping and now includes a feature to compare your rankings with up to four competitors. An enhancement to include a keyword file is planned, but currently, the script is functional and incorporates the competitor comparison feature





## Usage

To run the script and retrieve rankings for your site and competitors, you'll need to make some updates in the `rank.py` file. In line 15 of `rank.py`, you will find the following input parameters:

- keyword: Keyword we want to check.
- sitename: Your website URL.
- competitors: The URLs of the competitors you want to check.

For example, if you want to check the keyword **running shoes** and your website is https://www.adidas.com, it should look something like this:

```python
# inputs
keyword = 'running shoes'
sitename = "https://www.adidas.com/"

competitor1 = "https://www.nike.com"
competitor2 = "https://www.reebok.com"
competitor3 = "https://www.ascics.com"
competitor4 = "https://www.hoka.com"
```
Once you've updated these fields, you can run the following command in your terminal to execute the script:

```bash
python rank.py

```
## Results

The script performs two checks: one on mobile and the other on desktop. If everything goes well, you should be able to view your ranking results as well as your competitors' rankings for both mobile and desktop.

![Rankings check](rank.gif)

Additionally, the script generates an Excel (.xlsx) file in the same folder where rank.py is located. The file is named after the keyword and contains two tabs: one for mobile rankings and another for desktop rankings.

For example:
| Keyword       | Rank | URL                                               | Date       | Type         |
|---------------|------|---------------------------------------------------|------------|--------------|
| running shoes | 4    | https://www.adidas.com/us/women-running-shoes    | 09-01-2024 | My Site      |
| running shoes | 2    | https://www.nike.com/w/running-shoes-37v7jzy7ok | 09-01-2024 | Competitor  |
| running shoes | 19   | https://www.reebok.com/c/200000012/men-running-shoes | 09-01-2024 | Competitor  |
| running shoes | 8    | https://www.hoka.com/en/us/                      | 09-01-2024 | Competitor  |













