# Tixguru Step-by-Step 使用方式

1. 進入python virtual environment
```
cd ethscraper
source venv_3/bin/active
```

2. 安裝必要套件
```
pip install requests pandas simplejson
```

3. 執行ethscraper.py
```
python ethscraper.py
```

4. 看Raw Data
```
vim raw_result
```

# 注意事項

1. 目前只能看到此帳戶的資料

```
0x687aeda127fd2bd4f374c73e3724bf9b7c7a6b9c
```

2. 資料的名稱可以對照此網址
https://etherscan.io/address/0x687aeda127fd2bd4f374c73e3724bf9b7c7a6b9c

3. 如果想要查詢其他帳戶的資料，可以將ethscraper.py第11行的code改掉
```
address = '0x....'
```

# TODO

1. 完整API的查詢功能實作

https://etherscan.io/apis

# ETHScraper
simple web dashboard, which tracks transactions for one specified address on the Ethereum blockchain
## Getting started
The dashboard shows three different plots tracking the transactional data for the Ethereum address [0x687aeda127fd2bd4f374c73e3724bf9b7c7a6b9c](https://etherscan.io/txs?a=0x687aeda127fd2bd4f374c73e3724bf9b7c7a6b9c&p=1):
- The first plot represents the incoming transactions per day in total Ether transferred
- The second plot represents the outgoing transactions per day in total Ether transferred
- The third plot represents the number of new Ethereum addresses making incoming transactions

The data is scraped using the [ethscraper.py](ethscraper.py) Python script. The script is run via a Cron job to deliver daily updates of transaction data to the dashboard.
## Built with
- [Bootstrap](https://getbootstrap.com/) - The web framework used for the dashboard
- [plotly.js](https://plot.ly/javascript/) - The charting library for the plots
- [Etherscan](https://etherscan.io/apis/) - The API used to track Ethereum blockchain transaction data
- [Requests](http://docs.python-requests.org/en/master/) - The HTTP library used to query the Etherscan API
- [pandas](http://pandas.pydata.org/) - The data analysis library preparing the dataframes for the plots
## Contributing
Please feel free to fork and submit pull requests. However keep in mind that the project currently focuses on one specific ETH address, which will probably not be changed in the future. Changes requiring a different address are better off in a separate repository.
## License
This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details
## Acknowledgements
Thank you to [/u/ma007](https://www.reddit.com/user/ma007) for inspiration and the focal ETH address
