# How to use FinancialModelingPrep on Web3

> [Airnode](https://api3.org/airnode) API Documentation

<h3>Free <a href="https://financialmodelingprep.com/developer/docs">financial statement API</a>. <br> Real-time and historical data of stock prices.</h3>

Supports over **25000 stocks** across multiple exchanges. <br />
<br />
<br />

<div align="center">
  <span>
    <img alt="Apple" src="/images/image-1.png" width="50">
    <img alt="Netflix" src="/images/image-2.png" width="50">
    <img alt="Tesla" src="/images/image-3.png" width="50">
    <img alt="Bitcoin" src="/images/image-4.png" width="50">
    <img alt="Lyft" src="/images/image-5.png" width="50">
  </span>
</div>

<br />

<p align="center">
  <b>Whole U.S. market, XETRA, EURONEX, TSX, SEDAR, SEHK and more.</b>
</p>
<h4 align="center">
  <b><a href="https://financialmodelingprep.com">Home Page</a></b>
  •
  <a href="https://financialmodelingprep.com/register">Register</a>
  •
  <a href="https://financialmodelingprep.com/developer/docs">Documentation</a>
  •
  <a href="mailto:info@financialmodelingprep.com">Support</a>
</h4>
<p></p>

<h1 align="center">Key Features  <p> </p> </h1>

Use our data that goes up to 30 years back in history. Earnings calendar, financial statements, multiple exchanges and more. We provide one of the most accurate data available on the market. <br />

<p align="center">

[![Trusted By 30.000 Customers !](https://img.shields.io/badge/Trusted%20by-30K+%20Customers-1abc9c.svg)](https://financialmodelingprep.com/developer)
[![Twitter Follow](https://img.shields.io/twitter/follow/financial_mod?style=social)](https://twitter.com/financial_mod)
[![GitHub Repo stars](https://img.shields.io/github/stars/antoinevulcain/Financial-Modeling-Prep-API?style=social)](https://github.com/antoinevulcain/Financial-Modeling-Prep-API)
[![Linkedin](https://img.shields.io/badge/LinkedIn-blue)](https://www.linkedin.com/company/financial-modeling-prep)
[![Status](https://img.shields.io/badge/Status-success)](https://financialmodelingprep.com/developer/docs/status)
[![Docs](https://img.shields.io/badge/API%20Docs-red)](https://financialmodelingprep.com/developer/docs/)

</p>


**Home Page:** {{ URL to API home page }}  
**Web2 Docs:** {{ URL to API documentation }}

## Call this Airnode API

Read the [Airnode developer documentation](https://docs.api3.org/d/call-an-airnode) to learn how to call Airnode APIs. You'll need the **Provider ID** to call any endpoint in this API.

**Provider ID:** 0x182e9c2acbdf34d3b87cadc8b6423ab82f04d8d6d422897696274d31fe615cf5

**Provider XPub:** xpub661MyMwAqRbcGqJMAKgC35TYaAEScfLiHXRTyTk6amLXWgtyZsXBorxbQscwSUfVgLiu98FRUJbkeG8icfhLJQdSymfh5pzQ36hFwuPm85P 

[Reserved Parameters](https://docs.api3.org/r/reserved-parameters) are used to control Airnode behavior and are available for all endpoints.

## Available on Networks:

> Find more information on each chain [Here](https://ethereum.org/en/developers/docs/networks/).

| Chain                                | Airnode RRP Contract                       |
| ------------------------------------ | ------------------------------------------ |
| Rinkeby                                 | 0xF9C39ec11055508BddA0Bc2a0234aBbbC09a3DeC                                 |

# Endpoints
1. [GET /v3/financial-statement-symbol-lists](#0x7a92e04086a7612f85e55d8d791e1323dc4469f5c510176ac3e7b997d87cf8bd)
2. [GET /v3/income-statement/{symbol}](#0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db)
3. [GET /v3/balance-sheet-statement/{symbol}](#0x593e38bae8a4e3e7a1b80a8c4b2e7363bdcdfc8434fa46a76fc49aeed6894950)
4. [GET /v3/cash-flow-statement/{symbol}](#0xc93ced08b3801d834b9e0b46314deadd015923b59c3c9572f9b1109d76bde079)
5. [GET /v3/income-statement-as-reported/{symbol}](#0xdb2edde7c0fcd0c68e6b44b7d4a94873d6320a48a7204606770b4b2ca88cb2b1)
6. [GET /v3/balance-sheet-statement-as-reported/{symbol}](#0x8b36e15b108f18695210870aa5ef1ee0b6db8efd98637b04655afd02a08b2f50)
7. [GET /v3/cash-flow-statement-as-reported/{symbol}](#0xa9e134dca78a7301a94624dfc64a13baec0bb58a35d1318e47d2bffcecd4fdcd)
8. [GET /v3/financial-statement-full-as-reported/{symbol}](#0x1b94493ceb218bdfe5c6c1fa25c09e8366d3964939473d9a898118fffb7c015b)
9. [GET /v3/income-statement/{symbol}](#0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db)
10. [GET /v3/financial-statements/{symbol}](#0x5357de3fabc940fb28fc293e5ceb8b818b5a2ce0bbe4c891026893f28f682366)
11. [GET /v4/financial-reports-dates](#0x36c15ab2247a81e28aa6fa2c10222ae8ce840904b5857c27753e68ab4dc9b5c5)
12. [GET /v4/financial-reports-json](#0x0449d269e3c08f92abd5120dee267a777b1a0ae200abb3324ef2d5c5abc36162)
13. [GET /v4/shares_float](#0x2e8f5a7acb9c4ac1cb2e500ac09455b77917fa65770c79a83db4c71fac60642d)
14. [GET /v4/shares_float/all](#0x58baa0dcac6924c4129f64a64c1b414c5a9a3a429e9f1b828848bb75a884510f)
15. [GET /v4/rss_feed](#0x4f4516e2cc48556fcba36e80eab3baed1e0a012d237c52befce6099e7cafe084)
16. [GET /v3/earning_call_transcript/{symbol}](#0x338180d1ef637856e0c66e35fb6540272b4f6870f2a55eec7ac93915eb5644ee)
17. [GET /v4/batch_earning_call_transcript/{symbol}](#0x428748e780ae4ecf326c72f3fa469dc3508f96761ebaad0badc8cc588f8caea4)
18. [GET /v3/sec_filings/{symbol}](#0x784f5e8f14ac4e7131d0be44d8d6f948151764dd882b3600c6ad09ff02827722)
19. [GET /v4/rss_feed_8k](#0x7b60cd4f871c5219dc44e895b643bff03f7828a11f7bf3d063a858261fbcb5af)
20. [GET /v3/ratios/{symbol}](#0x3b6ef560e4820b136eae432f33ca3247a0120927a1c7649fdc86b83f1dfeafa6)
21. [GET /v3/enterprise-values/{symbol}](#0xcc40af84f4216d7f4802d01cf4edac5fdfd9c685d9ddb1c63812aba2e70a61bf)
22. [GET /v3/income-statement-growth/{symbol}](#0xcc9a4ba1acb4056107ff03d05f42716f213c0b39af2137ab96242697a8b75a0f)
23. [GET /v3/balance-sheet-statement-growth/{symbol}](#0x084237603893e0c1d750eeda13260670f1ed2086024a8992c4622f73a412a8ef)
24. [GET /v3/cash-flow-statement-growth/{symbol}](#0x294354ba847915b9be24ca5cf40aaa58cf1134adfa403d6129ce3f557e48a4a2)
25. [GET /v3/key-metrics-ttm/{symbol}](#0x78afea8f5f354b024be361d2dde7ed208ae59f77f4c929e01254a1d4a32de2db)
26. [GET /v3/key-metrics/{symbol}](#0xf5cee6b7e8a2d3035ef040942dcb9b16de0b6e356929eac760fec061c9c05ddf)
27. [GET /v3/financial-growth/{symbol}](#0xe608cdc0dbe1ee349249994d0b399ee0c250cf6e6c1a7a2ed9ab1a8ee0466277)
28. [GET /v3/rating/{symbol}](#0x45ee30f97f68b834762fb16b9f10f59e211bbe70b314800f7330015b564a3db6)
29. [GET /v3/historical-rating/{symbol}](#0xdfdb5312feb8f42f3651623b2af176f393ec7fb14b137f35b78d44ddb80c1973)
30. [GET /v3/discounted-cash-flow/{symbol}](#0x60a393d432d929e97bd7636109af2a75d858fd1ef5473eb8b8d37cfd3140f224)
31. [GET /v3/historical-discounted-cash-flow-statement/{symbol}](#0x79a8fd3caa539331b18e87fffc4f5d05d16085910c1fa79d785d36d27374838c)
32. [GET /v3/historical-daily-discounted-cash-flow/{symbol}](#0xaca8caf67075f059cb66f19d44c2efa598086cfb8a081159cbb07806324ff241)
33. [GET /v3/earning_calendar](#0x26d554accbfcbae6987dfa5b9f02b7bd3cbe887b23190bcc06bb022f1e494f0f)
34. [GET /v3/historical/earning_calendar/{symbol}](#0x47a1d9b10a83651bc37758429bdff597fcd25c3c49f9e5591c54d1a2fdd70abc)
35. [GET /v3/ipo_calendar](#0x4662cd94cfb11798eef704fdc211ee489693e45bb5f2a15e5b7b2b64ac106107)
36. [GET /v3/stock_split_calendar](#0xe6b64232543e0f8ec44b06b794ea9bac1f30e3194446b705f69d583505b2d887)
37. [GET /v3/stock_dividend_calendar](#0x7c82f8fd59f261f612e76210e69ae29128bbfde68acdcc910013a2bf3bb8ecc9)
38. [GET /v3/economic_calendar](#0xa8cd3d01e5a6ede542df42226fd8192a228f59c5455965de48bc1f2f8cded14d)
39. [GET /v3/search](#0xfd6eb01969f7e3a2904382229564636e4423a398acfe40f182c543737b27846b)
40. [GET /v3/search-ticker](#0x4c3bc218efd10bfa620732e05c94616d8ea50413781960d3a917af71c4e79eab)
41. [GET /v3/stock-screener](#0x2b39fd9c23518233cd8285813b3ee47cd3f58765ef7d6e39573575825e6f4d35)
42. [GET /v3/get-all-countries](#0x55de15995bf3086d8eb2e95be132c8e8fc683e7360f8f0d464aecc46a7ff38e0)
43. [GET /v3/profile/{symbol}](#0xc77379b6803bfb6a3bc8c17652916281c6c687fc9e7d50a6f4c9e6ba56715dca)
44. [GET /v3/key-executives/{symbol}](#0x9d02f28e45306d8729c95a8e38222ee2f6621e6a383475bb5845e4237bf942df)
45. [GET /v3/market-capitalization/{symbol}](#0x6f2a3e7e2d263d737fc8765fd1fefba6e0b011b1430be1a57c424c5b953c6dc5)
46. [GET /v3/historical-market-capitalization/{symbol}](#0xeeb404e11f70d5fd43f2ae5c8f04ba20ed33e58f55617c35e1035d5064288d98)
47. [GET /v4/company-outlook](#0x042989ba15709efe8105bfc178cc304e2e57b976cd3bcef0ac7cc60aa82f55b8)
48. [GET /v4/stock_peers](#0x94e8db923ed3a09bb3532dc1a6de3e904e90eb4b933757a1e2c427e07fea61bf)
49. [GET /v3/is-the-market-open](#0x0687de301cca188f078be3bbdb4be2f13373800316ae71cd9dace80858931b23)
50. [GET /v3/delisted-companies](#0x59ae66e39460b5e996adc11a1f1073a9dbffdf1eeb5341ca0a0af2e550d1cfea)
51. [GET /v4/articles](#0x92499117c90f908d061895ff836caecb00e58ee0f471e40a38032f2f68a053bd)
52. [GET /v3/stock_news](#0x3cc9821b6a5f6b8bdd6ca8c5e6be9465706f94a8c881dcf4100f360626309a9e)
53. [GET /v3/press-releases/{symbol}](#0xc34888ff56805321a7c2b650065753485a355c1ffc7e155d493dbe9f8278b30d)
54. [GET /v4/sector_price_earning_ratio](#0xea1299fa30035cf94bb01f94d040926e7966747934d394a4f91a3ae207e27813)
55. [GET /v4/industry_price_earning_ratio](#0x2717b835e234a48fc40947bad9278af346f58e30661175d63b53a0d6803bd8ce)
56. [GET /v3/sectors-performance](#0x1dac39aab45ce2908ef9f8885c7f368c52cce25633f41c42cceb6ae122a6c408)
57. [GET /v3/historical-sectors-performance](#0xda2e2fbf813778cd01bcf722b2b5871720793e8e0954043185ef620395e14d0d)
58. [GET /v3/gainers](#0x0eb26c96bd29e0a63458f325fcf1c61cbd8fe4cca4efa29581dd32f8e8687983)
59. [GET /v3/losers](#0x392ec92746669d2a0d28730830d9bf1e624d6ab5d5738b80214c80fea4dbbb65)
60. [GET /v3/actives](#0xebf4654d7c1a9224bd1b1ae7a27e0ea9b70f5e16b115d6ecc7803ed46e96b8ab)
61. [GET /v4/standard_industrial_classification](#0xc34c5cca5d18714d71f6a77b6f35b0a1dd3d018bf9df9aaadada6d84bb5b380a)
62. [GET /v4/standard_industrial_classification/all](#0xbac4d7a5a482602d0a6dddf13b8ec593e7fd554121d102810b930902a148e845)
63. [GET /v4/standard_industrial_classification_list](#0xe03fe1ca41560488cd4a10dbbbbfa25c980f5e323895d987a3f64557f7f8ffc2)
64. [GET /v4/commitment_of_traders_report/list](#0x6b60d1199f4ec6b2488b63e4d39fa211753ce6f9b5c4f8897b21ec1ea8487f6e)
65. [GET /v4/commitment_of_traders_report](#0xc3677a186218cf337748b18ff482711c3554882872ebab1067e04c2007c97432)
66. [GET /v4/commitment_of_traders_report/{symbol}](#0x64864439ea51c270825cdd137ac2473f3aa1530d213af05400ca9869c8726fca)
67. [GET /v4/commitment_of_traders_report_analysis](#0x7253ff38494d9dd0e61427a1962dc8bf78625d68eac17d154f028481822bb81d)
68. [GET /v4/commitment_of_traders_report_analysis/{symbol}](#0xde76a38d22c137626be9db37420ed7e5e6f9fadebd2a0c83fc0434d4723331f3)
69. [GET /v4/social-sentiment](#0x6d3844f911ef24504d3fd4096923dbe90043c3c8cc8ecc020dd1ba1731422531)
70. [GET /v3/grade/{symbol}](#0xc722594cd6883e15aa8929123f66ce0f4102c5869d23db8479c08b171095ce6e)
71. [GET /v3/earnings-surprises/{symbol}](#0x5def20718185062e609800c5edc04770a490b4e41035ec69112b4b368420ef8a)
72. [GET /v3/analyst-estimates/{symbol}](#0x4e12bccc65fefc1c8e7c1dd36cb5b71264e89be188c28a5f1cf52c0617566e9d)
73. [GET /v4/insider-trading](#0xe24dec2fddb301e74714049e94f8f2f369c407973e5a65909cc91fa8b30e16b9)
74. [GET /v4/insider-trading-transaction-type](#0x5bc8d1cfe63be647e00e0ec18684e79331503d69aa4a61c44b9154a12dc15eaa)
75. [GET /v4/mapper-cik-name](#0x38a978540e00dd030c05a16e1937f905e5354ba288cdb9db941e3be9efa4e166)
76. [GET /v4/mapper-cik-company/{symbol}](#0xf911c7a034d480cd9b2a977f8b5c982344ebddc8d0fa223e289b7f97ccae2ccd)
77. [GET /v4/insider-trading-rss-feed](#0xc4ab4b1e6c29ef28bc775f115d5eb1662915edbd1b5e03742698ef023df6c40b)
78. [GET /v4/fail_to_deliver](#0x3d07a30ef908c9a1fc5f511ac284f3b6196f167cee678971e6cf3e626dad8bfa)
79. [GET /v3/quote/{symbol}](#0x057200614b55d7def35dd8cab6a7c86e64387942310b79d36726bc8610db0f06)
80. [GET /v3/quote-short/{symbol}](#0xc5cc0fb33749af723052eaf3037a3c9d6e036e707c0d30c071927f93d2f575c7)
81. [GET /v3/quotes/{exchange}](#0xd5deebc79e31c9eea9506ac8086c96d82793d1b17509b4c9621a2b038808c3d5)
82. [GET /v3/historical-chart/1min/{symbol}](#0xd00d92abb1348429ed9b5ab9c41646ea21a8618b9ff7b38b41e3cc6b894e06f3)
83. [GET /v3/historical-chart/5min/{symbol}](#0xdef0f6d6d8416a408fed0a3ca76432403f17d33bfbd6f80634aefd7bb003ad4c)
84. [GET /v3/historical-chart/15min/{symbol}](#0x0bffe32171a75d9244c3146dadb0ccbc313766740a2e674342e1d0173b97b2d4)
85. [GET /v3/historical-chart/30min/{symbol}](#0x87411cfc1413922e1ed9872ae91441c311c465131de8f7bb968ff3e07ca2c461)
86. [GET /v3/historical-chart/1hour/{symbol}](#0x9c7120fe43466e8c74a08a577410e7f0450b1b1b7ecaf6b5ffebd58160ef28d6)
87. [GET /v3/historical-chart/4hour/{symbol}](#0xfa27ed50687decece1b374fc0048a43aeb2f40f000e648294a7ebbba63e49f5e)
88. [GET /v3/historical-price-full/{symbol}](#0x3506b1d2fec15e1b4fa743bdf2e87bb592a74d6131b0726f1ecd82d670862c7e)
89. [GET /v3/historical-price-full/stock_dividend/{symbol}](#0xc4a0e1e7933d8e11d6ff2026ec9ddacb28d73f82ed7e39b9dc3d0946831236b4)
90. [GET /v3/historical-price-full/stock_split/{symbol}](#0x17c4b82751150c3042b2d2787df65e32bca5ea28a3e24116f698a935946254a0)
91. [GET /v4/historical-price-full/{symbol}/{date}](#0x07af2019d0b192e95dabd980d17a1aadb91395d42702d132f59895c04101764e)
92. [GET /v3/technical_indicator/daily/{symbol}](#0x9fdc095046edee80824481c6527aa2d1248509801840c21c4028f418a8ea8ed9)
93. [GET /v3/technical_indicator/1min/{symbol}](#0xc35d0c0574bb39dc1f7b30a91d4e4045c96c42b9efc2ea962bd9a161d8f0471d)
94. [GET /v3/technical_indicator/5min/{symbol}](#0x551b14085dc94aa8f926691ffebeb7252a71f76287825a8845a28a80ba01f1fe)
95. [GET /v3/technical_indicator/15min/{symbol}](#0xbac1560f9593f92ee56971bb5fa1f052d60e81d516696c4fa9a62c5189b4e140)
96. [GET /v3/technical_indicator/30min/{symbol}](#0x7166e27d120b6f22a373dbc1f78e4f8031f97cd44075aff937daae043759c6e5)
97. [GET /v3/technical_indicator/1hour/{symbol}](#0xa5ca5579842315622d8a97b76a5436f28c2f56c78e2aaf154c7e197ff4ebe0fb)
98. [GET /v3/technical_indicator/4hour/{symbol}](#0xcb3d37386174679d30df9495f9b8943179d0099ccec406a8f7b2112f81c291ee)
99. [GET /v3/etf-holder/{symbol}](#0x5ef2e446a611145c6f07c6e0f9c5681ce7d0d12b053eeba5d9c2d14610a2b7cf)
100. [GET /v3/institutional-holder/{symbol}](#0x5e81f9f5e7394932806d4b8a927ea8ddc59bc37bbb749709e9054b5a9fc25ce1)
101. [GET /v3/mutual-fund-holder/{symbol}](#0x8446caecb8e10224de7690d8226e54609a737f10114501a5209bc84a1739afc5)
102. [GET /v3/etf-sector-weightings/{symbol}](#0x3630cc47ae7370cc7044ff3edd1596921cf15b41985b14294dc307c29d6e3b17)
103. [GET /v3/etf-country-weightings/{symbol}](#0x33dd26a76035242ee98ff311ed3af98aa40c5acf2ae68fbfcaeeb9ed2f1368f0)
104. [GET /v3/cik_list](#0x37110d60e2a6eacffe7d79b8f1d3cffc201efd3f61aa01b3271fed1a0332f291)
105. [GET /v3/cik-search/{name}](#0x619de61a08a5cc62a8497acb70e72faf4f7bdef9e26329c0ca57828cb8a80ba4)
106. [GET /v3/cik/{cik}](#0xe3b3de879e009f37c8528e2cbd7e8d4397953d226c7cfd123ded3225850f27a7)
107. [GET /v3/form-thirteen/{cik}](#0x8d8118e96a64feddf0fb9017787187247c2fb7f2492d843bb5ab0342a0dd596a)
108. [GET /v3/form-thirteen-date/{cik}](#0xb523aa687cf76843842ca727225eab04053dfaad3f44c70d71d87fd0927d7e32)
109. [GET /v3/cusip/{cik}](#0x4d4cc8d394727aa0d3e6fb21988e650e91c0ebcda2c8d2cb7206d5dc4bc3dc17)
110. [GET /v3/stock/list](#0x666544755232226f2b550bd4923b46cbe113b2e431cc7e8c23aa5bdba238f7fb)
111. [GET /v3/available-traded/list](#0x7303a24685698095d04dd56361b7834e86931dd9f7fb714e7ec59c289d0bbea3)
112. [GET /v3/etf/list](#0x00133d5d7101daebc253c152632a05849d11a07fe2e84b05bd9d1e0b4af6d552)
113. [GET /v4/batch-request-end-of-day-prices](#0xe2275fb76d94a2eb09d126210c63cbb019d71545fd68d8e81533231046f5ea7a)
114. [GET /v4/income-statement-bulk](#0xac94bfb37085ab6b1b7eb4a98d26724cc06187a086ff3bef473f4458ee439cdd)
115. [GET /v4/balance-sheet-statement-bulk](#0xa384fa151c7c37df43b2ff2d6d4826917020619eddc1e3189fc9466d6735bec0)
116. [GET /v4/cash-flow-statement-bulk](#0x580da25ae71f4949fb50b296248250725e233a9e36b08d13d76e750e74c45dca)
117. [GET /v4/ratios-bulk](#0x57673de82ce3868af6195f0a77430aa7b0777ba7c5c2b0eb71db300440d1cd9f)
118. [GET /v4/key-metrics-bulk](#0xdb78e185aa7dba83fd8928085083cd5ef658a01726e20b4be5c7911fd1f89b04)
119. [GET /v4/earnings-surprises-bulk](#0xdc4284f0c390df12fdf19a3abae3a5bb528fb78b5103753adffb210dfa41d359)
120. [GET /v4/profile/all](#0x39941ed918f7be6be8523c5786ee8ef399e094b7d310966da18e91a2acf32042)
121. [GET /v3/quotes/index](#0x53810b6bd02e8c55cb9bc1bb73bbf57005ea8049a049a9656a8877d1cd131fb2)
122. [GET /v3/quote/{index}](#0xba6fb29686df04532c934d47094d4161f5a1cd294c7041b0a7b03e3d7037e899)
123. [GET /v3/sp500_constituent](#0x0086c9e5229d83dfd28ee90dfb681ca2405153e36fa8548a2c8efeba6a1372cf)
124. [GET /v3/historical/sp500_constituent](#0xf0535c78caacd8cfa01bd5ab784deeff1a6b8b125267c2c6725cd8e4fa6a334b)
125. [GET /v3/nasdaq_constituent](#0x11bf4ecec2691ca58a89c76ad0b2d0bb1ac674dff3589ece923863ab8b082071)
126. [GET /v3/dowjones_constituent](#0x704e6c91c060c739593b0c5c9c5b0a6bf6f75f6e158ee52e561ab89e97d32955)
127. [GET /v3/historical/dowjones_constituent](#0x05d201f310049da032a2f34e29bdfb3feee8195c69f347079321ad72063f8bcd)
128. [GET /v3/symbol/available-indexes](#0x2158b17f6d31a6170a437bc1beb48ae08d881094db07fd79af29ab70a7722607)
129. [GET /v3/symbol/available-euronext](#0x56e465973b2067f14a41fe3f7b8b649d9375bbed49fa69ca75f8109649dcde8c)
130. [GET /v3/quotes/euronext](#0x592362f7700ccf0b4d0ede614875dffe2ad89d3255971b0dc13ea2f0b3f512d8)
131. [GET /v3/symbol/available-tsx](#0x4597f014d3e434ae9a7a6ecd01974dbfa8455074f461254fc4f85a7974f38133)
132. [GET /v3/quotes/tsx](#0x6c2991676ba0993fbbf340e8f5e759d13fd9228865542000087261a72203b9d1)
133. [GET /v3/quotes/crypto](#0x94741d14f09d9de38d6735807f3d7d9bfc367ccd66a09aea0bd7747924125dd6)
134. [GET /v3/symbol/available-cryptocurrencies](#0x3812e035581bceddaef8eeb58da8e7829263966849236a8548eb722ef1200cac)
135. [GET /v3/fx](#0x757cd231f1360e7c11b93e6190bf333e1bebe1baaab430712c5ac5a6ac6c769f)
136. [GET /v3/quotes/forex](#0xbfa94372a7570b36f07429fd80d3c872e4429677bf7d2aae8253d6735f933fa6)
137. [GET /v3/fx/{pair}](#0xdd1ffa0cd57648ce9f4959b3ac63d791a80234531cf852196177702e0af2255a)
138. [GET /v3/symbol/available-forex-currency-pairs](#0x51dad5124d84a2a19618c33a7a49368a3bb9c972e7bedc5300315c9e69ecae61)
139. [GET /v3/symbol/available-commodities](#0x40ac15c012581e2dce07187c589b19549e8c12429fd4b96f31b0d8ede5a1c6c3)
140. [GET /v3/quotes/commodity](#0xf0b910a9f0fbfad2bf7171390fcb407f0f4609bcf2d0b0984a5393aa2ac2daef)
141. [GET /v3/symbol/available-etfs](#0x9d55f88adb0b1d7bb63f638926153f6e8068c43c142a6eb14175d1cbb7843d55)
142. [GET /v3/quotes/etf](#0xc30478970247c62b2cbac7cf912008dcee51785e5527bee0a31d042e98f4b764)
143. [GET /v3/symbol/available-mutual-funds](#0x09fa92ec3dfd92f9edbb3c30fa07b311f436341036392d17422c556febc8578d)
144. [GET /v3/quotes/mutual_fund](#0x78abc827d77172880ec0137590c4228197198670ddf78da142d4f0de45915773)
---
## GET /v3/financial-statement-symbol-lists <a name="0x7a92e04086a7612f85e55d8d791e1323dc4469f5c510176ac3e7b997d87cf8bd"></a>

List of symbols that have financial statements.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs#Financial-Statements-List

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7a92e04086a7612f85e55d8d791e1323dc4469f5c510176ac3e7b997d87cf8bd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ 
  "02M.DE", "0A00.L", "0A02.L", "0A05.L", "0A0C.L", "0A0D.L", "0A0E.L", "0A0F.L", "0A0H.L", "0A0I.L", "0A0J.L", 
  "0A0K.L", "0A0L.L", "0A0M.L", "0A0S.L", "0A0V.L", "0A0W.L", "0A0X.L", "0A10.L", "0A14.L", "0A15.L", "0A18.L", "0A1C.L", 
  "0A1J.L", "0A1K.L", "0A1L.L", "0A1M.L", "0A1N.L", "0A1O.L", "0A1R.L", "0A1S.L", "0A1U.L", "0A1V.L", "0A1W.L", "0A1X.L",
  "0A20.L", "0A21.L", "0A23.L", "0A26.L", "0A27.L", "0A28.L", "0A29.L", "0A2A.L", "0A2G.L", "0A2H.L", "0A2I.L", "0A2O.L", 
  "0A2P.L", "0A2S.L", "0A2T.L", "0A2X.L", "0A2Z.L", "0A33.L", "0A34.L", "0A36.L", "0A37.L", "0A39.L", "0ACT.L", "0AH3.L",
  "0AH7.L", "0AHI.L", "0AHJ.L", "0AI4.L", "0AJ1.L", "0AR9.L", "0B67.L", "0BDR.L", "0BFA.L", "0BJP.L", "0BNT.L", "0C6Y.L", 
  "0CDX.L", "0CHZ.L", "0CIJ.L", "0CUM.L", "0CUN.L", "0CXC.L", "0D00.L", "0D1X.L", "0DDP.L", "0DH7.L", "0DHC.L", "0DHJ.L", 
  "0DI7.L", "0DJI.L", "0DJV.L", "0DK7.L","0DK9.L", "0DKX.L", "0DLI.L", "0DMQ.L", "0DNH.L", "0DNW.L", "0DO7.L", "0DOL.L", 
  "0DOS.L", "0DP0.L", "0DP4.L", "0DPB.L", "0DPM.L", "0DPU.L", "0DQ7.L", "0DQK.L", "0DQZ.L", "0DRH.L", "0DRV.L", "0DSJ.L", 
  "0DTF.L", "0DTI.L", "0DTK.L", "0DU3.L", "0DUI.L", "0DUK.L", "0DVE.L", "0DVR.L", "0DWL.L", "0DWV.L", "0DXG.L", "0DXU.L", 
  "0DYD.L", "0DYQ.L", "0DZ0.L", "0DZC.L", "0DZJ.L", "0E1L.L", "0E1Y.L", "0E3C.L", "0E4K.L", "0E4Q.L", "0E5M.L", "0E6Y.L", 
  "0E7S.L", "0E7Z.L", "0E9V.L", "0EA2.L", "0EAQ.L", "0EAW.L", "0EBQ.L", "0EDD.L", "0EDE.L", ...
]
```
----
## GET /v3/income-statement/{symbol} <a name="0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/balance-sheet-statement/{symbol} <a name="0x593e38bae8a4e3e7a1b80a8c4b2e7363bdcdfc8434fa46a76fc49aeed6894950"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x593e38bae8a4e3e7a1b80a8c4b2e7363bdcdfc8434fa46a76fc49aeed6894950

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cash-flow-statement/{symbol} <a name="0xc93ced08b3801d834b9e0b46314deadd015923b59c3c9572f9b1109d76bde079"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc93ced08b3801d834b9e0b46314deadd015923b59c3c9572f9b1109d76bde079

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/income-statement-as-reported/{symbol} <a name="0xdb2edde7c0fcd0c68e6b44b7d4a94873d6320a48a7204606770b4b2ca88cb2b1"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdb2edde7c0fcd0c68e6b44b7d4a94873d6320a48a7204606770b4b2ca88cb2b1

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/balance-sheet-statement-as-reported/{symbol} <a name="0x8b36e15b108f18695210870aa5ef1ee0b6db8efd98637b04655afd02a08b2f50"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x8b36e15b108f18695210870aa5ef1ee0b6db8efd98637b04655afd02a08b2f50

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cash-flow-statement-as-reported/{symbol} <a name="0xa9e134dca78a7301a94624dfc64a13baec0bb58a35d1318e47d2bffcecd4fdcd"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa9e134dca78a7301a94624dfc64a13baec0bb58a35d1318e47d2bffcecd4fdcd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/financial-statement-full-as-reported/{symbol} <a name="0x1b94493ceb218bdfe5c6c1fa25c09e8366d3964939473d9a898118fffb7c015b"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x1b94493ceb218bdfe5c6c1fa25c09e8366d3964939473d9a898118fffb7c015b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/income-statement/{symbol} <a name="0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/financial-statements/{symbol} <a name="0x5357de3fabc940fb28fc293e5ceb8b818b5a2ce0bbe4c891026893f28f682366"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5357de3fabc940fb28fc293e5ceb8b818b5a2ce0bbe4c891026893f28f682366

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
datatype		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/financial-reports-dates <a name="0x36c15ab2247a81e28aa6fa2c10222ae8ce840904b5857c27753e68ab4dc9b5c5"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x36c15ab2247a81e28aa6fa2c10222ae8ce840904b5857c27753e68ab4dc9b5c5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/financial-reports-json <a name="0x0449d269e3c08f92abd5120dee267a777b1a0ae200abb3324ef2d5c5abc36162"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0449d269e3c08f92abd5120dee267a777b1a0ae200abb3324ef2d5c5abc36162

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
symbol		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/shares_float <a name="0x2e8f5a7acb9c4ac1cb2e500ac09455b77917fa65770c79a83db4c71fac60642d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2e8f5a7acb9c4ac1cb2e500ac09455b77917fa65770c79a83db4c71fac60642d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/shares_float/all <a name="0x58baa0dcac6924c4129f64a64c1b414c5a9a3a429e9f1b828848bb75a884510f"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x58baa0dcac6924c4129f64a64c1b414c5a9a3a429e9f1b828848bb75a884510f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/rss_feed <a name="0x4f4516e2cc48556fcba36e80eab3baed1e0a012d237c52befce6099e7cafe084"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4f4516e2cc48556fcba36e80eab3baed1e0a012d237c52befce6099e7cafe084

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
datatype		// Parameter Description...
from		// Parameter Description...
isDone		// Parameter Description...
limit		// Parameter Description...
to		// Parameter Description...
type		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/earning_call_transcript/{symbol} <a name="0x338180d1ef637856e0c66e35fb6540272b4f6870f2a55eec7ac93915eb5644ee"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x338180d1ef637856e0c66e35fb6540272b4f6870f2a55eec7ac93915eb5644ee

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
quarter		// Parameter Description...
year		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/batch_earning_call_transcript/{symbol} <a name="0x428748e780ae4ecf326c72f3fa469dc3508f96761ebaad0badc8cc588f8caea4"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x428748e780ae4ecf326c72f3fa469dc3508f96761ebaad0badc8cc588f8caea4

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
year		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/sec_filings/{symbol} <a name="0x784f5e8f14ac4e7131d0be44d8d6f948151764dd882b3600c6ad09ff02827722"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x784f5e8f14ac4e7131d0be44d8d6f948151764dd882b3600c6ad09ff02827722

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
type		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/rss_feed_8k <a name="0x7b60cd4f871c5219dc44e895b643bff03f7828a11f7bf3d063a858261fbcb5af"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7b60cd4f871c5219dc44e895b643bff03f7828a11f7bf3d063a858261fbcb5af

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
hasFinancial		// Parameter Description...
limit		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/ratios/{symbol} <a name="0x3b6ef560e4820b136eae432f33ca3247a0120927a1c7649fdc86b83f1dfeafa6"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3b6ef560e4820b136eae432f33ca3247a0120927a1c7649fdc86b83f1dfeafa6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/enterprise-values/{symbol} <a name="0xcc40af84f4216d7f4802d01cf4edac5fdfd9c685d9ddb1c63812aba2e70a61bf"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xcc40af84f4216d7f4802d01cf4edac5fdfd9c685d9ddb1c63812aba2e70a61bf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/income-statement-growth/{symbol} <a name="0xcc9a4ba1acb4056107ff03d05f42716f213c0b39af2137ab96242697a8b75a0f"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xcc9a4ba1acb4056107ff03d05f42716f213c0b39af2137ab96242697a8b75a0f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/balance-sheet-statement-growth/{symbol} <a name="0x084237603893e0c1d750eeda13260670f1ed2086024a8992c4622f73a412a8ef"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x084237603893e0c1d750eeda13260670f1ed2086024a8992c4622f73a412a8ef

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cash-flow-statement-growth/{symbol} <a name="0x294354ba847915b9be24ca5cf40aaa58cf1134adfa403d6129ce3f557e48a4a2"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x294354ba847915b9be24ca5cf40aaa58cf1134adfa403d6129ce3f557e48a4a2

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/key-metrics-ttm/{symbol} <a name="0x78afea8f5f354b024be361d2dde7ed208ae59f77f4c929e01254a1d4a32de2db"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x78afea8f5f354b024be361d2dde7ed208ae59f77f4c929e01254a1d4a32de2db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/key-metrics/{symbol} <a name="0xf5cee6b7e8a2d3035ef040942dcb9b16de0b6e356929eac760fec061c9c05ddf"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xf5cee6b7e8a2d3035ef040942dcb9b16de0b6e356929eac760fec061c9c05ddf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/financial-growth/{symbol} <a name="0xe608cdc0dbe1ee349249994d0b399ee0c250cf6e6c1a7a2ed9ab1a8ee0466277"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe608cdc0dbe1ee349249994d0b399ee0c250cf6e6c1a7a2ed9ab1a8ee0466277

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/rating/{symbol} <a name="0x45ee30f97f68b834762fb16b9f10f59e211bbe70b314800f7330015b564a3db6"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x45ee30f97f68b834762fb16b9f10f59e211bbe70b314800f7330015b564a3db6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-rating/{symbol} <a name="0xdfdb5312feb8f42f3651623b2af176f393ec7fb14b137f35b78d44ddb80c1973"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdfdb5312feb8f42f3651623b2af176f393ec7fb14b137f35b78d44ddb80c1973

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/discounted-cash-flow/{symbol} <a name="0x60a393d432d929e97bd7636109af2a75d858fd1ef5473eb8b8d37cfd3140f224"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x60a393d432d929e97bd7636109af2a75d858fd1ef5473eb8b8d37cfd3140f224

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-discounted-cash-flow-statement/{symbol} <a name="0x79a8fd3caa539331b18e87fffc4f5d05d16085910c1fa79d785d36d27374838c"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x79a8fd3caa539331b18e87fffc4f5d05d16085910c1fa79d785d36d27374838c

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-daily-discounted-cash-flow/{symbol} <a name="0xaca8caf67075f059cb66f19d44c2efa598086cfb8a081159cbb07806324ff241"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xaca8caf67075f059cb66f19d44c2efa598086cfb8a081159cbb07806324ff241

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/earning_calendar <a name="0x26d554accbfcbae6987dfa5b9f02b7bd3cbe887b23190bcc06bb022f1e494f0f"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x26d554accbfcbae6987dfa5b9f02b7bd3cbe887b23190bcc06bb022f1e494f0f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical/earning_calendar/{symbol} <a name="0x47a1d9b10a83651bc37758429bdff597fcd25c3c49f9e5591c54d1a2fdd70abc"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x47a1d9b10a83651bc37758429bdff597fcd25c3c49f9e5591c54d1a2fdd70abc

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/ipo_calendar <a name="0x4662cd94cfb11798eef704fdc211ee489693e45bb5f2a15e5b7b2b64ac106107"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4662cd94cfb11798eef704fdc211ee489693e45bb5f2a15e5b7b2b64ac106107

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/stock_split_calendar <a name="0xe6b64232543e0f8ec44b06b794ea9bac1f30e3194446b705f69d583505b2d887"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe6b64232543e0f8ec44b06b794ea9bac1f30e3194446b705f69d583505b2d887

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/stock_dividend_calendar <a name="0x7c82f8fd59f261f612e76210e69ae29128bbfde68acdcc910013a2bf3bb8ecc9"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7c82f8fd59f261f612e76210e69ae29128bbfde68acdcc910013a2bf3bb8ecc9

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/economic_calendar <a name="0xa8cd3d01e5a6ede542df42226fd8192a228f59c5455965de48bc1f2f8cded14d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa8cd3d01e5a6ede542df42226fd8192a228f59c5455965de48bc1f2f8cded14d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/search <a name="0xfd6eb01969f7e3a2904382229564636e4423a398acfe40f182c543737b27846b"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xfd6eb01969f7e3a2904382229564636e4423a398acfe40f182c543737b27846b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
exchange		// Parameter Description...
limit		// Parameter Description...
query		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/search-ticker <a name="0x4c3bc218efd10bfa620732e05c94616d8ea50413781960d3a917af71c4e79eab"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4c3bc218efd10bfa620732e05c94616d8ea50413781960d3a917af71c4e79eab

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
exchange		// Parameter Description...
limit		// Parameter Description...
query		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/stock-screener <a name="0x2b39fd9c23518233cd8285813b3ee47cd3f58765ef7d6e39573575825e6f4d35"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2b39fd9c23518233cd8285813b3ee47cd3f58765ef7d6e39573575825e6f4d35

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
betaMoreThan		// Parameter Description...
country		// Parameter Description...
dividendMoreThan		// Parameter Description...
exchange		// Parameter Description...
industry		// Parameter Description...
limit		// Parameter Description...
marketCapLowerThan		// Parameter Description...
marketCapMoreThan		// Parameter Description...
priceMoreThan		// Parameter Description...
sector		// Parameter Description...
volumeMoreThan		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/get-all-countries <a name="0x55de15995bf3086d8eb2e95be132c8e8fc683e7360f8f0d464aecc46a7ff38e0"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x55de15995bf3086d8eb2e95be132c8e8fc683e7360f8f0d464aecc46a7ff38e0

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/profile/{symbol} <a name="0xc77379b6803bfb6a3bc8c17652916281c6c687fc9e7d50a6f4c9e6ba56715dca"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc77379b6803bfb6a3bc8c17652916281c6c687fc9e7d50a6f4c9e6ba56715dca

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/key-executives/{symbol} <a name="0x9d02f28e45306d8729c95a8e38222ee2f6621e6a383475bb5845e4237bf942df"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x9d02f28e45306d8729c95a8e38222ee2f6621e6a383475bb5845e4237bf942df

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/market-capitalization/{symbol} <a name="0x6f2a3e7e2d263d737fc8765fd1fefba6e0b011b1430be1a57c424c5b953c6dc5"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6f2a3e7e2d263d737fc8765fd1fefba6e0b011b1430be1a57c424c5b953c6dc5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-market-capitalization/{symbol} <a name="0xeeb404e11f70d5fd43f2ae5c8f04ba20ed33e58f55617c35e1035d5064288d98"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xeeb404e11f70d5fd43f2ae5c8f04ba20ed33e58f55617c35e1035d5064288d98

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/company-outlook <a name="0x042989ba15709efe8105bfc178cc304e2e57b976cd3bcef0ac7cc60aa82f55b8"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x042989ba15709efe8105bfc178cc304e2e57b976cd3bcef0ac7cc60aa82f55b8

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/stock_peers <a name="0x94e8db923ed3a09bb3532dc1a6de3e904e90eb4b933757a1e2c427e07fea61bf"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x94e8db923ed3a09bb3532dc1a6de3e904e90eb4b933757a1e2c427e07fea61bf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/is-the-market-open <a name="0x0687de301cca188f078be3bbdb4be2f13373800316ae71cd9dace80858931b23"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0687de301cca188f078be3bbdb4be2f13373800316ae71cd9dace80858931b23

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/delisted-companies <a name="0x59ae66e39460b5e996adc11a1f1073a9dbffdf1eeb5341ca0a0af2e550d1cfea"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x59ae66e39460b5e996adc11a1f1073a9dbffdf1eeb5341ca0a0af2e550d1cfea

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/articles <a name="0x92499117c90f908d061895ff836caecb00e58ee0f471e40a38032f2f68a053bd"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x92499117c90f908d061895ff836caecb00e58ee0f471e40a38032f2f68a053bd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
page		// Parameter Description...
size		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/stock_news <a name="0x3cc9821b6a5f6b8bdd6ca8c5e6be9465706f94a8c881dcf4100f360626309a9e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3cc9821b6a5f6b8bdd6ca8c5e6be9465706f94a8c881dcf4100f360626309a9e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
tickers		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/press-releases/{symbol} <a name="0xc34888ff56805321a7c2b650065753485a355c1ffc7e155d493dbe9f8278b30d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc34888ff56805321a7c2b650065753485a355c1ffc7e155d493dbe9f8278b30d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/sector_price_earning_ratio <a name="0xea1299fa30035cf94bb01f94d040926e7966747934d394a4f91a3ae207e27813"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xea1299fa30035cf94bb01f94d040926e7966747934d394a4f91a3ae207e27813

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date		// Parameter Description...
exchange		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/industry_price_earning_ratio <a name="0x2717b835e234a48fc40947bad9278af346f58e30661175d63b53a0d6803bd8ce"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2717b835e234a48fc40947bad9278af346f58e30661175d63b53a0d6803bd8ce

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date		// Parameter Description...
exchange		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/sectors-performance <a name="0x1dac39aab45ce2908ef9f8885c7f368c52cce25633f41c42cceb6ae122a6c408"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x1dac39aab45ce2908ef9f8885c7f368c52cce25633f41c42cceb6ae122a6c408

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-sectors-performance <a name="0xda2e2fbf813778cd01bcf722b2b5871720793e8e0954043185ef620395e14d0d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xda2e2fbf813778cd01bcf722b2b5871720793e8e0954043185ef620395e14d0d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/gainers <a name="0x0eb26c96bd29e0a63458f325fcf1c61cbd8fe4cca4efa29581dd32f8e8687983"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0eb26c96bd29e0a63458f325fcf1c61cbd8fe4cca4efa29581dd32f8e8687983

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/losers <a name="0x392ec92746669d2a0d28730830d9bf1e624d6ab5d5738b80214c80fea4dbbb65"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x392ec92746669d2a0d28730830d9bf1e624d6ab5d5738b80214c80fea4dbbb65

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/actives <a name="0xebf4654d7c1a9224bd1b1ae7a27e0ea9b70f5e16b115d6ecc7803ed46e96b8ab"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xebf4654d7c1a9224bd1b1ae7a27e0ea9b70f5e16b115d6ecc7803ed46e96b8ab

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/standard_industrial_classification <a name="0xc34c5cca5d18714d71f6a77b6f35b0a1dd3d018bf9df9aaadada6d84bb5b380a"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc34c5cca5d18714d71f6a77b6f35b0a1dd3d018bf9df9aaadada6d84bb5b380a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
cik		// Parameter Description...
sicCode		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/standard_industrial_classification/all <a name="0xbac4d7a5a482602d0a6dddf13b8ec593e7fd554121d102810b930902a148e845"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xbac4d7a5a482602d0a6dddf13b8ec593e7fd554121d102810b930902a148e845

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/standard_industrial_classification_list <a name="0xe03fe1ca41560488cd4a10dbbbbfa25c980f5e323895d987a3f64557f7f8ffc2"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe03fe1ca41560488cd4a10dbbbbfa25c980f5e323895d987a3f64557f7f8ffc2

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
industryTitle		// Parameter Description...
sicCode		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/commitment_of_traders_report/list <a name="0x6b60d1199f4ec6b2488b63e4d39fa211753ce6f9b5c4f8897b21ec1ea8487f6e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6b60d1199f4ec6b2488b63e4d39fa211753ce6f9b5c4f8897b21ec1ea8487f6e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/commitment_of_traders_report <a name="0xc3677a186218cf337748b18ff482711c3554882872ebab1067e04c2007c97432"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc3677a186218cf337748b18ff482711c3554882872ebab1067e04c2007c97432

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/commitment_of_traders_report/{symbol} <a name="0x64864439ea51c270825cdd137ac2473f3aa1530d213af05400ca9869c8726fca"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x64864439ea51c270825cdd137ac2473f3aa1530d213af05400ca9869c8726fca

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/commitment_of_traders_report_analysis <a name="0x7253ff38494d9dd0e61427a1962dc8bf78625d68eac17d154f028481822bb81d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7253ff38494d9dd0e61427a1962dc8bf78625d68eac17d154f028481822bb81d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/commitment_of_traders_report_analysis/{symbol} <a name="0xde76a38d22c137626be9db37420ed7e5e6f9fadebd2a0c83fc0434d4723331f3"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xde76a38d22c137626be9db37420ed7e5e6f9fadebd2a0c83fc0434d4723331f3

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/social-sentiment <a name="0x6d3844f911ef24504d3fd4096923dbe90043c3c8cc8ecc020dd1ba1731422531"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6d3844f911ef24504d3fd4096923dbe90043c3c8cc8ecc020dd1ba1731422531

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/grade/{symbol} <a name="0xc722594cd6883e15aa8929123f66ce0f4102c5869d23db8479c08b171095ce6e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc722594cd6883e15aa8929123f66ce0f4102c5869d23db8479c08b171095ce6e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/earnings-surprises/{symbol} <a name="0x5def20718185062e609800c5edc04770a490b4e41035ec69112b4b368420ef8a"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5def20718185062e609800c5edc04770a490b4e41035ec69112b4b368420ef8a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/analyst-estimates/{symbol} <a name="0x4e12bccc65fefc1c8e7c1dd36cb5b71264e89be188c28a5f1cf52c0617566e9d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4e12bccc65fefc1c8e7c1dd36cb5b71264e89be188c28a5f1cf52c0617566e9d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
period		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/insider-trading <a name="0xe24dec2fddb301e74714049e94f8f2f369c407973e5a65909cc91fa8b30e16b9"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe24dec2fddb301e74714049e94f8f2f369c407973e5a65909cc91fa8b30e16b9

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
companyCik		// Parameter Description...
limit		// Parameter Description...
reportingCik		// Parameter Description...
transactionType		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/insider-trading-transaction-type <a name="0x5bc8d1cfe63be647e00e0ec18684e79331503d69aa4a61c44b9154a12dc15eaa"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5bc8d1cfe63be647e00e0ec18684e79331503d69aa4a61c44b9154a12dc15eaa

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/mapper-cik-name <a name="0x38a978540e00dd030c05a16e1937f905e5354ba288cdb9db941e3be9efa4e166"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x38a978540e00dd030c05a16e1937f905e5354ba288cdb9db941e3be9efa4e166

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
name		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/mapper-cik-company/{symbol} <a name="0xf911c7a034d480cd9b2a977f8b5c982344ebddc8d0fa223e289b7f97ccae2ccd"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xf911c7a034d480cd9b2a977f8b5c982344ebddc8d0fa223e289b7f97ccae2ccd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/insider-trading-rss-feed <a name="0xc4ab4b1e6c29ef28bc775f115d5eb1662915edbd1b5e03742698ef023df6c40b"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc4ab4b1e6c29ef28bc775f115d5eb1662915edbd1b5e03742698ef023df6c40b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/fail_to_deliver <a name="0x3d07a30ef908c9a1fc5f511ac284f3b6196f167cee678971e6cf3e626dad8bfa"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3d07a30ef908c9a1fc5f511ac284f3b6196f167cee678971e6cf3e626dad8bfa

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quote/{symbol} <a name="0x057200614b55d7def35dd8cab6a7c86e64387942310b79d36726bc8610db0f06"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x057200614b55d7def35dd8cab6a7c86e64387942310b79d36726bc8610db0f06

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quote-short/{symbol} <a name="0xc5cc0fb33749af723052eaf3037a3c9d6e036e707c0d30c071927f93d2f575c7"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc5cc0fb33749af723052eaf3037a3c9d6e036e707c0d30c071927f93d2f575c7

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/{exchange} <a name="0xd5deebc79e31c9eea9506ac8086c96d82793d1b17509b4c9621a2b038808c3d5"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xd5deebc79e31c9eea9506ac8086c96d82793d1b17509b4c9621a2b038808c3d5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
exchange		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/1min/{symbol} <a name="0xd00d92abb1348429ed9b5ab9c41646ea21a8618b9ff7b38b41e3cc6b894e06f3"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xd00d92abb1348429ed9b5ab9c41646ea21a8618b9ff7b38b41e3cc6b894e06f3

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/5min/{symbol} <a name="0xdef0f6d6d8416a408fed0a3ca76432403f17d33bfbd6f80634aefd7bb003ad4c"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdef0f6d6d8416a408fed0a3ca76432403f17d33bfbd6f80634aefd7bb003ad4c

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/15min/{symbol} <a name="0x0bffe32171a75d9244c3146dadb0ccbc313766740a2e674342e1d0173b97b2d4"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0bffe32171a75d9244c3146dadb0ccbc313766740a2e674342e1d0173b97b2d4

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/30min/{symbol} <a name="0x87411cfc1413922e1ed9872ae91441c311c465131de8f7bb968ff3e07ca2c461"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x87411cfc1413922e1ed9872ae91441c311c465131de8f7bb968ff3e07ca2c461

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/1hour/{symbol} <a name="0x9c7120fe43466e8c74a08a577410e7f0450b1b1b7ecaf6b5ffebd58160ef28d6"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x9c7120fe43466e8c74a08a577410e7f0450b1b1b7ecaf6b5ffebd58160ef28d6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-chart/4hour/{symbol} <a name="0xfa27ed50687decece1b374fc0048a43aeb2f40f000e648294a7ebbba63e49f5e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xfa27ed50687decece1b374fc0048a43aeb2f40f000e648294a7ebbba63e49f5e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-price-full/{symbol} <a name="0x3506b1d2fec15e1b4fa743bdf2e87bb592a74d6131b0726f1ecd82d670862c7e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3506b1d2fec15e1b4fa743bdf2e87bb592a74d6131b0726f1ecd82d670862c7e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from		// Parameter Description...
symbol		// Parameter Description...
timeseries		// Parameter Description...
to		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-price-full/stock_dividend/{symbol} <a name="0xc4a0e1e7933d8e11d6ff2026ec9ddacb28d73f82ed7e39b9dc3d0946831236b4"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc4a0e1e7933d8e11d6ff2026ec9ddacb28d73f82ed7e39b9dc3d0946831236b4

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical-price-full/stock_split/{symbol} <a name="0x17c4b82751150c3042b2d2787df65e32bca5ea28a3e24116f698a935946254a0"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x17c4b82751150c3042b2d2787df65e32bca5ea28a3e24116f698a935946254a0

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/historical-price-full/{symbol}/{date} <a name="0x07af2019d0b192e95dabd980d17a1aadb91395d42702d132f59895c04101764e"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x07af2019d0b192e95dabd980d17a1aadb91395d42702d132f59895c04101764e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
date		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/daily/{symbol} <a name="0x9fdc095046edee80824481c6527aa2d1248509801840c21c4028f418a8ea8ed9"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x9fdc095046edee80824481c6527aa2d1248509801840c21c4028f418a8ea8ed9

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/1min/{symbol} <a name="0xc35d0c0574bb39dc1f7b30a91d4e4045c96c42b9efc2ea962bd9a161d8f0471d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc35d0c0574bb39dc1f7b30a91d4e4045c96c42b9efc2ea962bd9a161d8f0471d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/5min/{symbol} <a name="0x551b14085dc94aa8f926691ffebeb7252a71f76287825a8845a28a80ba01f1fe"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x551b14085dc94aa8f926691ffebeb7252a71f76287825a8845a28a80ba01f1fe

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/15min/{symbol} <a name="0xbac1560f9593f92ee56971bb5fa1f052d60e81d516696c4fa9a62c5189b4e140"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xbac1560f9593f92ee56971bb5fa1f052d60e81d516696c4fa9a62c5189b4e140

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/30min/{symbol} <a name="0x7166e27d120b6f22a373dbc1f78e4f8031f97cd44075aff937daae043759c6e5"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7166e27d120b6f22a373dbc1f78e4f8031f97cd44075aff937daae043759c6e5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/1hour/{symbol} <a name="0xa5ca5579842315622d8a97b76a5436f28c2f56c78e2aaf154c7e197ff4ebe0fb"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa5ca5579842315622d8a97b76a5436f28c2f56c78e2aaf154c7e197ff4ebe0fb

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/technical_indicator/4hour/{symbol} <a name="0xcb3d37386174679d30df9495f9b8943179d0099ccec406a8f7b2112f81c291ee"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xcb3d37386174679d30df9495f9b8943179d0099ccec406a8f7b2112f81c291ee

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
type		// Parameter Description...
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/etf-holder/{symbol} <a name="0x5ef2e446a611145c6f07c6e0f9c5681ce7d0d12b053eeba5d9c2d14610a2b7cf"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5ef2e446a611145c6f07c6e0f9c5681ce7d0d12b053eeba5d9c2d14610a2b7cf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/institutional-holder/{symbol} <a name="0x5e81f9f5e7394932806d4b8a927ea8ddc59bc37bbb749709e9054b5a9fc25ce1"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5e81f9f5e7394932806d4b8a927ea8ddc59bc37bbb749709e9054b5a9fc25ce1

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/mutual-fund-holder/{symbol} <a name="0x8446caecb8e10224de7690d8226e54609a737f10114501a5209bc84a1739afc5"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x8446caecb8e10224de7690d8226e54609a737f10114501a5209bc84a1739afc5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/etf-sector-weightings/{symbol} <a name="0x3630cc47ae7370cc7044ff3edd1596921cf15b41985b14294dc307c29d6e3b17"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3630cc47ae7370cc7044ff3edd1596921cf15b41985b14294dc307c29d6e3b17

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/etf-country-weightings/{symbol} <a name="0x33dd26a76035242ee98ff311ed3af98aa40c5acf2ae68fbfcaeeb9ed2f1368f0"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x33dd26a76035242ee98ff311ed3af98aa40c5acf2ae68fbfcaeeb9ed2f1368f0

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cik_list <a name="0x37110d60e2a6eacffe7d79b8f1d3cffc201efd3f61aa01b3271fed1a0332f291"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x37110d60e2a6eacffe7d79b8f1d3cffc201efd3f61aa01b3271fed1a0332f291

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cik-search/{name} <a name="0x619de61a08a5cc62a8497acb70e72faf4f7bdef9e26329c0ca57828cb8a80ba4"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x619de61a08a5cc62a8497acb70e72faf4f7bdef9e26329c0ca57828cb8a80ba4

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
name		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cik/{cik} <a name="0xe3b3de879e009f37c8528e2cbd7e8d4397953d226c7cfd123ded3225850f27a7"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe3b3de879e009f37c8528e2cbd7e8d4397953d226c7cfd123ded3225850f27a7

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
cik		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/form-thirteen/{cik} <a name="0x8d8118e96a64feddf0fb9017787187247c2fb7f2492d843bb5ab0342a0dd596a"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x8d8118e96a64feddf0fb9017787187247c2fb7f2492d843bb5ab0342a0dd596a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date		// Parameter Description...
cik		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/form-thirteen-date/{cik} <a name="0xb523aa687cf76843842ca727225eab04053dfaad3f44c70d71d87fd0927d7e32"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xb523aa687cf76843842ca727225eab04053dfaad3f44c70d71d87fd0927d7e32

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
cik		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/cusip/{cik} <a name="0x4d4cc8d394727aa0d3e6fb21988e650e91c0ebcda2c8d2cb7206d5dc4bc3dc17"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4d4cc8d394727aa0d3e6fb21988e650e91c0ebcda2c8d2cb7206d5dc4bc3dc17

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
cik		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/stock/list <a name="0x666544755232226f2b550bd4923b46cbe113b2e431cc7e8c23aa5bdba238f7fb"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x666544755232226f2b550bd4923b46cbe113b2e431cc7e8c23aa5bdba238f7fb

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/available-traded/list <a name="0x7303a24685698095d04dd56361b7834e86931dd9f7fb714e7ec59c289d0bbea3"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7303a24685698095d04dd56361b7834e86931dd9f7fb714e7ec59c289d0bbea3

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/etf/list <a name="0x00133d5d7101daebc253c152632a05849d11a07fe2e84b05bd9d1e0b4af6d552"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x00133d5d7101daebc253c152632a05849d11a07fe2e84b05bd9d1e0b4af6d552

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/batch-request-end-of-day-prices <a name="0xe2275fb76d94a2eb09d126210c63cbb019d71545fd68d8e81533231046f5ea7a"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe2275fb76d94a2eb09d126210c63cbb019d71545fd68d8e81533231046f5ea7a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/income-statement-bulk <a name="0xac94bfb37085ab6b1b7eb4a98d26724cc06187a086ff3bef473f4458ee439cdd"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xac94bfb37085ab6b1b7eb4a98d26724cc06187a086ff3bef473f4458ee439cdd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/balance-sheet-statement-bulk <a name="0xa384fa151c7c37df43b2ff2d6d4826917020619eddc1e3189fc9466d6735bec0"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa384fa151c7c37df43b2ff2d6d4826917020619eddc1e3189fc9466d6735bec0

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/cash-flow-statement-bulk <a name="0x580da25ae71f4949fb50b296248250725e233a9e36b08d13d76e750e74c45dca"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x580da25ae71f4949fb50b296248250725e233a9e36b08d13d76e750e74c45dca

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/ratios-bulk <a name="0x57673de82ce3868af6195f0a77430aa7b0777ba7c5c2b0eb71db300440d1cd9f"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x57673de82ce3868af6195f0a77430aa7b0777ba7c5c2b0eb71db300440d1cd9f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/key-metrics-bulk <a name="0xdb78e185aa7dba83fd8928085083cd5ef658a01726e20b4be5c7911fd1f89b04"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdb78e185aa7dba83fd8928085083cd5ef658a01726e20b4be5c7911fd1f89b04

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
period		// Parameter Description...
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/earnings-surprises-bulk <a name="0xdc4284f0c390df12fdf19a3abae3a5bb528fb78b5103753adffb210dfa41d359"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdc4284f0c390df12fdf19a3abae3a5bb528fb78b5103753adffb210dfa41d359

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
year		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v4/profile/all <a name="0x39941ed918f7be6be8523c5786ee8ef399e094b7d310966da18e91a2acf32042"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x39941ed918f7be6be8523c5786ee8ef399e094b7d310966da18e91a2acf32042

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/index <a name="0x53810b6bd02e8c55cb9bc1bb73bbf57005ea8049a049a9656a8877d1cd131fb2"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x53810b6bd02e8c55cb9bc1bb73bbf57005ea8049a049a9656a8877d1cd131fb2

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quote/{index} <a name="0xba6fb29686df04532c934d47094d4161f5a1cd294c7041b0a7b03e3d7037e899"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xba6fb29686df04532c934d47094d4161f5a1cd294c7041b0a7b03e3d7037e899

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
index		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/sp500_constituent <a name="0x0086c9e5229d83dfd28ee90dfb681ca2405153e36fa8548a2c8efeba6a1372cf"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0086c9e5229d83dfd28ee90dfb681ca2405153e36fa8548a2c8efeba6a1372cf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```[Fixed Parameters](https://docs.api3.org/pre-alpha/airnode/specifications/ois.html#_5-3-fixedoperationparameters)

```solidity

```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical/sp500_constituent <a name="0xf0535c78caacd8cfa01bd5ab784deeff1a6b8b125267c2c6725cd8e4fa6a334b"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xf0535c78caacd8cfa01bd5ab784deeff1a6b8b125267c2c6725cd8e4fa6a334b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/nasdaq_constituent <a name="0x11bf4ecec2691ca58a89c76ad0b2d0bb1ac674dff3589ece923863ab8b082071"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x11bf4ecec2691ca58a89c76ad0b2d0bb1ac674dff3589ece923863ab8b082071

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```[Fixed Parameters](https://docs.api3.org/pre-alpha/airnode/specifications/ois.html#_5-3-fixedoperationparameters)

```solidity

```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/dowjones_constituent <a name="0x704e6c91c060c739593b0c5c9c5b0a6bf6f75f6e158ee52e561ab89e97d32955"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x704e6c91c060c739593b0c5c9c5b0a6bf6f75f6e158ee52e561ab89e97d32955

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```[Fixed Parameters](https://docs.api3.org/pre-alpha/airnode/specifications/ois.html#_5-3-fixedoperationparameters)

```solidity

```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/historical/dowjones_constituent <a name="0x05d201f310049da032a2f34e29bdfb3feee8195c69f347079321ad72063f8bcd"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x05d201f310049da032a2f34e29bdfb3feee8195c69f347079321ad72063f8bcd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-indexes <a name="0x2158b17f6d31a6170a437bc1beb48ae08d881094db07fd79af29ab70a7722607"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2158b17f6d31a6170a437bc1beb48ae08d881094db07fd79af29ab70a7722607

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-euronext <a name="0x56e465973b2067f14a41fe3f7b8b649d9375bbed49fa69ca75f8109649dcde8c"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x56e465973b2067f14a41fe3f7b8b649d9375bbed49fa69ca75f8109649dcde8c

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/euronext <a name="0x592362f7700ccf0b4d0ede614875dffe2ad89d3255971b0dc13ea2f0b3f512d8"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x592362f7700ccf0b4d0ede614875dffe2ad89d3255971b0dc13ea2f0b3f512d8

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-tsx <a name="0x4597f014d3e434ae9a7a6ecd01974dbfa8455074f461254fc4f85a7974f38133"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4597f014d3e434ae9a7a6ecd01974dbfa8455074f461254fc4f85a7974f38133

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/tsx <a name="0x6c2991676ba0993fbbf340e8f5e759d13fd9228865542000087261a72203b9d1"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6c2991676ba0993fbbf340e8f5e759d13fd9228865542000087261a72203b9d1

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/crypto <a name="0x94741d14f09d9de38d6735807f3d7d9bfc367ccd66a09aea0bd7747924125dd6"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x94741d14f09d9de38d6735807f3d7d9bfc367ccd66a09aea0bd7747924125dd6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-cryptocurrencies <a name="0x3812e035581bceddaef8eeb58da8e7829263966849236a8548eb722ef1200cac"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3812e035581bceddaef8eeb58da8e7829263966849236a8548eb722ef1200cac

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/fx <a name="0x757cd231f1360e7c11b93e6190bf333e1bebe1baaab430712c5ac5a6ac6c769f"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x757cd231f1360e7c11b93e6190bf333e1bebe1baaab430712c5ac5a6ac6c769f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/forex <a name="0xbfa94372a7570b36f07429fd80d3c872e4429677bf7d2aae8253d6735f933fa6"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xbfa94372a7570b36f07429fd80d3c872e4429677bf7d2aae8253d6735f933fa6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/fx/{pair} <a name="0xdd1ffa0cd57648ce9f4959b3ac63d791a80234531cf852196177702e0af2255a"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdd1ffa0cd57648ce9f4959b3ac63d791a80234531cf852196177702e0af2255a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
pair		// Parameter Description...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-forex-currency-pairs <a name="0x51dad5124d84a2a19618c33a7a49368a3bb9c972e7bedc5300315c9e69ecae61"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x51dad5124d84a2a19618c33a7a49368a3bb9c972e7bedc5300315c9e69ecae61

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-commodities <a name="0x40ac15c012581e2dce07187c589b19549e8c12429fd4b96f31b0d8ede5a1c6c3"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x40ac15c012581e2dce07187c589b19549e8c12429fd4b96f31b0d8ede5a1c6c3

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/commodity <a name="0xf0b910a9f0fbfad2bf7171390fcb407f0f4609bcf2d0b0984a5393aa2ac2daef"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xf0b910a9f0fbfad2bf7171390fcb407f0f4609bcf2d0b0984a5393aa2ac2daef

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-etfs <a name="0x9d55f88adb0b1d7bb63f638926153f6e8068c43c142a6eb14175d1cbb7843d55"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x9d55f88adb0b1d7bb63f638926153f6e8068c43c142a6eb14175d1cbb7843d55

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/etf <a name="0xc30478970247c62b2cbac7cf912008dcee51785e5527bee0a31d042e98f4b764"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc30478970247c62b2cbac7cf912008dcee51785e5527bee0a31d042e98f4b764

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/symbol/available-mutual-funds <a name="0x09fa92ec3dfd92f9edbb3c30fa07b311f436341036392d17422c556febc8578d"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x09fa92ec3dfd92f9edbb3c30fa07b311f436341036392d17422c556febc8578d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----
## GET /v3/quotes/mutual_fund <a name="0x78abc827d77172880ec0137590c4228197198670ddf78da142d4f0de45915773"></a>

{{ Describe the endpoint. Explain what it does and, if possible, deep link to the Web2 documentation. }}

**Web2 Docs:** {{ URL to endpoint documentation }}

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x78abc827d77172880ec0137590c4228197198670ddf78da142d4f0de45915773

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{ Add example response json here }
```
----