# How to use FinancialModelingPrep on Web3

> [Airnode](https://api3.org/airnode) API Documentation



Financial Modeling Prep is a  financial statements API, a free stock API and a historical quotes API. Find all companies financial reports, company stock prices in Real-time.<br />

We have real time stock price, we cover the fundamental data part of the stocks via providing income statement, balance sheet statement and cashflow statement quarterly and annually. <br />


**Home Page:** https://financialmodelingprep.com/developer <br />
**Web2 Docs:** https://financialmodelingprep.com/developer/docs

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

This endpoint allows you to get a list of all companies for which the API has financial statements.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statements-list

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

This endpoint returns company financial statements. SEC forms 10-K, 10-Q, and 8-K are used to obtain all financial statements for US companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-09-26",
    "symbol" : "AAPL",
    "reportedCurrency" : "USD",
    "fillingDate" : "2020-10-30",
    "acceptedDate" : "2020-10-29 18:06:25",
    "period" : "FY",
    "revenue" : 274515000000,
    "costOfRevenue" : 169559000000,
    "grossProfit" : 104956000000,
    "grossProfitRatio" : 0.38233247727810865,
    "researchAndDevelopmentExpenses" : 18752000000,
    "generalAndAdministrativeExpenses" : 19916000000,
    "sellingAndMarketingExpenses" : 0.0,
    "sellingGeneralAndAdministrativeExpenses" : 19916000000,
    "otherExpenses" : 0.0,
    "operatingExpenses" : 38668000000,
    "costAndExpenses" : 208227000000,
    "interestExpense" : 2873000000,
    "depreciationAndAmortization" : 11056000000,
    "ebitda" : 81020000000,
    "ebitdaratio" : 0.2951386991603373,
    "operatingIncome" : 66288000000,
    "operatingIncomeRatio" : 0.24147314354406862,
    "totalOtherIncomeExpensesNet" : -803000000,
    "incomeBeforeTax" : 67091000000,
    "incomeBeforeTaxRatio" : 0.24439830246070343,
    "incomeTaxExpense" : 9680000000,
    "netIncome" : 57411000000,
    "netIncomeRatio" : 0.20913611278072236,
    "eps" : 3.31,
    "epsdiluted" : 3.28,
    "weightedAverageShsOut" : 17352119000,
    "weightedAverageShsOutDil" : 17528214000,
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/0000320193-20-000096-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/aapl-20200926.htm"
  }, ...
]
```
----
## GET /v3/balance-sheet-statement/{symbol} <a name="0x593e38bae8a4e3e7a1b80a8c4b2e7363bdcdfc8434fa46a76fc49aeed6894950"></a>

This endpoint returns company financial statements. SEC forms 10-K, 10-Q, and 8-K are used to obtain all financial statements for US companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-free-api#Balance-Sheet-Statement

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x593e38bae8a4e3e7a1b80a8c4b2e7363bdcdfc8434fa46a76fc49aeed6894950

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-09-26",
    "symbol" : "AAPL",
    "reportedCurrency" : "USD",
    "fillingDate" : "2020-10-30",
    "acceptedDate" : "2020-10-29 18:06:25",
    "period" : "FY",
    "revenue" : 274515000000,
    "costOfRevenue" : 169559000000,
    "grossProfit" : 104956000000,
    "grossProfitRatio" : 0.38233247727810865,
    "researchAndDevelopmentExpenses" : 18752000000,
    "generalAndAdministrativeExpenses" : 19916000000,
    "sellingAndMarketingExpenses" : 0.0,
    "sellingGeneralAndAdministrativeExpenses" : 19916000000,
    "otherExpenses" : 0.0,
    "operatingExpenses" : 38668000000,
    "costAndExpenses" : 208227000000,
    "interestExpense" : 2873000000,
    "depreciationAndAmortization" : 11056000000,
    "ebitda" : 81020000000,
    "ebitdaratio" : 0.2951386991603373,
    "operatingIncome" : 66288000000,
    "operatingIncomeRatio" : 0.24147314354406862,
    "totalOtherIncomeExpensesNet" : -803000000,
    "incomeBeforeTax" : 67091000000,
    "incomeBeforeTaxRatio" : 0.24439830246070343,
    "incomeTaxExpense" : 9680000000,
    "netIncome" : 57411000000,
    "netIncomeRatio" : 0.20913611278072236,
    "eps" : 3.31,
    "epsdiluted" : 3.28,
    "weightedAverageShsOut" : 17352119000,
    "weightedAverageShsOutDil" : 17528214000,
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/0000320193-20-000096-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/aapl-20200926.htm"
  }, ...
]
```
----
## GET /v3/cash-flow-statement/{symbol} <a name="0xc93ced08b3801d834b9e0b46314deadd015923b59c3c9572f9b1109d76bde079"></a>

This endpoint returns company financial statements. SEC forms 10-K, 10-Q, and 8-K are used to obtain all financial statements for US companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-free-api#Cash-Flow-Statement

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc93ced08b3801d834b9e0b46314deadd015923b59c3c9572f9b1109d76bde079

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-09-26",
    "symbol" : "AAPL",
    "reportedCurrency" : "USD",
    "fillingDate" : "2020-10-30",
    "acceptedDate" : "2020-10-29 18:06:25",
    "period" : "FY",
    "revenue" : 274515000000,
    "costOfRevenue" : 169559000000,
    "grossProfit" : 104956000000,
    "grossProfitRatio" : 0.38233247727810865,
    "researchAndDevelopmentExpenses" : 18752000000,
    "generalAndAdministrativeExpenses" : 19916000000,
    "sellingAndMarketingExpenses" : 0.0,
    "sellingGeneralAndAdministrativeExpenses" : 19916000000,
    "otherExpenses" : 0.0,
    "operatingExpenses" : 38668000000,
    "costAndExpenses" : 208227000000,
    "interestExpense" : 2873000000,
    "depreciationAndAmortization" : 11056000000,
    "ebitda" : 81020000000,
    "ebitdaratio" : 0.2951386991603373,
    "operatingIncome" : 66288000000,
    "operatingIncomeRatio" : 0.24147314354406862,
    "totalOtherIncomeExpensesNet" : -803000000,
    "incomeBeforeTax" : 67091000000,
    "incomeBeforeTaxRatio" : 0.24439830246070343,
    "incomeTaxExpense" : 9680000000,
    "netIncome" : 57411000000,
    "netIncomeRatio" : 0.20913611278072236,
    "eps" : 3.31,
    "epsdiluted" : 3.28,
    "weightedAverageShsOut" : 17352119000,
    "weightedAverageShsOutDil" : 17528214000,
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/0000320193-20-000096-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/aapl-20200926.htm"
  }, ...
]
```
----
## GET /v3/income-statement-as-reported/{symbol} <a name="0xdb2edde7c0fcd0c68e6b44b7d4a94873d6320a48a7204606770b4b2ca88cb2b1"></a>

This endpoint returns reported financial values from company statements.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-as-reported#Income-Statements-as-reported

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdb2edde7c0fcd0c68e6b44b7d4a94873d6320a48a7204606770b4b2ca88cb2b1

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "date" : "2019-09-28",
  "symbol" : "AAPL",
  "period" : "FY",
  "costofgoodsandservicessold" : "161782000000.000000",
  "netincomeloss" : 5.5256E10,
  "researchanddevelopmentexpense" : 1.6217E10,
  "grossprofit" : 9.8392E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaociforsaleofsecuritiesnetoftax" : -2.5E7,
  "othercomprehensiveincomelossavailableforsalesecuritiesadjustmentnetoftax" : 3.827E9,
  "othercomprehensiveincomelossderivativesqualifyingashedgesnetoftax" : -6.38E8,
  "othercomprehensiveincomelossforeigncurrencytransactionandtranslationadjustmentnetoftax" : -4.08E8,
  "weightedaveragenumberofdilutedsharesoutstanding" : 4.648913E9,
  "weightedaveragenumberofsharesoutstandingbasic" : 4.617834E9,
  "othercomprehensiveincomeunrealizedgainlossonderivativesarisingduringperiodnetoftax" : -6.61E8,
  "operatingincomeloss" : 6.393E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaocionderivativesnetoftax" : -2.3E7,
  "incomelossfromcontinuingoperationsbeforeincometaxesextraordinaryitemsnoncontrollinginterest" : 6.5737E10,
  "earningspersharebasic" : 11.97,
  "incometaxexpensebenefit" : 1.0481E10,
  "revenuefromcontractwithcustomerexcludingassessedtax" : "260174000000.000000",
  "nonoperatingincomeexpense" : 1.807E9,
  "operatingexpenses" : 3.4462E10,
  "earningspersharediluted" : 11.89,
  "othercomprehensiveincomeunrealizedholdinggainlossonsecuritiesarisingduringperiodnetoftax" : 3.802E9,
  "sellinggeneralandadministrativeexpense" : 1.8245E10,
  "othercomprehensiveincomelossnetoftaxportionattributabletoparent" : 2.781E9,
  "comprehensiveincomenetoftax" : 5.8037E10
}
```
----
## GET /v3/balance-sheet-statement-as-reported/{symbol} <a name="0x8b36e15b108f18695210870aa5ef1ee0b6db8efd98637b04655afd02a08b2f50"></a>

This endpoint returns reported financial values from company statements.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-as-reported#Balance-Sheet-Statement-as-reported

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x8b36e15b108f18695210870aa5ef1ee0b6db8efd98637b04655afd02a08b2f50

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "date" : "2019-09-28",
  "symbol" : "AAPL",
  "period" : "FY",
  "costofgoodsandservicessold" : "161782000000.000000",
  "netincomeloss" : 5.5256E10,
  "researchanddevelopmentexpense" : 1.6217E10,
  "grossprofit" : 9.8392E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaociforsaleofsecuritiesnetoftax" : -2.5E7,
  "othercomprehensiveincomelossavailableforsalesecuritiesadjustmentnetoftax" : 3.827E9,
  "othercomprehensiveincomelossderivativesqualifyingashedgesnetoftax" : -6.38E8,
  "othercomprehensiveincomelossforeigncurrencytransactionandtranslationadjustmentnetoftax" : -4.08E8,
  "weightedaveragenumberofdilutedsharesoutstanding" : 4.648913E9,
  "weightedaveragenumberofsharesoutstandingbasic" : 4.617834E9,
  "othercomprehensiveincomeunrealizedgainlossonderivativesarisingduringperiodnetoftax" : -6.61E8,
  "operatingincomeloss" : 6.393E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaocionderivativesnetoftax" : -2.3E7,
  "incomelossfromcontinuingoperationsbeforeincometaxesextraordinaryitemsnoncontrollinginterest" : 6.5737E10,
  "earningspersharebasic" : 11.97,
  "incometaxexpensebenefit" : 1.0481E10,
  "revenuefromcontractwithcustomerexcludingassessedtax" : "260174000000.000000",
  "nonoperatingincomeexpense" : 1.807E9,
  "operatingexpenses" : 3.4462E10,
  "earningspersharediluted" : 11.89,
  "othercomprehensiveincomeunrealizedholdinggainlossonsecuritiesarisingduringperiodnetoftax" : 3.802E9,
  "sellinggeneralandadministrativeexpense" : 1.8245E10,
  "othercomprehensiveincomelossnetoftaxportionattributabletoparent" : 2.781E9,
  "comprehensiveincomenetoftax" : 5.8037E10
}
```
----
## GET /v3/cash-flow-statement-as-reported/{symbol} <a name="0xa9e134dca78a7301a94624dfc64a13baec0bb58a35d1318e47d2bffcecd4fdcd"></a>

This endpoint returns company financial statements. SEC forms 10-K, 10-Q, and 8-K are used to obtain all financial statements for US companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-free-api#Cash-Flow-Statement

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa9e134dca78a7301a94624dfc64a13baec0bb58a35d1318e47d2bffcecd4fdcd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-09-26",
    "symbol" : "AAPL",
    "reportedCurrency" : "USD",
    "fillingDate" : "2020-10-30",
    "acceptedDate" : "2020-10-29 18:06:25",
    "period" : "FY",
    "revenue" : 274515000000,
    "costOfRevenue" : 169559000000,
    "grossProfit" : 104956000000,
    "grossProfitRatio" : 0.38233247727810865,
    "researchAndDevelopmentExpenses" : 18752000000,
    "generalAndAdministrativeExpenses" : 19916000000,
    "sellingAndMarketingExpenses" : 0.0,
    "sellingGeneralAndAdministrativeExpenses" : 19916000000,
    "otherExpenses" : 0.0,
    "operatingExpenses" : 38668000000,
    "costAndExpenses" : 208227000000,
    "interestExpense" : 2873000000,
    "depreciationAndAmortization" : 11056000000,
    "ebitda" : 81020000000,
    "ebitdaratio" : 0.2951386991603373,
    "operatingIncome" : 66288000000,
    "operatingIncomeRatio" : 0.24147314354406862,
    "totalOtherIncomeExpensesNet" : -803000000,
    "incomeBeforeTax" : 67091000000,
    "incomeBeforeTaxRatio" : 0.24439830246070343,
    "incomeTaxExpense" : 9680000000,
    "netIncome" : 57411000000,
    "netIncomeRatio" : 0.20913611278072236,
    "eps" : 3.31,
    "epsdiluted" : 3.28,
    "weightedAverageShsOut" : 17352119000,
    "weightedAverageShsOutDil" : 17528214000,
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/0000320193-20-000096-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/aapl-20200926.htm"
  }, ...
]
```
----
## GET /v3/financial-statement-full-as-reported/{symbol} <a name="0x1b94493ceb218bdfe5c6c1fa25c09e8366d3964939473d9a898118fffb7c015b"></a>

This endpoint returns reported financial values from company statements

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statement-as-reported#Full-Financial-Statement-as-reported

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x1b94493ceb218bdfe5c6c1fa25c09e8366d3964939473d9a898118fffb7c015b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "date" : "2019-09-28",
  "symbol" : "AAPL",
  "period" : "FY",
  "costofgoodsandservicessold" : "161782000000.000000",
  "netincomeloss" : 5.5256E10,
  "researchanddevelopmentexpense" : 1.6217E10,
  "grossprofit" : 9.8392E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaociforsaleofsecuritiesnetoftax" : -2.5E7,
  "othercomprehensiveincomelossavailableforsalesecuritiesadjustmentnetoftax" : 3.827E9,
  "othercomprehensiveincomelossderivativesqualifyingashedgesnetoftax" : -6.38E8,
  "othercomprehensiveincomelossforeigncurrencytransactionandtranslationadjustmentnetoftax" : -4.08E8,
  "weightedaveragenumberofdilutedsharesoutstanding" : 4.648913E9,
  "weightedaveragenumberofsharesoutstandingbasic" : 4.617834E9,
  "othercomprehensiveincomeunrealizedgainlossonderivativesarisingduringperiodnetoftax" : -6.61E8,
  "operatingincomeloss" : 6.393E10,
  "othercomprehensiveincomelossreclassificationadjustmentfromaocionderivativesnetoftax" : -2.3E7,
  "incomelossfromcontinuingoperationsbeforeincometaxesextraordinaryitemsnoncontrollinginterest" : 6.5737E10,
  "earningspersharebasic" : 11.97,
  "incometaxexpensebenefit" : 1.0481E10,
  "revenuefromcontractwithcustomerexcludingassessedtax" : "260174000000.000000",
  "nonoperatingincomeexpense" : 1.807E9,
  "operatingexpenses" : 3.4462E10,
  "earningspersharediluted" : 11.89,
  "othercomprehensiveincomeunrealizedholdinggainlossonsecuritiesarisingduringperiodnetoftax" : 3.802E9,
  "sellinggeneralandadministrativeexpense" : 1.8245E10,
  "othercomprehensiveincomelossnetoftaxportionattributabletoparent" : 2.781E9,
  "comprehensiveincomenetoftax" : 5.8037E10
}
```
----
## GET /v3/income-statement/{symbol} <a name="0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db"></a>

Financial statement reports, such as the income statement, balance sheet statement, and cash flow statement, are available.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/international-filings

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3e60ef161562c598d9beaf07a3eb49681695fb1a2598991e6dfbfe2e52f7d9db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
datatype : csv
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-10-31",
    "symbol" : "RY.TO",
    "reportedCurrency" : "CAD",
    "fillingDate" : "2020-10-31",
    "acceptedDate" : "2020-10-31",
    "period" : "FY",
    "revenue" : 47104000000,
    "costOfRevenue" : 0.0,
    "grossProfit" : 0.0,
    "grossProfitRatio" : 0.0,
    "researchAndDevelopmentExpenses" : 0.0,
    "generalAndAdministrativeExpenses" : 19924000000,
    "sellingAndMarketingExpenses" : 0.0,
    "sellingGeneralAndAdministrativeExpenses" : 0.0,
    "otherExpenses" : 0.0,
    "operatingExpenses" : 0.0,
    "costAndExpenses" : 0.0,
    "interestExpense" : 14048000000,
    "depreciationAndAmortization" : 1273000000,
    "ebitda" : 0.0,
    "ebitdaratio" : 0.0,
    "operatingIncome" : 0.0,
    "operatingIncomeRatio" : 0.0,
    "totalOtherIncomeExpensesNet" : 0.0,
    "incomeBeforeTax" : 14389000000,
    "incomeBeforeTaxRatio" : 0.305472995923913,
    "incomeTaxExpense" : 2952000000,
    "netIncome" : 11432000000,
    "netIncomeRatio" : 0.24269701086956522,
    "eps" : 7.9677776159255185,
    "epsdiluted" : 7.9677776159255185,
    "weightedAverageShsOut" : 1434779000,
    "weightedAverageShsOutDil" : 1434779000,
    "link" : "https://www.sedar.com/ModifyCompanyDocumentSearchForm.do?lang=EN&company_search=Royal Bank of Canada&document_selection=0&industry_group=A&FromDate=13&FromMonth=05&FromYear=2000&ToDate=13&ToMonth=11&ToYear=2020&Variable=Issuer",


    "finalLink" : "https://www.sedar.com/ModifyCompanyDocumentSearchForm.do?lang=EN&company_search=Royal Bank of Canada&document_selection=0&industry_group=A&FromDate=13&FromMonth=05&FromYear=2000&ToDate=13&ToMonth=11&ToYear=2020&Variable=Issuer"
  }, ...
]
```
----
## GET /v3/financial-statements/{symbol} <a name="0x5357de3fabc940fb28fc293e5ceb8b818b5a2ce0bbe4c891026893f28f682366"></a>

You can use this endpoint to download all financial statements of a company in one zip file. It contains XLSX files with all of the company's financial statements.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financials-zip

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5357de3fabc940fb28fc293e5ceb8b818b5a2ce0bbe4c891026893f28f682366

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
datatype : zip
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

----
## GET /v4/financial-reports-dates <a name="0x36c15ab2247a81e28aa6fa2c10222ae8ce840904b5857c27753e68ab4dc9b5c5"></a>

The endpoint returns all statements from the company that include links to the JSON and XLSX versions of the statement.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/list-dates-links

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x36c15ab2247a81e28aa6fa2c10222ae8ce840904b5857c27753e68ab4dc9b5c5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "symbol" : "AAPL",
    "date" : "2020",
    "period" : "FY",
    "linkXlsx" : "https://financialmodelingprep.com/api/v4/financial-reports-xlsx?symbol=AAPL&year=2020&period=FY&apikey=YOUR_API_KEY",
    "linkJson" : "https://financialmodelingprep.com/api/v4/financial-reports-json?symbol=AAPL&year=2020&period=FY&apikey=YOUR_API_KEY"
  }, {
    "symbol" : "AAPL",
    "date" : "2019",
    "period" : "FY",
    "linkXlsx" : "https://financialmodelingprep.com/api/v4/financial-reports-xlsx?symbol=AAPL&year=2019&period=FY&apikey=YOUR_API_KEY",
    "linkJson" : "https://financialmodelingprep.com/api/v4/financial-reports-json?symbol=AAPL&year=2019&period=FY&apikey=YOUR_API_KEY"
  }, {
    "symbol" : "AAPL",
    "date" : "2018",
    "period" : "FY",
    "linkXlsx" : "https://financialmodelingprep.com/api/v4/financial-reports-xlsx?symbol=AAPL&year=2018&period=FY&apikey=YOUR_API_KEY",
    "linkJson" : "https://financialmodelingprep.com/api/v4/financial-reports-json?symbol=AAPL&year=2018&period=FY&apikey=YOUR_API_KEY"
  }, ...
]
```
----
## GET /v4/financial-reports-json <a name="0x0449d269e3c08f92abd5120dee267a777b1a0ae200abb3324ef2d5c5abc36162"></a>

Financial Data access Quarterly Earnings Reports and Annual Reports on Form 10-K.
The 10-K report is equivalent to the annual report that a company publish, the 10-Q is for the quartely report.
Each company has a different fiscal year, for example AAPL end its fiscal year in september.
This endpoint uses the calendar year.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/annual-report-form

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0449d269e3c08f92abd5120dee267a777b1a0ae200abb3324ef2d5c5abc36162

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
Year : Number
Period : FY | Q1 | Q2 | Q3 | Q4
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "period" : "FY",
  "year" : "2020",
  "Cover Page" : [ {
    "Cover Page - USD ($) shares in Thousands, $ in Millions" : [ "12 Months Ended" ]
  }, {
    "items" : [ "Sep. 26, 2020", "Oct. 16, 2020", "Mar. 27, 2020" ]
  }, {
    "Document Type" : [ "10-K" ]
  }, {
    "Document Annual Report" : [ "true" ]
  }, {
    "Document Period End Date" : [ "Sep. 26,2020" ]
  }, {
    "Document Transition Report" : [ "false" ]
  }, {
    "Entity File Number" : [ "001-36743" ]
  }, {
    "Entity Registrant Name" : [ "Apple Inc." ]
  }, {
    "Entity Incorporation, State or Country Code" : [ "CA" ]
  }, {
    "Entity Tax Identification Number" : [ "94-2404110" ]
  }, {
    "Entity Address, Address Line One" : [ "One Apple Park Way" ]
  }, {
    "Entity Address, City or Town" : [ "Cupertino" ]
  }, {
    "Entity Address, State or Province" : [ "CA" ]
  }, {
    "Entity Address, Postal Zip Code" : [ "95014" ]
  }, {
    "City Area Code" : [ "408" ]
  }, {
    "Local Phone Number" : [ "996-1010" ]
  }, ...
}
```
----
## GET /v4/shares_float <a name="0x2e8f5a7acb9c4ac1cb2e500ac09455b77917fa65770c79a83db4c71fac60642d"></a>

The number of shares available for trading is known as the float. The more floatable shares there are, the better. RSUs and remaining shares are used to calculate float shares.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/shares-float

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2e8f5a7acb9c4ac1cb2e500ac09455b77917fa65770c79a83db4c71fac60642d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "date" : "2021-06-03",
  "freeFloat" : 99.89818787368489,
  "floatShares" : 1.6670609616E10,
  "outstandingShares" : 1.6687599616E10,
  "source" : "https://www.sec.gov/Archives/edgar/data/320193/000032019321000056/aapl-20210327.htm"
} ]
```
----
## GET /v4/shares_float/all <a name="0x58baa0dcac6924c4129f64a64c1b414c5a9a3a429e9f1b828848bb75a884510f"></a>

All latest shares float available.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/shares-float

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x58baa0dcac6924c4129f64a64c1b414c5a9a3a429e9f1b828848bb75a884510f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "date" : "2021-06-03",
  "freeFloat" : 99.89818787368489,
  "floatShares" : 1.6670609616E10,
  "outstandingShares" : 1.6687599616E10,
  "source" : "https://www.sec.gov/Archives/edgar/data/320193/000032019321000056/aapl-20210327.htm"
} ]
```
----
## GET /v4/rss_feed <a name="0x4f4516e2cc48556fcba36e80eab3baed1e0a012d237c52befce6099e7cafe084"></a>

This endpoint returns specified SEC filings in JSON and CSV in real time. Examine the query parameters to see what kinds of filings it returns. You can also check if a filing was processed by us and specify a filing date range.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/sec-rss-feeds-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4f4516e2cc48556fcba36e80eab3baed1e0a012d237c52befce6099e7cafe084

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
datatype : csv
type : 10-Q | 10-K | 13F-HR | 6-K
from : YYYY-MM-DD
to : YYYY-MM-DD
isDone : true/false
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
    {
        "title" : "6-K - ONCOLYTICS BIOTECH INC (0001129928) (Filer)",
        "date" : "2020-05-29 16:48:22",
        "link" : "https://www.sec.gov/Archives/edgar/data/1129928/000112992820000034/0001129928-20-000034-index.htm",
        "cik" : "0001129928",
        "form_type" : "6-K",
        "ticker" : "ONCY"
    }, {
        "title" : "10-Q - BERKSHIRE HILLS BANCORP INC (0001108134) (Filer)",
        "date" : "2020-05-29 16:45:47",
        "link" : "https://www.sec.gov/Archives/edgar/data/1108134/000110813420000012/0001108134-20-000012-index.htm",
        "cik" : "0001108134",
        "form_type" : "10-Q",
        "ticker" : "BHLB"
    }, {
        "title" : "10-Q - URBAN ONE, INC. (0001041657) (Filer)",
        "date" : "2020-05-29 16:45:24",
        "link" : "https://www.sec.gov/Archives/edgar/data/1041657/000110465920067812/0001104659-20-067812-index.htm",
        "cik" : "0001041657",
        "form_type" : "10-Q",
        "ticker" : "UONEK"
    }, {
        "title" : "10-K - REMARK HOLDINGS, INC. (0001368365) (Filer)",
        "date" : "2020-05-29 16:42:40",
        "link" : "https://www.sec.gov/Archives/edgar/data/1368365/000136836520000028/0001368365-20-000028-index.htm",
        "cik" : "0001368365",
        "form_type" : "10-K",
        "ticker" : "MARK"
    }, {
        "title" : "10-K - SONO TEK CORP (0000806172) (Filer)",
        "date" : "2020-05-29 16:41:11",
        "link" : "https://www.sec.gov/Archives/edgar/data/806172/000117152020000252/0001171520-20-000252-index.htm",
        "cik" : "0000806172",
        "form_type" : "10-K",
        "ticker" : "SOTK"
  }
]
```
----
## GET /v3/earning_call_transcript/{symbol} <a name="0x338180d1ef637856e0c66e35fb6540272b4f6870f2a55eec7ac93915eb5644ee"></a>

One important report is the Earning Call Transcript.
You can find a real example on how to do NLP (Natural language processing) to analyze earning call transcripts and consequent ticker quarter growth to predict performance as compared to respective index.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/earning-call-transcript

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x338180d1ef637856e0c66e35fb6540272b4f6870f2a55eec7ac93915eb5644ee

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
Quarter : 1 | 2 | 3 | 4
Year : Number (ex: 2020)
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "quarter" : 3,
    "year" : 2020,
    "date" : "2020-07-31 17:00:00",
    "content" : "Operator - Good day, everyone. Welcome to the Apple Incorporated Third Quarter Fiscal Year 2020 Earnings Conference Call. Today's call is being recorded. At this time, for opening remarks and introductions, I would like to turn things over to Mr. Tejas Gala, Senior Manager, Corporate Finance and Investor Relations. Please go ahead, sir. Tejas Gala: Thank you. Good afternoon and thank you for joining us. Speaking first today is Apple's CEO, Tim Cook; and he'll be followed  by CFO, Luca Maestri. After that, we'll open the call to questions from analysts. Please note that some of the information you'll hear during our discussion today will consist of forward-looking statements including without limitation those regarding revenue, gross margin, operating expenses, other income and expense, taxes, capitalallocation, and future business outlook, including the potential impact of COVID-19 on the company's business and results of operations. Actual results or trends could differ materially from our forecast. For more information, please refer to the risk factors discussed in Apple's most recently filed periodic reports Form 10-K and Form 10-Q and the Form 8-K filed with the SEC today along with the associated press release. Apple assumes no obligation to update any forward-looking statements or information, which speak as of their respective dates. I'd now like to turn the call over to Tim for introductory remarks.Tim Cook: Thanks, Tejas. Good afternoon, everyone. Thanks for joining the call today. Before we begin, I joined the many millions across this country in mourning and memorialize Congressman John Lewis, who was laid to rest earlier today. We've lost a hero who walked among us, a leader in the truest sense who urged this country to aim higher and be better until the very end."
  }
]
```
----
## GET /v4/batch_earning_call_transcript/{symbol} <a name="0x428748e780ae4ecf326c72f3fa469dc3508f96761ebaad0badc8cc588f8caea4"></a>

Transcripts for symbol for specific year

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/earning-call-transcript

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x428748e780ae4ecf326c72f3fa469dc3508f96761ebaad0badc8cc588f8caea4

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Year : Number (ex: 2020)
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "quarter" : 3,
    "year" : 2020,
    "date" : "2020-07-31 17:00:00",
    "content" : "Operator - Good day, everyone. Welcome to the Apple Incorporated Third Quarter Fiscal Year 2020 Earnings Conference Call. Today's call is being recorded. At this time, for opening remarks and introductions, I would like to turn things over to Mr. Tejas Gala, Senior Manager, Corporate Finance and Investor Relations. Please go ahead, sir. Tejas Gala: Thank you. Good afternoon and thank you for joining us. Speaking first today is Apple's CEO, Tim Cook; and he'll be followed  by CFO, Luca Maestri. After that, we'll open the call to questions from analysts. Please note that some of the information you'll hear during our discussion today will consist of forward-looking statements including without limitation those regarding revenue, gross margin, operating expenses, other income and expense, taxes, capitalallocation, and future business outlook, including the potential impact of COVID-19 on the company's business and results of operations. Actual results or trends could differ materially from our forecast. For more information, please refer to the risk factors discussed in Apple's most recently filed periodic reports Form 10-K and Form 10-Q and the Form 8-K filed with the SEC today along with the associated press release. Apple assumes no obligation to update any forward-looking statements or information, which speak as of their respective dates. I'd now like to turn the call over to Tim for introductory remarks.Tim Cook: Thanks, Tejas. Good afternoon, everyone. Thanks for joining the call today. Before we begin, I joined the many millions across this country in mourning and memorialize Congressman John Lewis, who was laid to rest earlier today. We've lost a hero who walked among us, a leader in the truest sense who urged this country to aim higher and be better until the very end."
  }
]
```
----
## GET /v3/sec_filings/{symbol} <a name="0x784f5e8f14ac4e7131d0be44d8d6f948151764dd882b3600c6ad09ff02827722"></a>

It returns all SEC filings for a specific company. 10-K, 8-K, and all other types of filings are covered. Filings are a good way to keep track of what's going on inside a company, because every significant event has its own form type in the SEC.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/sec-filings

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x784f5e8f14ac4e7131d0be44d8d6f948151764dd882b3600c6ad09ff02827722

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
type : 10-Q | 10-K | 13F-HR | ...
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "fillingDate" : "2020-10-05 00:00:00",
    "acceptedDate" : "2020-10-05 18:33:56",
    "cik" : "0000320193",
    "type" : "4",
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000084/0000320193-20-000084-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000084/xslF345X03/wf-form4_160193720275669.xml"
  }, {
    "symbol" : "AAPL",
    "fillingDate" : "2020-10-05 00:00:00",
    "acceptedDate" : "2020-10-05 18:32:48",
    "cik" : "0000320193",
    "type" : "4",
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000083/0000320193-20-000083-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000083/xslF345X03/wf-form4_160193715587800.xml"
  }, {
    "symbol" : "AAPL",
    "fillingDate" : "2020-10-05 00:00:00",
    "acceptedDate" : "2020-10-05 18:30:48",
    "cik" : "0000320193",
    "type" : "4",
    "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000082/0000320193-20-000082-index.htm",
    "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000082/xslF345X03/wf-form4_160193701297920.xml"
  }, ...
]
```
----
## GET /v4/rss_feed_8k <a name="0x7b60cd4f871c5219dc44e895b643bff03f7828a11f7bf3d063a858261fbcb5af"></a>

If a publicly traded company experiences a significant event, it is usually required to file Form 8-K to notify the public and the Securities and Exchange Commission. There are a variety of situations that can necessitate the filing of an 8-K, and they frequently affect the stock price of the company.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/rss-feed-8k

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7b60cd4f871c5219dc44e895b643bff03f7828a11f7bf3d063a858261fbcb5af

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
      "title" : "8-K - Fusion Acquisition Corp. (0001807846) (Filer)",
      "date" : "2021-09-28 17:27:56",
      "symbol" : "FUSE-UN",
      "cik" : "0001807846",
      "link" : "https://www.sec.gov/Archives/edgar/data/1807846/000121390021050379/0001213900-21-050379-index.htm",
      "finalLink" : "",
      "process" : "False",
      "hasFinancials" : "False"
    }, {
      "title" : "8-K - Fusion Acquisition Corp. (0001807846) (Filer)",
      "date" : "2021-09-28 17:27:56",
      "symbol" : "FUSE",
      "cik" : "0001807846",
      "link" : "https://www.sec.gov/Archives/edgar/data/1807846/000121390021050379/0001213900-21-050379-index.htm",
      "finalLink" : "",
      "process" : "False",
      "hasFinancials" : "False"
    }, {
      "title" : "8-K - Fusion Acquisition Corp. (0001807846) (Filer)",
      "date" : "2021-09-28 17:27:56",
      "symbol" : "ML",
      "cik" : "0001807846",
      "link" : "https://www.sec.gov/Archives/edgar/data/1807846/000121390021050379/0001213900-21-050379-index.htm",
      "finalLink" : "",
      "process" : "False",
      "hasFinancials" : "False"
    }, ...
  ]
```
----
## GET /v3/ratios/{symbol} <a name="0x3b6ef560e4820b136eae432f33ca3247a0120927a1c7649fdc86b83f1dfeafa6"></a>

This endpoint returns financial ratios for companies to help in company analysis. This endpoint computes ratios for each financial statement presented by the company.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-ratio-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3b6ef560e4820b136eae432f33ca3247a0120927a1c7649fdc86b83f1dfeafa6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "date" : "2020-09-26",
    "period" : "FY",
    "currentRatio" : 1.3636044481554577,
    "quickRatio" : 1.2181949294064065,
    "cashRatio" : 0.36071049035979963,
    "daysOfSalesOutstanding" : 49.78753437881355,
    "daysOfInventoryOutstanding" : 8.741883356235881,
    "operatingCycle" : 58.52941773504943,
    "daysOfPayablesOutstanding" : 91.04818971567418,
    "cashConversionCycle" : -32.518771980624756,
    "grossProfitMargin" : 0.38233247727810865,
    "operatingProfitMargin" : 0.24147314354406862,
    "pretaxProfitMargin" : 0.24439830246070343,
    "netProfitMargin" : 0.20913611278072236,
    "effectiveTaxRate" : 0.14428164731484103,
    "returnOnAssets" : 0.1772557180259843,
    "returnOnEquity" : 0.8786635853012749,
    "returnOnCapitalEmployed" : 0.3033831282952548,
    "netIncomePerEBT" : 0.855718352685159,
    "ebtPerEbit" : 1.0121138064204682,
    "ebitPerRevenue" : 0.24147314354406862,
    "debtRatio" : 0.7982666847799239,
    "debtEquityRatio" : 3.957039440456695,
    "longTermDebtToCapitalization" : 0.6016060388034584,
    "totalDebtToCapitalization" : 0.6324623822247223,
    "interestCoverage" : 23.07274625826662,
    "cashFlowToDebtRatio" : 0.7175104059198122,
    "companyEquityMultiplier" : 4.957039440456695,
    "receivablesTurnover" : 7.331152356789959,
    "payablesTurnover" : 4.008866086627577,
    "inventoryTurnover" : 41.75301649839941,
    "fixedAssetTurnover" : 7.466545177609748,
    "assetTurnover" : 0.8475615027416885,
    "operatingCashFlowPerShare" : 4.649230448454163,
    "freeCashFlowPerShare" : 4.2280138811865,
    "cashPerShare" : 5.241031369137106,
    "payoutRatio" : 0.24526658654264863,
    "operatingCashFlowSalesRatio" : 0.2938782944465694,
    "freeCashFlowOperatingCashFlowRatio" : 0.909400798274537,
    "cashFlowCoverageRatios" : 0.7175104059198122,
    "shortTermCoverageRatios" : 5.8591037838623,
    "capitalExpenditureCoverageRatio" : -11.037624846080176,
    "dividendPaidAndCapexCoverageRatio" : 11.912876550502068,
    "dividendPayoutRatio" : 0.2452665865426486,
    "priceBookValueRatio" : 30.553901085207258,
    "priceToBookRatio" : 30.553901085207258,
    "priceToSalesRatio" : 7.272321523437178,
    "priceEarningsRatio" : 34.773150493918536,
    "priceToFreeCashFlowsRatio" : 27.211358863304806,
    "priceToOperatingCashFlowsRatio" : 24.74603147242429,
    "priceCashFlowRatio" : 24.74603147242429,
    "priceEarningsToGrowthRatio" : 3.2774378851354733,
    "priceSalesRatio" : 7.272321523437178,
    "dividendYield" : 0.007053332328502797,
    "enterpriseValueMultiple" : 26.773652035146323,
    "priceFairValue" : 30.553901085207258
  }, ...
]
```
----
## GET /v3/enterprise-values/{symbol} <a name="0xcc40af84f4216d7f4802d01cf4edac5fdfd9c685d9ddb1c63812aba2e70a61bf"></a>

Get a company enterprise value based on its financial statement, it is calculated from Market Value.
The enterprise Value is a proportion of an organization's absolute worth, frequently utilized as a more thorough option in contrast to value market capitalization.
Its estimation the market capitalization of an organization yet in addition present moment and long obligation just as any money on the organization's asset report.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/company-enterprise-value-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xcc40af84f4216d7f4802d01cf4edac5fdfd9c685d9ddb1c63812aba2e70a61bf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "enterpriseValues" : [ {
    "date" : "2018-09-29",
    "Stock Price" : "224.6375",
    "Number of Shares" : "4955377000.0",
    "Market Capitalization" : 1.1131635008375E12,
    "- Cash & Cash Equivalents" : 2.5913E10,
    "+ Total Debt" : 1.14483E11,
    "Enterprise Value" : 1.2017335008375E12
  }, {
    "date" : "2017-09-30",
    "Stock Price" : "149.7705",
    "Number of Shares" : "5217242000.0",
    "Market Capitalization" : 7.81388942961E11,
    "- Cash & Cash Equivalents" : 2.0289E10,
    "+ Total Debt" : 1.1568E11,
    "Enterprise Value" : 8.76779942961E11
  }, {
    "date" : "2016-09-24",
    "Stock Price" : "108.0101",
    "Number of Shares" : "5470820000.0",
    "Market Capitalization" : 5.90903815282E11,
    "- Cash & Cash Equivalents" : 2.0484E10,
    "+ Total Debt" : 8.7032E10,
    "Enterprise Value" : 6.57451815282E11
  }, {
    "date" : "2015-09-26",
    "Stock Price" : "105.3369",
    "Number of Shares" : "5753421000.0",
    "Market Capitalization" : 6.060475325349E11,
    "- Cash & Cash Equivalents" : 2.112E10,
    "+ Total Debt" : 6.4328E10,
    "Enterprise Value" : 6.492555325349E11
  }, {
    "date" : "2014-09-27",
    "Stock Price" : "92.2095",
    "Number of Shares" : "6085572000.0",
    "Market Capitalization" : 5.61147551334E11,
    "- Cash & Cash Equivalents" : 1.3844E10,
    "+ Total Debt" : 3.5295E10,
    "Enterprise Value" : 5.82598551334E1
  } ]
}
```
----
## GET /v3/income-statement-growth/{symbol} <a name="0xcc9a4ba1acb4056107ff03d05f42716f213c0b39af2137ab96242697a8b75a0f"></a>

This endpoint allows you to examine how the company has grown since its initial public offering. It provides details such as revenue growth and net income growth.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statements-growth

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xcc9a4ba1acb4056107ff03d05f42716f213c0b39af2137ab96242697a8b75a0f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
period : annual | quarter
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "date" : "2019-09-28",
    "symbol" : "AAPL",
    "period" : "FY",
    "growthRevenue" : -0.0204107758052674178,
    "growthCostOfRevenue" : -0.0120545201397200714,
    "growthGrossProfit" : -0.0338475436718742306,
    "growthGrossProfitRatio" : -0.0137154213078027384,
    "growthResearchAndDevelopmentExpenses" : 0.139154256813711713,
    "growthGeneralAndAdministrativeExpenses" : 0.0921879676743490029,
    "growthSellingAndMarketingExpenses" : 0,
    "growthOtherExpenses" : 0,
    "growthOperatingExpenses" : 0.113797226980382013,
    "growthCostAndExpenses" : 0.00794567969717047476,
    "growthInterestExpense" : 0.103703703703703701,
    "growthDepreciationAndAmortization" : 0.150784187838209655,
    "growthEBITDA" : -0.0430879293011946773,
    "growthEBITDARatio" : -0.0231486655986487197,
    "growthOperatingIncome" : -0.0982820389855849214,
    "growthOperatingIncomeRatio" : -0.0794935191428786103,
    "growthTotalOtherIncomeExpensesNet" : -1.95691609977324266,
    "growthIncomeBeforeTax" : -0.0982949947190101952,
    "growthIncomeBeforeTaxRatio" : -0.0795040967033286694,
    "growthIncomeTaxExpense" : -0.117166442048517519,
    "growthNetIncome" : -0.0718113251919168111,
    "growthNetIncomeRatio" : -0.0524712012920381735,
    "growthEPS" : -0.0262266179034436608,
    "growthEPSDiluted" : -0.0262266179034436608,
    "growthWeightedAverageShsOut" : -0.0702376688188197512,
    "growthWeightedAverageShsOutDil" : -0.0702376688188197512
  }, ...
]
```
----
## GET /v3/balance-sheet-statement-growth/{symbol} <a name="0x084237603893e0c1d750eeda13260670f1ed2086024a8992c4622f73a412a8ef"></a>

Annual balance sheet growth.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statements-growth

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x084237603893e0c1d750eeda13260670f1ed2086024a8992c4622f73a412a8ef

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "date" : "2019-09-28",
    "symbol" : "AAPL",
    "period" : "FY",
    "growthRevenue" : -0.0204107758052674178,
    "growthCostOfRevenue" : -0.0120545201397200714,
    "growthGrossProfit" : -0.0338475436718742306,
    "growthGrossProfitRatio" : -0.0137154213078027384,
    "growthResearchAndDevelopmentExpenses" : 0.139154256813711713,
    "growthGeneralAndAdministrativeExpenses" : 0.0921879676743490029,
    "growthSellingAndMarketingExpenses" : 0,
    "growthOtherExpenses" : 0,
    "growthOperatingExpenses" : 0.113797226980382013,
    "growthCostAndExpenses" : 0.00794567969717047476,
    "growthInterestExpense" : 0.103703703703703701,
    "growthDepreciationAndAmortization" : 0.150784187838209655,
    "growthEBITDA" : -0.0430879293011946773,
    "growthEBITDARatio" : -0.0231486655986487197,
    "growthOperatingIncome" : -0.0982820389855849214,
    "growthOperatingIncomeRatio" : -0.0794935191428786103,
    "growthTotalOtherIncomeExpensesNet" : -1.95691609977324266,
    "growthIncomeBeforeTax" : -0.0982949947190101952,
    "growthIncomeBeforeTaxRatio" : -0.0795040967033286694,
    "growthIncomeTaxExpense" : -0.117166442048517519,
    "growthNetIncome" : -0.0718113251919168111,
    "growthNetIncomeRatio" : -0.0524712012920381735,
    "growthEPS" : -0.0262266179034436608,
    "growthEPSDiluted" : -0.0262266179034436608,
    "growthWeightedAverageShsOut" : -0.0702376688188197512,
    "growthWeightedAverageShsOutDil" : -0.0702376688188197512
  }, ...
]
```
----
## GET /v3/cash-flow-statement-growth/{symbol} <a name="0x294354ba847915b9be24ca5cf40aaa58cf1134adfa403d6129ce3f557e48a4a2"></a>

Annual cash flow statements growth.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/financial-statements-growth

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x294354ba847915b9be24ca5cf40aaa58cf1134adfa403d6129ce3f557e48a4a2

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "date" : "2019-09-28",
    "symbol" : "AAPL",
    "period" : "FY",
    "growthRevenue" : -0.0204107758052674178,
    "growthCostOfRevenue" : -0.0120545201397200714,
    "growthGrossProfit" : -0.0338475436718742306,
    "growthGrossProfitRatio" : -0.0137154213078027384,
    "growthResearchAndDevelopmentExpenses" : 0.139154256813711713,
    "growthGeneralAndAdministrativeExpenses" : 0.0921879676743490029,
    "growthSellingAndMarketingExpenses" : 0,
    "growthOtherExpenses" : 0,
    "growthOperatingExpenses" : 0.113797226980382013,
    "growthCostAndExpenses" : 0.00794567969717047476,
    "growthInterestExpense" : 0.103703703703703701,
    "growthDepreciationAndAmortization" : 0.150784187838209655,
    "growthEBITDA" : -0.0430879293011946773,
    "growthEBITDARatio" : -0.0231486655986487197,
    "growthOperatingIncome" : -0.0982820389855849214,
    "growthOperatingIncomeRatio" : -0.0794935191428786103,
    "growthTotalOtherIncomeExpensesNet" : -1.95691609977324266,
    "growthIncomeBeforeTax" : -0.0982949947190101952,
    "growthIncomeBeforeTaxRatio" : -0.0795040967033286694,
    "growthIncomeTaxExpense" : -0.117166442048517519,
    "growthNetIncome" : -0.0718113251919168111,
    "growthNetIncomeRatio" : -0.0524712012920381735,
    "growthEPS" : -0.0262266179034436608,
    "growthEPSDiluted" : -0.0262266179034436608,
    "growthWeightedAverageShsOut" : -0.0702376688188197512,
    "growthWeightedAverageShsOutDil" : -0.0702376688188197512
  }, ...
]
```
----
## GET /v3/key-metrics-ttm/{symbol} <a name="0x78afea8f5f354b024be361d2dde7ed208ae59f77f4c929e01254a1d4a32de2db"></a>

Get Company Key Metrics such as Market capitalization, PE ratio, Price to Sales Ratio, POCF ratio, Graham Net-Net

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/company-key-metrics-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x78afea8f5f354b024be361d2dde7ed208ae59f77f4c929e01254a1d4a32de2db

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
period : quarter | annual
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "metrics" : [ {
    "date" : "2019-09-28",
    "Revenue per Share" : "56.3411",
    "Net Income per Share" : "11.9658",
    "Operating Cash Flow per Share" : "15.0267",
    "Free Cash Flow per Share" : "12.94",
    "Cash per Share" : "10.5773",
    "Book Value per Share" : "19.595",
    "Tangible Book Value per Share" : "73.306",
    "Shareholders Equity per Share" : "19.5953",
    "Interest Debt per Share" : "23.3978",
    "Market Cap" : "1012160744600.0",
    "Enterprise Value" : "1019650744600.0",
    "PE ratio" : "18.7109",
    "Price to Sales Ratio" : "3.8903",
    "POCF ratio" : "14.5863",
    "PFCF ratio" : "17.5607",
    "PB ratio" : "11.1154",
    "PTB ratio" : "11.1154",
    "EV to Sales" : "3.9191",
    "Enterprise Value over EBITDA" : "13.025",
    "EV to Operating cash flow" : "14.6943",
    "EV to Free cash flow" : "17.3127",
    "Earnings Yield" : "0.0534",
    "Free Cash Flow Yield" : "0.0582",
    "Debt to Equity" : "1.194",
    "Debt to Assets" : "0.3192",
    "Net Debt to EBITDA" : "0.0957",
    "Current ratio" : "1.54",
    "Interest Coverage" : "0.0",
    .....
    },
    {...}
    ]
}
```
----
## GET /v3/key-metrics/{symbol} <a name="0xf5cee6b7e8a2d3035ef040942dcb9b16de0b6e356929eac760fec061c9c05ddf"></a>

Get Company Key Metrics such as Market capitalization, PE ratio, Price to Sales Ratio, POCF ratio, Graham Net-Net
The key metrics are calculated quarter by quarter, year by year. The change in company metrics is essential for valuating a company. You can also acces the metrcis TTM.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/company-key-metrics-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xf5cee6b7e8a2d3035ef040942dcb9b16de0b6e356929eac760fec061c9c05ddf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
period : quarter | annual
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "metrics" : [ {
    "date" : "2019-09-28",
    "Revenue per Share" : "56.3411",
    "Net Income per Share" : "11.9658",
    "Operating Cash Flow per Share" : "15.0267",
    "Free Cash Flow per Share" : "12.94",
    "Cash per Share" : "10.5773",
    "Book Value per Share" : "19.595",
    "Tangible Book Value per Share" : "73.306",
    "Shareholders Equity per Share" : "19.5953",
    "Interest Debt per Share" : "23.3978",
    "Market Cap" : "1012160744600.0",
    "Enterprise Value" : "1019650744600.0",
    "PE ratio" : "18.7109",
    "Price to Sales Ratio" : "3.8903",
    "POCF ratio" : "14.5863",
    "PFCF ratio" : "17.5607",
    "PB ratio" : "11.1154",
    "PTB ratio" : "11.1154",
    "EV to Sales" : "3.9191",
    "Enterprise Value over EBITDA" : "13.025",
    "EV to Operating cash flow" : "14.6943",
    "EV to Free cash flow" : "17.3127",
    "Earnings Yield" : "0.0534",
    "Free Cash Flow Yield" : "0.0582",
    "Debt to Equity" : "1.194",
    "Debt to Assets" : "0.3192",
    "Net Debt to EBITDA" : "0.0957",
    "Current ratio" : "1.54",
    "Interest Coverage" : "0.0",
    .....
    },
    {...}
    ]
}
```
----
## GET /v3/financial-growth/{symbol} <a name="0xe608cdc0dbe1ee349249994d0b399ee0c250cf6e6c1a7a2ed9ab1a8ee0466277"></a>

Get the Financial Statement Growth of a company based on its financial statement, it compares previous financial statement to get growth of all its statement.
The growth is calculated quarter by quarter, year by year. The change in company metrics is essential for valuating a company.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/company-financial-statement-growth-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe608cdc0dbe1ee349249994d0b399ee0c250cf6e6c1a7a2ed9ab1a8ee0466277

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
period : quarter | annual
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "growth" : [ {
    "date" : "2019-09-28",
    "Gross Profit Growth" : "-0.0338",
    "EBIT Growth" : "-0.0983",
    "Operating Income Growth" : "-0.0983",
    "Net Income Growth" : "-0.0718",
    "EPS Growth" : "-0.0033",
    "EPS Diluted Growth" : "-0.0017",
    "Weighted Average Shares Growth" : "-0.0681",
    "Weighted Average Shares Diluted Growth" : "-0.0702",
    "Dividends per Share Growth" : "0.1029",
    "Operating Cash Flow growth" : "-0.1039",
    "Free Cash Flow growth" : "-0.0815",
    "10Y Revenue Growth (per Share)" : "0.2343",
    "5Y Revenue Growth (per Share)" : "0.1341",
    "3Y Revenue Growth (per Share)" : "0.1265",
    "10Y Operating CF Growth (per Share)" : "0.2491",
    "5Y Operating CF Growth (per Share)" : "0.089",
    "3Y Operating CF Growth (per Share)" : "0.0747",
    "10Y Net Income Growth (per Share)" : "0.2469",
    "5Y Net Income Growth (per Share)" : "0.1301",
    "3Y Net Income Growth (per Share)" : "0.1274",
    "10Y Shareholders Equity Growth (per Share)" : "0.145",
    "5Y Shareholders Equity Growth (per Share)" : "0.0134",
    "3Y Shareholders Equity Growth (per Share)" : "-0.058",
    "10Y Dividend per Share Growth (per Share)" : "0.0",
    "5Y Dividend per Share Growth (per Share)" : "0.1062",
    "3Y Dividend per Share Growth (per Share)" : "0.1123",
    "Receivables growth" : "-0.0651",
    "Inventory Growth" : "0.0379",
    "Asset Growth" : "-0.0744",
    "Book Value per Share Growth" : "-0.0937",
    "Debt Growth" : "-0.0562",
    "R&D Expense Growth" : "0.1392",
    "SG&A Expenses Growth" : "0.0922"
    },
    {...}
    ]
}
```
----
## GET /v3/rating/{symbol} <a name="0x45ee30f97f68b834762fb16b9f10f59e211bbe70b314800f7330015b564a3db6"></a>

Get the rating of a company based on its financial statement, Discounted cash flow analysis, financial rations and its intrinsic value.
Our ratings are based on comapnies being able to cover their debts and the strength of their ratios.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-rating-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x45ee30f97f68b834762fb16b9f10f59e211bbe70b314800f7330015b564a3db6

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "rating" : {
    "score" : 5,
    "rating" : "S-",
    "recommendation" : "Strong Buy"
  },
  "ratingDetails" : {
    "P/B" : {
      "score" : 5,
      "recommendation" : "Strong Buy"
    },
    "ROA" : {
      "score" : 5,
      "recommendation" : "Neutral"
    },
    "DCF" : {
      "score" : 3,
      "recommendation" : "Neutral"
    },
    "P/E" : {
      "score" : 5,
      "recommendation" : "Strong Buy"
    },
    "ROE" : {
      "score" : 5,
      "recommendation" : "Strong Buy"
    },
    "D/E" : {
      "score" : 3,
      "recommendation" : "Strong Buy"
    }
  }
}
```
----
## GET /v3/historical-rating/{symbol} <a name="0xdfdb5312feb8f42f3651623b2af176f393ec7fb14b137f35b78d44ddb80c1973"></a>

Historical companies rating.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-rating-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xdfdb5312feb8f42f3651623b2af176f393ec7fb14b137f35b78d44ddb80c1973

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "date" : "2021-10-27",
  "rating" : "S",
  "ratingScore" : 5,
  "ratingRecommendation" : "Strong Buy",
  "ratingDetailsDCFScore" : 5,
  "ratingDetailsDCFRecommendation" : "Strong Buy",
  "ratingDetailsROEScore" : 5,
  "ratingDetailsROERecommendation" : "Strong Buy",
  "ratingDetailsROAScore" : 3,
  "ratingDetailsROARecommendation" : "Neutral",
  "ratingDetailsDEScore" : 5,
  "ratingDetailsDERecommendation" : "Strong Buy",
  "ratingDetailsPEScore" : 5,
  "ratingDetailsPERecommendation" : "Strong Buy",
  "ratingDetailsPBScore" : 5,
  "ratingDetailsPBRecommendation" : "Strong Buy"
}, ...
]
```
----
## GET /v3/discounted-cash-flow/{symbol} <a name="0x60a393d432d929e97bd7636109af2a75d858fd1ef5473eb8b8d37cfd3140f224"></a>

Access a stock discounted cash flow value. This value represents a stock intrinsic value calculated from its free cash flow analysis. If this value is over the current stock price the stock is considered undervalued and vice versa.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-dcf-reports-free-api#DCF

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x60a393d432d929e97bd7636109af2a75d858fd1ef5473eb8b8d37cfd3140f224

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "date" : "2020-01-19",
  "dcf" : 332.10579358634374,
  "Stock Price" : 310.33
}
```
----
## GET /v3/historical-discounted-cash-flow-statement/{symbol} <a name="0x79a8fd3caa539331b18e87fffc4f5d05d16085910c1fa79d785d36d27374838c"></a>

Companies Historical Discounted cash flow value.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-dcf-reports-free-api#Historical-DCF

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x79a8fd3caa539331b18e87fffc4f5d05d16085910c1fa79d785d36d27374838c

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
period : annual | quater
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "date" : "2020-01-19",
    "dcf" : 332.10579358634374,
    "Stock Price" : 310.33
  }, ...
]
```
----
## GET /v3/historical-daily-discounted-cash-flow/{symbol} <a name="0xaca8caf67075f059cb66f19d44c2efa598086cfb8a081159cbb07806324ff241"></a>

Companies Daily Discounted cash flow value.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-dcf-reports-free-api#Historical-DCF

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xaca8caf67075f059cb66f19d44c2efa598086cfb8a081159cbb07806324ff241

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "date" : "2020-01-19",
    "dcf" : 332.10579358634374,
    "Stock Price" : 310.33
  }, ...
]
```
----
## GET /v3/earning_calendar <a name="0x26d554accbfcbae6987dfa5b9f02b7bd3cbe887b23190bcc06bb022f1e494f0f"></a>

Access Earnings calendar to Access all Earnings Calendar date such as AAPL, FB , MSFT next earnings date, EPS and EPS estimated.
You will be bale to Track companies who release earnings reports ordered by date.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/earnings-calendar-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x26d554accbfcbae6987dfa5b9f02b7bd3cbe887b23190bcc06bb022f1e494f0f

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2021-09-14",
    "symbol" : "CNM",
    "eps" : null,
    "epsEstimated" : 0.270000000000000018,
    "time" : "bmo",
    "revenue" : 0,
    "revenueEstimated" : 1241620000
  }, {
    "date" : "2021-09-14",
    "symbol" : "GGAL",
    "eps" : null,
    "epsEstimated" : 0.160000000000000003,
    "time" : "bmo",
    "revenue" : 0,
    "revenueEstimated" : 337540000
  }, {
    "date" : "2021-09-14",
    "symbol" : "SKIL",
    "eps" : null,
    "epsEstimated" : -0.0899999999999999967,
    "time" : "amc",
    "revenue" : 0,
    "revenueEstimated" : 158610000
  }, ...
]
```
----
## GET /v3/historical/earning_calendar/{symbol} <a name="0x47a1d9b10a83651bc37758429bdff597fcd25c3c49f9e5591c54d1a2fdd70abc"></a>

Access Earnings calendar to Access all Earnings Calendar date such as AAPL, FB , MSFT next earnings date, EPS and EPS estimated.
You will be bale to Track companies who release earnings reports ordered by date.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/earnings-calendar-api#Company-Historical-Earnings-Calendar

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x47a1d9b10a83651bc37758429bdff597fcd25c3c49f9e5591c54d1a2fdd70abc

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2021-07-27",
    "symbol" : "AAPL",
    "eps" : 1.30000000000000004,
    "epsEstimated" : 1,
    "time" : "amc",
    "revenue" : 81434000000,
    "revenueEstimated" : 84581900000
  }, {
    "date" : "2021-04-28",
    "symbol" : "AAPL",
    "eps" : 1.39999999999999991,
    "epsEstimated" : 0.989999999999999991,
    "time" : "amc",
    "revenue" : 89584000000,
    "revenueEstimated" : 76920700000
  }, ...
]
```
----
## GET /v3/ipo_calendar <a name="0x4662cd94cfb11798eef704fdc211ee489693e45bb5f2a15e5b7b2b64ac106107"></a>

We support a few calendars, and IPO Calendar is one of them. This calendar keeps track of all IPOs currently taking place in the market. Action shares exchange price range and other fields are among the fields returned. You can use it to keep track of what interesting stocks are going public and when they are going public. You can specify a date range, and if you don't  you will get the most recent IPOs

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/ipo-calendarы

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4662cd94cfb11798eef704fdc211ee489693e45bb5f2a15e5b7b2b64ac106107

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
 {
  "date" : "2020-08-31",
  "company" : "Applied UV, Inc.",
  "symbol" : "AUVI",
  "exchange" : "NASDAQ Capital",
  "actions" : "expected",
  "shares" : 1000000,
  "priceRange" : "5.00",
  "marketCap" : 5750000
}, {
  "date" : "2020-08-28",
  "company" : "Petra Acquisition Inc.",
  "symbol" : "PAICU",
  "exchange" : "NASDAQ Capital",
  "actions" : "expected",
  "shares" : 7500000,
  "priceRange" : "10.00",
  "marketCap" : 86250000
}, {
  "date" : "2020-08-28",
  "company" : "Sun BioPharma, Inc.",
  "symbol" : "",
  "exchange" : "NASDAQ Capital",
  "actions" : "expected",
  "shares" : 2100000,
  "priceRange" : "5.00",
  "marketCap" : 10500000
}, { ... }
]
```
----
## GET /v3/stock_split_calendar <a name="0xe6b64232543e0f8ec44b06b794ea9bac1f30e3194446b705f69d583505b2d887"></a>

Access a stock split calendar that includes the numerator, denominator, and exact date of the split. Stock splits are a way for publicly traded companies to improve stock liquidity, typically, companies increase the number of shares outstanding, which lowers the stock price, however, the number of shares outstanding can also be reduced, increasing the stock price. The value of a company does not change as a result of a stock split.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-split-calendar

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe6b64232543e0f8ec44b06b794ea9bac1f30e3194446b705f69d583505b2d887

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
 {
  "date" : "2020-08-31",
  "label" : "August 31, 20",
  "symbol" : "TSLA",
  "numerator" : 5.0,
  "denominator" : 5.0
}, {
  "date" : "2020-08-31",
  "label" : "August 31, 20",
  "symbol" : "AAPL",
  "numerator" : 4.0,
  "denominator" : 4.0
}, {
  "date" : "2020-08-28",
  "label" : "August 28, 20",
  "symbol" : "WEBS",
  "numerator" : 1.0,
  "denominator" : 1.0
}, ...
]
```
----
## GET /v3/stock_dividend_calendar <a name="0x7c82f8fd59f261f612e76210e69ae29128bbfde68acdcc910013a2bf3bb8ecc9"></a>

Access Dividend calendar to get dividends within period of time.
Profit stocks appropriate a part of the organization's income to financial backers consistently.
In addition to Stock paying dividend, Stock Market Index plays an important role in the flow of money within the stock market.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/dividend-calendar

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7c82f8fd59f261f612e76210e69ae29128bbfde68acdcc910013a2bf3bb8ecc9

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
{
  "date" : "2020-09-02",
  "label" : "September 02, 20",
  "adjDividend" : 0.02,
  "symbol" : "BOL.PA"
}, {
  "date" : "2020-09-01",
  "label" : "September 01, 20",
  "adjDividend" : 0.47,
  "symbol" : "WKL.AS"
}, {
  "date" : "2020-09-01",
  "label" : "September 01, 20",
  "adjDividend" : 0.002809,
  "symbol" : "ITUB"
}, {
  "date" : "2020-09-01",
  "label" : "September 01, 20",
  "adjDividend" : 0.05,
  "symbol" : "FEI"
}, { ... }
]
```
----
## GET /v3/economic_calendar <a name="0xa8cd3d01e5a6ede542df42226fd8192a228f59c5455965de48bc1f2f8cded14d"></a>

This is an economic calendar that returns all of the world's major economic events and numbers. It has a significant impact on currency and stock market prices. It returns fields such as the name of the event, the country, the previous and current value of the event, and more. Every 15 minutes, the calendar is updated.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/economic-calendar

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xa8cd3d01e5a6ede542df42226fd8192a228f59c5455965de48bc1f2f8cded14d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "event" : "United States Job Openings JOLTS Job Openings",
    "date" : "2020-10-06 14:00:00",
    "country" : "US",
    "actual" : null,
    "previous" : 6.618,
    "change" : null,
    "changePercentage" : null,
    "estimate" : null
  }, {
    "event" : "United States Redbook Redbook MM ",
    "date" : "2020-10-06 12:55:00",
    "country" : "US",
    "actual" : null,
    "previous" : -0.3,
    "change" : null,
    "changePercentage" : null,
    "estimate" : null
  }, {
    "event" : "United States Redbook Redbook YY ",
    "date" : "2020-10-06 12:55:00",
    "country" : "US",
    "actual" : null,
    "previous" : 2.2,
    "change" : null,
    "changePercentage" : null,
    "estimate" : null
  }, ...
]
```
----
## GET /v3/search <a name="0xfd6eb01969f7e3a2904382229564636e4423a398acfe40f182c543737b27846b"></a>

Search stocks that are in our API by company name or ticker. You can also use the exchange filter to narrow down your results. Company name, currency, and exchange are some of the fields that are returned by API.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-ticker-symbol-lookup-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xfd6eb01969f7e3a2904382229564636e4423a398acfe40f182c543737b27846b

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Limit : Number
Query : String
Exchange : ETF | MUTUAL_FUND | COMMODITY | INDEX | CRYPTO | FOREX | TSX | AMEX | NASDAQ | NYSE | EURONEXT
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
    {
        "symbol" : "PRAA",
        "name" : "PRA Group, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "PAAS",
        "name" : "Pan American Silver Corp.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "PAAC",
        "name" : "Proficient Alpha Acquisition Corp.",
        "currency" : "USD",
        "stockExchange" : "NasdaqCM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "RYAAY",
        "name" : "Ryanair Holdings plc",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "MPAA",
        "name" : "Motorcar Parts of America, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "STAA",
        "name" : "STAAR Surgical Company",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "RBCAA",
        "name" : "Republic Bancorp, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AABA",
        "name" : "Altaba Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AAXJ",
        "name" : "iShares MSCI All Country Asia ex Japan ETF",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "ZNWAA",
        "name" : "Zion Oil & Gas, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    }
]
```
----
## GET /v3/search-ticker <a name="0x4c3bc218efd10bfa620732e05c94616d8ea50413781960d3a917af71c4e79eab"></a>

Search stocks that are in our API by company name or ticker. You can also use the exchange filter to narrow down your results. Company name, currency, and exchange are some of the fields that are returned by API.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-ticker-symbol-lookup-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4c3bc218efd10bfa620732e05c94616d8ea50413781960d3a917af71c4e79eab

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Limit : Number
Query : String
Exchange : ETF | MUTUAL_FUND | COMMODITY | INDEX | CRYPTO | FOREX | TSX | AMEX | NASDAQ | NYSE | EURONEXT
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
    {
        "symbol" : "PRAA",
        "name" : "PRA Group, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "PAAS",
        "name" : "Pan American Silver Corp.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "PAAC",
        "name" : "Proficient Alpha Acquisition Corp.",
        "currency" : "USD",
        "stockExchange" : "NasdaqCM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "RYAAY",
        "name" : "Ryanair Holdings plc",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "MPAA",
        "name" : "Motorcar Parts of America, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "STAA",
        "name" : "STAAR Surgical Company",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "RBCAA",
        "name" : "Republic Bancorp, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AABA",
        "name" : "Altaba Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGS",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AAXJ",
        "name" : "iShares MSCI All Country Asia ex Japan ETF",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "ZNWAA",
        "name" : "Zion Oil & Gas, Inc.",
        "currency" : "USD",
        "stockExchange" : "NasdaqGM",
        "exchangeShortName" : "NASDAQ"
    }
]
```
----
## GET /v3/stock-screener <a name="0x2b39fd9c23518233cd8285813b3ee47cd3f58765ef7d6e39573575825e6f4d35"></a>

Stock screener is a more advanced way to search for stocks. Unlike our search endpoint, there is no query parameter, but there are numerous parameters such as market cap, price, volume, beta, sector, country, and so on. For example, you can use this endpoint to find NASDAQ-listed software companies that pay dividends and have good liquidity.


**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-screener-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2b39fd9c23518233cd8285813b3ee47cd3f58765ef7d6e39573575825e6f4d35

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
marketCapMoreThan & marketCapLowerThan : Number
priceMoreThan & priceLowerThan : Number
betaMoreThan & betaLowerThan : Number
volumeMoreThan & volumeLowerThan : Number
dividendMoreThan & dividendLowerThan : Number
isEtf & isActivelyTrading : true/false
sector : Consumer Cyclical | Energy | Technology | Industrials | Financial Services | Basic Materials | Communication Services | Consumer Defensive | Healthcare | Real Estate | Utilities | Industrial Goods | Financial | Services | Conglomerates
Industry : Autos | Banks | Banks Diversified | Software | Banks Regional | Beverages Alcoholic | Beverages Brewers | Beverages Non-Alcoholic
Country : US | UK | MX | BR | RU | HK | CA | ...
exchange : nyse | nasdaq | amex | euronext | tsx | etf | mutual_fund
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
    {
    "symbol" : "MSFT",
    "companyName" : "Microsoft Corporation",
    "marketCap" : 1391637040000,
    "sector" : "Technology",
    "beta" : 1.2310280000000000111270992420031689107418060302734375,
    "price" : 183.509999999999990905052982270717620849609375,
    "lastAnnualDividend" : 1.939999999999999946709294817992486059665679931640625,
    "volume" : 54536583,
    "exchange" : "Nasdaq Global Select",
    "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AAPL",
        "companyName" : "Apple Inc.",
        "marketCap" : 1382174560000,
        "sector" : "Technology",
        "beta" : 1.2284990000000000076596506914938800036907196044921875,
        "price" : 318.8899999999999863575794734060764312744140625,
        "lastAnnualDividend" : 3.0800000000000000710542735760100185871124267578125,
        "volume" : 51500795,
        "exchange" : "Nasdaq Global Select",
        "exchangeShortName" : "NASDAQ"
    },
    {
        "symbol" : "AMZN",
        "companyName" : "Amazon.com Inc.",
        "marketCap" : 1215457260000,
        "sector" : "Technology",
        "beta" : 1.5168630000000000723758830645238049328327178955078125,
        "price" : 2436.8800000000001091393642127513885498046875,
        "lastAnnualDividend" : 0,
        "volume" : 6105985,
        "exchange" : "Nasdaq Global Select",
        "exchangeShortName" : "NASDAQ"
    }
]
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

Access data for a company such as 52 week high, 52 week low, market capitalization, and key stats to understand a company finance.
Access companies profile (Price, Beta, Volume Average, Market Capitalisation, Last Dividend, 52 week range, stock price change, stock price change in percentage, Company Name, Exchange, Description, Industry, Sector, CEO,Website and image).

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/companies-key-stats-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc77379b6803bfb6a3bc8c17652916281c6c687fc9e7d50a6f4c9e6ba56715dca

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "price" : 145.85,
  "beta" : 1.201965,
  "volAvg" : 79766736,
  "mktCap" : 2410929717248,
  "lastDiv" : 0.85,
  "range" : "105.0-157.26",
  "changes" : 2.4200134,
  "companyName" : "Apple Inc.",
  "currency" : "USD",
  "cik" : "0000320193",
  "isin" : "US0378331005",
  "cusip" : "037833100",
  "exchange" : "Nasdaq Global Select",
  "exchangeShortName" : "NASDAQ",
  "industry" : "Consumer Electronics",
  "website" : "http://www.apple.com",
  "description" : "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables, and accessories worldwide. It also sells various related services. The company offers iPhone, a line of smartphones; Mac, a line of personal computers; iPad, a line of multi-purpose tablets; and wearables, home, and accessories comprising AirPods, Apple TV, Apple Watch, Beats products, HomePod, iPod touch, and other Apple-branded and third-party accessories. It also provides AppleCare support services; cloud services store services; and operates various platforms, including the App Store, that allow customers to discover and download applications and digital content, such as books, music, video, games, and podcasts. In addition, the company offers various services, such as Apple Arcade, a game subscription service; Apple Music, which offers users a curated listening experience with on-demand radio stations; Apple News+, a subscription news and magazine service; Apple TV+, which offers exclusive original content; Apple Card, a co-branded credit card; and Apple Pay, a cashless payment service, as well as licenses its intellectual property. The company serves consumers, and small and mid-sized businesses; and the education, enterprise, and government markets. It sells and delivers third-party applications for its products through the App Store. The company also sells its products through its retail and online stores, and direct sales force; and third-party cellular network carriers, wholesalers, retailers, and resellers. Apple Inc. was founded in 1977 and is headquartered in Cupertino, California.",
  "ceo" : "Mr. Timothy Cook",
  "sector" : "Technology",
  "country" : "US",
  "fullTimeEmployees" : "147000",
  "phone" : "14089961010",
  "address" : "1 Apple Park Way",
  "city" : "Cupertino",
  "state" : "CALIFORNIA",
  "zip" : "95014",
  "dcfDiff" : 89.92,
  "dcf" : 148.019,
  "image" : "https://financialmodelingprep.com/image-stock/AAPL.png",
  "ipoDate" : "1980-12-12",
  "defaultImage" : false,
  "isEtf" : false,
  "isActivelyTrading" : true,
  "isAdr" : false,
  "isFund" : false
} ]
```
----
## GET /v3/key-executives/{symbol} <a name="0x9d02f28e45306d8729c95a8e38222ee2f6621e6a383475bb5845e4237bf942df"></a>

Key executives are the people at the top of a company who make critical decisions that affect the company. We keep track of who they are, what their titles are, and how much money they make. We support the majority of companies because not everyone discloses all of their information.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/key-executives

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x9d02f28e45306d8729c95a8e38222ee2f6621e6a383475bb5845e4237bf942df

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "yearBorn" : 1950,
  "pay" : 557922,
  "currencyPay" : "USD",
  "name" : "Dr. Arthur Levinson",
  "title" : "Independent Chairman of the Board",
  "gender" : "male",
  "titleSince" : "2011"
}, {
  "symbol" : "AAPL",
  "yearBorn" : 1960,
  "pay" : 11555466,
  "currencyPay" : "USD",
  "name" : "Mr. Timothy Cook",
  "title" : "Chief Executive Officer, Director",
  "gender" : "male",
  "titleSince" : "2011"
}, ...
```
----
## GET /v3/market-capitalization/{symbol} <a name="0x6f2a3e7e2d263d737fc8765fd1fefba6e0b011b1430be1a57c424c5b953c6dc5"></a>

The value of a company is measured by its market capitalization. It's calculated by multiplying the price by the number of outstanding shares, both of which can be found on our quote endpoint. It's crucial in determining whether a company is undervalued, fairly valued or overvalued.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/market-capitalization

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6f2a3e7e2d263d737fc8765fd1fefba6e0b011b1430be1a57c424c5b953c6dc5

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "symbol" : "AAPL",
    "date" : "2020-07-24",
    "marketCap" : 1641007358213.16797
} ]
```
----
## GET /v3/historical-market-capitalization/{symbol} <a name="0xeeb404e11f70d5fd43f2ae5c8f04ba20ed33e58f55617c35e1035d5064288d98"></a>

The value of a company is measured by its market capitalization. It's calculated by multiplying the price by the number of outstanding shares, both of which can be found on our quote endpoint. It's crucial in determining whether a company is undervalued, fairly valued or overvalued.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/market-capitalization

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xeeb404e11f70d5fd43f2ae5c8f04ba20ed33e58f55617c35e1035d5064288d98

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "symbol" : "AAPL",
  "date" : "2020-07-27",
  "marketCap" : 1679899663223.52002
}
```
----
## GET /v4/company-outlook <a name="0x042989ba15709efe8105bfc178cc304e2e57b976cd3bcef0ac7cc60aa82f55b8"></a>

Get the overview of any company. You will access its profile information, most insider trading transactions, financial statements in one API call.
Accessing all of this information in one API call is very usefull to get companies insight.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/company-outlook

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x042989ba15709efe8105bfc178cc304e2e57b976cd3bcef0ac7cc60aa82f55b8

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "profile" : {
    "symbol" : "AAPL",
    "price" : 124.76,
    "beta" : 1.33758,
    "volAvg" : 111774589,
    "mktCap" : 2094483370000,
    "lastDiv" : 0.82,
    "range" : "53.1525-145.09",
    "changes" : -0.81,
    "companyName" : "Apple Inc",
    "currency" : "USD",
    "cik" : "0000320193",
    "isin" : "US0378331005",
    "cusip" : "037833100",
    "exchange" : "Nasdaq Global Select",
    "exchangeShortName" : "NASDAQ",
    "industry" : "Consumer Electronics",
    "website" : "https://www.apple.com/",
    "description" : "Apple Inc. designs, manufactures, and markets smartphones, personal computers, tablets, wearables, and accessories worldwide. It also sells various related services. The company offers iPhone, a line of smartphones; Mac, a line of personal computers; iPad, a line of multi-purpose tablets; and wearables, home, and accessories comprising AirPods, Apple TV, Apple Watch, Beats products, HomePod, iPod touch, and other Apple-branded and third-party accessories. It also provides AppleCare support services; cloud services store services; and operates various platforms, including the App Store, that allow customers to discover and download applications and digital content, such as books, music, video, games, and podcasts. In addition, the company offers various services, such as Apple Arcade, a game subscription service; Apple Music, which offers users a curated listening experience with on-demand radio stations; Apple News+, a subscription news and magazine service; Apple TV+, which offers exclusive original content; Apple Card, a co-branded credit card; and Apple Pay, a cashless payment service, as well as licenses its intellectual property. The company serves consumers, and small and mid-sized businesses; and the education, enterprise, and government markets. It sells and delivers third-party applications for its products through the App Store. The company also sells its products through its retail and online stores, and direct sales force; and third-party cellular network carriers, wholesalers, retailers, and resellers. Apple Inc. was founded in 1977 and is headquartered in Cupertino, California.",
    "ceo" : "Mr. Timothy Cook",
    "sector" : "Technology",
    "country" : "US",
    "fullTimeEmployees" : "147000",
    "phone" : "14089961010",
    "address" : "1 Apple Park Way",
    "city" : "Cupertino",
    "state" : "CALIFORNIA",
    "zip" : "95014",
    "dcfDiff" : 89.92,
    "dcf" : 127.377,
    "image" : "https://financialmodelingprep.com/image-stock/AAPL.png",
    "ipoDate" : "1980-12-12",
    "defaultImage" : false,
    "isEtf" : false,
    "isActivelyTrading" : true
  },
  "insideTrades" : [ {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-23",
    "reportingCik" : "0001051401",
    "transactionType" : "A-Award",
    "securitiesOwned" : 1986.0,
    "companyCik" : "0000320193",
    "reportingName" : "JUNG ANDREA",
    "typeOfOwner" : "director",
    "acquistionOrDisposition" : "A",
    "formType" : "4",
    "securitiesTransacted" : 1986.0,
    "price" : 0.0,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000036/0000320193-21-000036-index.htm"
  }, {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-23",
    "reportingCik" : "0001224944",
    "transactionType" : "A-Award",
    "securitiesOwned" : 1986.0,
    "companyCik" : "0000320193",
    "reportingName" : "GORE ALBERT JR",
    "typeOfOwner" : "director",
    "acquistionOrDisposition" : "A",
    "formType" : "4",
    "securitiesTransacted" : 1986.0,
    "price" : 0.0,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000035/0000320193-21-000035-index.htm"
  }, {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-23",
    "reportingCik" : "0001182047",
    "transactionType" : "A-Award",
    "securitiesOwned" : 1986.0,
    "companyCik" : "0000320193",
    "reportingName" : "BELL JAMES A",
    "typeOfOwner" : "director",
    "acquistionOrDisposition" : "A",
    "formType" : "4",
    "securitiesTransacted" : 1986.0,
    "price" : 0.0,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000034/0000320193-21-000034-index.htm"
  }, {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-23",
    "reportingCik" : "0001216519",
    "transactionType" : "A-Award",
    "securitiesOwned" : 1986.0,
    "companyCik" : "0000320193",
    "reportingName" : "SUGAR RONALD D",
    "typeOfOwner" : "director",
    "acquistionOrDisposition" : "A",
    "formType" : "4",
    "securitiesTransacted" : 1986.0,
    "price" : 0.0,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000039/0000320193-21-000039-index.htm"
  }, {
    "symbol" : "AAPL",
    "transactionDate" : "2021-02-23",
    "reportingCik" : "0001179864",
    "transactionType" : "A-Award",
    "securitiesOwned" : 1986.0,
    "companyCik" : "0000320193",
    "reportingName" : "LOZANO MONICA C",
    "typeOfOwner" : "director",
    "acquistionOrDisposition" : "A",
    "formType" : "4",
    "securitiesTransacted" : 1986.0,
    "price" : 0.0,
    "securityName" : "Restricted Stock Unit",
    "link" : "https://www.sec.gov/Archives/edgar/data/0000320193/000032019321000038/0000320193-21-000038-index.htm"
  } ],
  "keyExecutives" : [ {
    "title" : "Chief Executive Officer & Director",
    "name" : "Mr. Timothy D. Cook",
    "gender" : "male",
    "pay" : 14770000,
    "currencyPay" : "USD"
  }, {
    "title" : "Chief Financial Officer & Senior Vice President",
    "name" : "Mr. Luca  Maestri",
    "gender" : "male",
    "pay" : 4600000,
    "currencyPay" : "USD"
  }, {
    "title" : "Chief Operating Officer",
    "name" : "Mr. Jeffrey E. Williams",
    "gender" : "male",
    "pay" : 4590000,
    "currencyPay" : "USD"
  }, {
    "title" : "Senior Vice President, Gen. Counsel & Sec.",
    "name" : "Ms. Katherine L. Adams",
    "gender" : "female",
    "pay" : 4590000,
    "currencyPay" : "USD"
  }, {
    "title" : "Senior Vice President of People & Retail",
    "name" : "Ms. Deirdre  O'Brien",
    "gender" : "female",
    "pay" : 4610000,
    "currencyPay" : "USD"
  }, {
    "title" : "Senior Director of Corporation Accounting",
    "name" : "Mr. Chris  Kondo",
    "gender" : "male",
    "pay" : 288170,
    "currencyPay" : "USD"
  }, {
    "title" : "Chief Technology Officer",
    "name" : "Mr. James  Wilson",
    "gender" : "male",
    "pay" : 249840,
    "currencyPay" : "USD"
  }, {
    "title" : "Chief Information Officer",
    "name" : "Ms. Mary  Demby",
    "gender" : "female",
    "pay" : 500960,
    "currencyPay" : "USD"
  }, {
    "title" : "Senior Director of Investor Relations & Treasury",
    "name" : "Ms. Nancy  Paxton",
    "gender" : "female",
    "pay" : 311610,
    "currencyPay" : "USD"
  }, {
    "title" : "Senior Vice President of Worldwide Marketing",
    "name" : "Mr. Greg  Joswiak",
    "gender" : "male",
    "pay" : null,
    "currencyPay" : "USD"
  } ],
  "splitHistory" : [ {
    "date" : "2020-08-31",
    "label" : "August 31, 20",
    "numerator" : 4.00,
    "denominator" : 1.00
  }, {
    "date" : "2014-06-09",
    "label" : "June 09, 14",
    "numerator" : 7.00,
    "denominator" : 1.00
  }, {
    "date" : "2005-02-28",
    "label" : "February 28, 05",
    "numerator" : 2.00,
    "denominator" : 1.00
  }, {
    "date" : "2000-06-21",
    "label" : "June 21, 00",
    "numerator" : 2.00,
    "denominator" : 1.00
  }, {
    "date" : "1987-06-16",
    "label" : "June 16, 87",
    "numerator" : 2.00,
    "denominator" : 1.00
  } ],
  "stockDividend" : [ {
    "date" : "2021-02-05",
    "label" : "February 05, 21",
    "adjDividend" : 0.2050000000,
    "dividend" : 0.205,
    "recordDate" : "2021-02-08",
    "paymentDate" : "2021-02-11",
    "declarationDate" : "2021-01-27"
  }, {
    "date" : "2020-11-06",
    "label" : "November 06, 20",
    "adjDividend" : 0.2050000000,
    "dividend" : 0.205,
    "recordDate" : "2020-11-9",
    "paymentDate" : "2020-11-12",
    "declarationDate" : "2020-10-29"
  }, {
    "date" : "2020-08-07",
    "label" : "August 07, 20",
    "adjDividend" : 0.2050000000,
    "dividend" : 0.82,
    "recordDate" : "2020-08-10",
    "paymentDate" : "2020-08-13",
    "declarationDate" : "2020-07-30"
  }, {
    "date" : "2020-05-08",
    "label" : "May 08, 20",
    "adjDividend" : 0.2050000000,
    "dividend" : 0.82,
    "recordDate" : "2020-05-11",
    "paymentDate" : "2020-05-14",
    "declarationDate" : "2020-04-30"
  }, {
    "date" : "2020-02-07",
    "label" : "February 07, 20",
    "adjDividend" : 0.1925000000,
    "dividend" : 0.77,
    "recordDate" : "2020-02-10",
    "paymentDate" : "2020-02-13",
    "declarationDate" : "2020-01-28"
  } ],
  "stockNews" : [ {
    "symbol" : "AAPL",
    "publishedDate" : "2021-03-18 07:42:00",
    "title" : "Apple may launch newer, faster iPad models by April: report",
    "image" : "https://cdn.snapi.dev/images/v1/i/d/im-313314width620size15005861664712778-729137.jpg",
    "site" : "Market Watch",
    "text" : "Tech giant Apple may be gearing up to roll out new iPads for consumers, in what could be its first product event of 2021, Bloomberg reports.",
    "url" : "https://www.marketwatch.com/story/apple-may-launch-newer-faster-ipad-models-by-april-report-11616067771"
  }, {
    "symbol" : "AAPL",
    "publishedDate" : "2021-03-18 07:05:00",
    "title" : "Here's Why Apple Is a Good Stock to Buy Now",
    "image" : "https://cdn.snapi.dev/images/v1/2/l/ap82-729066.jpg",
    "site" : "The Motley Fool",
    "text" : "Down 15% from its all-time high, the tech-giant's shares look like a good long-term bet.",
    "url" : "https://www.fool.com/investing/2021/03/18/heres-why-apple-is-a-good-stock-to-buy-now/"
  }, {
    "symbol" : "AAPL",
    "publishedDate" : "2021-03-18 05:32:57",
    "title" : "Apple: The Buyback Will Go On",
    "image" : "https://cdn.snapi.dev/images/v1/t/j/105439160-1536344620107airpower0530x298-728944.jpg",
    "site" : "Seeking Alpha",
    "text" : "Current repurchase plan could be finished in the next few months. Next earnings update should feature a major authorization increase.",
    "url" : "https://seekingalpha.com/article/4414704-apple-buyback-will-go-on"
  }, {
    "symbol" : "AAPL",
    "publishedDate" : "2021-03-18 05:30:00",
    "title" : "Should You Invest Your Stimulus Check in Penny Stocks?",
    "image" : "https://cdn.snapi.dev/images/v1/e/a/urlhttps3a2f2fgfoolcdncom2feditorial2fimages2f6182672fpenny-sitting-on-assorted-billsjpgw700opresize-728946.jpg",
    "site" : "The Motley Fool",
    "text" : "Are penny stocks the right investment for you?",
    "url" : "https://www.fool.com/investing/2021/03/18/should-you-invest-your-stimulus-check-in-penny-sto/"
  }, {
    "symbol" : "AAPL",
    "publishedDate" : "2021-03-18 04:42:51",
    "title" : "Apple's 'I Am a Mac' Guy Now Wants You To Buy A PC Instead",
    "image" : "https://cdn.snapi.dev/images/v1/2/5/250alsbntf-1-728916.jpg",
    "site" : "Benzinga",
    "text" : "Intel Corporation (NASDAQ: INTC) is borrowing a few leaves out of Apple Inc's (NASDAQ: AAPL) advertising playbook in a recent spate of advertisements aimed at the iPhone maker. What Happened: The silicon giant has roped in Justin Long of the “I'm a Mac and I'm a PC” era fame to take a few digs at the Tim Cook-led company.",
    "url" : "https://www.benzinga.com/news/21/03/20228121/apples-i-am-a-mac-guy-now-wants-you-to-buy-a-pc-instead"
  } ],
  "financialsAnnual" : {
    "income" : [ {
      "date" : "2020-09-26",
      "symbol" : "AAPL",
      "reportedCurrency" : "USD",
      "fillingDate" : "2020-10-30",
      "acceptedDate" : "2020-10-29 18:06:25",
      "period" : "FY",
      "revenue" : 274515000000,
      "costOfRevenue" : 169559000000,
      "grossProfit" : 104956000000,
      "grossProfitRatio" : 0.38233247727810865,
      "researchAndDevelopmentExpenses" : 18752000000,
      "generalAndAdministrativeExpenses" : 19916000000,
      "sellingAndMarketingExpenses" : 0.0,
      "otherExpenses" : -87000000,
      "operatingExpenses" : 38668000000,
      "costAndExpenses" : 208227000000,
      "interestExpense" : 2873000000,
      "depreciationAndAmortization" : 11056000000,
      "ebitda" : 81020000000,
      "ebitdaratio" : 0.2951386991603373,
      "operatingIncome" : 66288000000,
      "operatingIncomeRatio" : 0.24439830246070343,
      "totalOtherIncomeExpensesNet" : -87000000,
      "incomeBeforeTax" : 67091000000,
      "incomeBeforeTaxRatio" : 0.24439830246070343,
      "incomeTaxExpense" : 9680000000,
      "netIncome" : 57411000000,
      "netIncomeRatio" : 0.20913611278072236,
      "eps" : 3.31,
      "epsdiluted" : 3.28,
      "weightedAverageShsOut" : 17352119000,
      "weightedAverageShsOutDil" : 17528214000,
      "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/0000320193-20-000096-index.htm",
      "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019320000096/aapl-20200926.htm"
    }, {
      "date" : "2019-09-28",
      "symbol" : "AAPL",
      "reportedCurrency" : "USD",
      "fillingDate" : "2019-10-31 00:00:00",
      "acceptedDate" : "2019-10-30 18:12:36",
      "period" : "FY",
      "revenue" : 260174000000,
      "costOfRevenue" : 161782000000,
      "grossProfit" : 98392000000,
      "grossProfitRatio" : 0.3781776810903472,
      "researchAndDevelopmentExpenses" : 16217000000,
      "generalAndAdministrativeExpenses" : 18245000000,
      "sellingAndMarketingExpenses" : 0.0,
      "otherExpenses" : 422000000,
      "operatingExpenses" : 34462000000,
      "costAndExpenses" : 196244000000,
      "interestExpense" : 3576000000,
      "depreciationAndAmortization" : 12547000000,
      "ebitda" : 81860000000,
      "ebitdaratio" : 0.3146355900282119,
      "operatingIncome" : 63930000000,
      "operatingIncomeRatio" : 0.2526655238417367,
      "totalOtherIncomeExpensesNet" : 422000000,
      "incomeBeforeTax" : 65737000000,
      "incomeBeforeTaxRatio" : 0.2526655238417367,
      "incomeTaxExpense" : 10481000000,
      "netIncome" : 55256000000,
      "netIncomeRatio" : 0.21238094505984456,
      "eps" : 2.9925,
      "epsdiluted" : 2.9725,
      "weightedAverageShsOut" : 18471336000,
      "weightedAverageShsOutDil" : 18595652000,
      "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019319000119/0000320193-19-000119-index.html",
      "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019319000119/a10-k20199282019.htm"
    }, {
      "date" : "2018-09-29",
      "symbol" : "AAPL",
      "reportedCurrency" : "USD",
      "fillingDate" : "2018-11-05 00:00:00",
      "acceptedDate" : "2018-11-05 08:01:40",
      "period" : "FY",
      "revenue" : 265595000000,
      "costOfRevenue" : 163756000000,
      "grossProfit" : 101839000000,
      "grossProfitRatio" : 0.38343718820007905,
      "researchAndDevelopmentExpenses" : 14236000000,
      "generalAndAdministrativeExpenses" : 16705000000,
      "sellingAndMarketingExpenses" : 0.0,
      "otherExpenses" : -441000000,
      "operatingExpenses" : 30941000000,
      "costAndExpenses" : 194697000000,
      "interestExpense" : 3240000000,
      "depreciationAndAmortization" : 10903000000,
      "ebitda" : 87046000000,
      "ebitdaratio" : 0.327739603531693,
      "operatingIncome" : 70898000000,
      "operatingIncomeRatio" : 0.27448935409175623,
      "totalOtherIncomeExpensesNet" : -441000000,
      "incomeBeforeTax" : 72903000000,
      "incomeBeforeTaxRatio" : 0.27448935409175623,
      "incomeTaxExpense" : 13372000000,
      "netIncome" : 59531000000,
      "netIncomeRatio" : 0.22414202074587247,
      "eps" : 3.0025,
      "epsdiluted" : 2.9775,
      "weightedAverageShsOut" : 19821508000,
      "weightedAverageShsOutDil" : 20000436000,
      "link" : "https://www.sec.gov/Archives/edgar/data/320193/000032019318000145/0000320193-18-000145-index.html",
      "finalLink" : "https://www.sec.gov/Archives/edgar/data/320193/000032019318000145/a10-k20189292018.htm"
    }, { ... }
```
----
## GET /v4/stock_peers <a name="0x94e8db923ed3a09bb3532dc1a6de3e904e90eb4b933757a1e2c427e07fea61bf"></a>

Stock peers are a group of companies that trade on the same exchange, are in the same industry (values can be found on our profile endpoint), and have a similar market capitalizations (which can be found on our market cap endpoint). All of our peers are based on stocks available through our API. This endpoint can be used to look up the competitors of a company you're interested in.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-peers

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x94e8db923ed3a09bb3532dc1a6de3e904e90eb4b933757a1e2c427e07fea61bf

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "peersList" : [ "MSFT", "NVDA", "ASML", "ADBE", "INTC", "CSCO", "AVGO", "TXN", "QCOM", "AMAT" ]
} ]
```
----
## GET /v3/is-the-market-open <a name="0x0687de301cca188f078be3bbdb4be2f13373800316ae71cd9dace80858931b23"></a>

We support many markets, and this endpoint tells you which ones are open and which ones are closed. It returns the current state of the US market and EURONEXT. It also returns days when the stock market is closed, such as New Year's Day or Christmas.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/is-the-market-open

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0687de301cca188f078be3bbdb4be2f13373800316ae71cd9dace80858931b23

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "stockExchangeName" : "New York Stock Exchange",
  "stockMarketHours" : {
    "openingHour" : "09:30 a.m. ET",
    "closingHour" : "04:00 p.m. ET"
  },
  "stockMarketHolidays" : [ {
    "year" : 2019,
    "New Years Day" : "2019-01-01",
    "Martin Luther King, Jr. Day" : "2019-01-21",
    "Washington's Birthday" : "2019-02-18",
    "Good Friday" : "2019-04-19",
    "Memorial Day" : "2019-05-27",
    "Independence Day" : "2019-07-04",
    "Labor Day" : "2019-09-02",
    "Thanksgiving Day" : "2019-11-28",
    "Christmas" : "2019-12-25"
  }, {
    "year" : 2020,
    "New Years Day" : "2020-01-02",
    "Martin Luther King, Jr. Day" : "2020-01-21",
    "Washington's Birthday" : "2020-02-18",
    "Good Friday" : "2020-04-12",
    "Memorial Day" : "2020-05-27",
    "Independence Day" : "2020-07-05",
    "Labor Day" : "2020-09-09",
    "Thanksgiving Day" : "2020-11-28",
    "Christmas" : "2020-12-27"
  }, {
    "year" : 2021,
    "New Years Day" : "2021-01-04",
    "Martin Luther King, Jr. Day" : "2021-01-21",
    "Washington's Birthday" : "2021-02-18",
    "Good Friday" : "2021-04-05",
    "Memorial Day" : "2021-06-03",
    "Independence Day" : "2021-07-08",
    "Labor Day" : "2021-09-09",
    "Thanksgiving Day" : "2021-11-28",
    "Christmas" : "2021-12-27"
  } ],
  "isTheStockMarketOpen" : false
}
```
----
## GET /v3/delisted-companies <a name="0x59ae66e39460b5e996adc11a1f1073a9dbffdf1eeb5341ca0a0af2e550d1cfea"></a>

Access a list of delisted companies from the US exchanges.
Stock delisting is the removal of a recorded stock from a stock trade exchange, and accordingly it would presently don't be exchanged on the bourse.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/delisted-companies

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x59ae66e39460b5e996adc11a1f1073a9dbffdf1eeb5341ca0a0af2e550d1cfea

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
 {
  "symbol" : "AA-W",
  "companyName" : "Alcoa Corporation When Issued",
  "exchange" : "NYSE",
  "ipoDate" : "2016-10-18",
  "delistedDate" : "2016-11-08"
}, {
  "symbol" : "AAAP",
  "companyName" : "Advanced Accelerator Applications SA",
  "exchange" : "NASDAQ",
  "ipoDate" : "2015-11-11",
  "delistedDate" : "2018-02-20"
}, {
  "symbol" : "AABA",
  "companyName" : "Altaba Inc",
  "exchange" : "NASDAQ",
  "ipoDate" : "1996-04-12",
  "delistedDate" : "2019-11-06"
}, {
  "symbol" : "AAC",
  "companyName" : "American Addiction Centers",
  "exchange" : "NYSE",
  "ipoDate" : "2014-10-02",
  "delistedDate" : "2019-11-04"
}, { ... }
]
```
----
## GET /v4/articles <a name="0x92499117c90f908d061895ff836caecb00e58ee0f471e40a38032f2f68a053bd"></a>

Access Financial Modeling Prep own proprietary articles written by our analysts. New articles are being created everyday. This endpoint contains fields like image, tickers, content and more.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/fmp-articles

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x92499117c90f908d061895ff836caecb00e58ee0f471e40a38032f2f68a053bd

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
page : Number
size : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "content" : [
    {
      "title" : "Soros Fund Management Has Also Invested in Bitcoin",
      "date" : "2021-10-08 14:07:00",
      "content" : "<p>Bitcoin continues to trade around $54,000 today following its solid upsurge since the start of the month.</p>
<p>Dawn Fitzpatrick, the CEO and CIO of Soros Fund Management, founded by billionaire investor George Soros, said that they have also invested in Bitcoin and other digital currencies, as cryptos has gone mainstream and are not only viewed as an inflation hedge.</p>
<p>In March, Fitzpatrick commented on CBDCs, viewing them as a potential threat to Bitcoin, however noting that the threat will be temporary as she believes CBDCs won’t be successful in permanently destabilizing bitcoin.</p>
",
      "tickers" : "BTCUSD",
      "image" : "https://cdn.financialmodelingprep.com/images/fmp-1633716457854.jpg",
      "link" : "https://financialmodelingprep.com/market-news/fmp-soros-fund-management-has-also-invested-in-bitcoin",
      "author" : "Davit Kirakosyan",
      "site" : "Financial Modeling Prep"
    }, {
      "title" : "Allogene Therapeutics Shares Plunged 45% Following FDA’s Hold on AlloCAR T",
      "date" : "2021-10-08 13:06:00",
      "content" : "<p><a href='https://financialmodelingprep.com/financial-summary/ALLO'>Allogene Therapeutics, Inc. (NASDAQ:ALLO) </a>shares dropped more than 45% on Friday following the U.S. Food and Drug Administration’s (FDA) halt on the company’s AlloCAR T clinical trials after the detection of AlloCAR cells with chromosomal abnormality in a single patient treated with ALLO-501A. </p>
<p>Rafael Amado, Executive Vice President of Research and Development and Chief Medical Officer of Allogene, said that they will work closely with the FDA to determine the next steps for advancing ALLO-501A. As the company investigates the issue, the analysts at Oppenheimer think that there will be delayed development timelines for key programs including ALLO-501A and ALLO-715, estimating the holds to range from 3 to 6 months.</p>
<p>Following this announcement, the analysts lowered their price target on the company’s shares to $40 from $44, while maintaining their outperform rating.</p>
",
      "tickers" : "NASDAQ:ALLO",
      "image" : "https://cdn.financialmodelingprep.com/images/fmp-1633712793569.jpg",
      "link" : "https://financialmodelingprep.com/market-news/fmp-allogene-therapeutics-shares-plunged-45-following-fda’s-hold-on-allocar-t",
      "author" : "Davit Kirakosyan",
      "site" : "Financial Modeling Prep"
    }, ...
  ],
  "pageable" : {
    "sort" : {
      "sorted" : true,
      "unsorted" : false,
      "empty" : false
    },
    "pageSize" : 5,
    "pageNumber" : 0,
    "offset" : 0,
    "paged" : true,
    "unpaged" : false
  },
  "totalPages" : 30,
  "totalElements" : 150,
  "last" : false,
  "number" : 0,
  "size" : 5,
  "numberOfElements" : 5,
  "sort" : {
    "sorted" : true,
    "unsorted" : false,
    "empty" : false
  },
  "first" : true,
  "empty" : false
}
```
----
## GET /v3/stock_news <a name="0x3cc9821b6a5f6b8bdd6ca8c5e6be9465706f94a8c881dcf4100f360626309a9e"></a>

It returns the most recent news with parameters like image or url of the original article. If you only want news about specific stocks, you can use the tickers parameter. Since 2017, we've kept track of everything that's happened.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-news

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x3cc9821b6a5f6b8bdd6ca8c5e6be9465706f94a8c881dcf4100f360626309a9e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
tickers : String
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[
  {
    "symbol" : "AAPL",
    "publishedDate" : "2020-09-08 09:25:00",
    "title" : "This Is Not 1999",
    "image" : "https://static.seekingalpha.com/uploads/2020/9/4/33552555-1599243045230633_origin.png",
    "site" : "seekingalpha.com",
    "text" : "Investors compare 2020 to 1999 because it's the easy answer. Humans like easy answers - patterns - because it helps them assert control and make sense of the world.",
    "url" : "https://seekingalpha.com/article/4372707-this-is-not-1999"
  }, {
    "symbol" : "FB",
    "publishedDate" : "2020-09-08 09:00:00",
    "title" : "Facebook: 25% Upside As It Climbs To The Trillion Mark",
    "image" : "https://static3.seekingalpha.com/uploads/2020/9/5/12629971-15993371256494496.png",
    "site" : "seekingalpha.com",
    "text" : "FB is still a buy as 1/3rd of the global population uses its platforms, there is zero long-term debt on the balance sheet and FB continuously delivers significant growth.",
    "url" : "https://seekingalpha.com/article/4372906-facebook-25-upside-climbs-to-trillion-mark"
  }, {
    "symbol" : "AAPL",
    "publishedDate" : "2020-09-08 08:30:00",
    "title" : "Where Fundamentals Meet Technicals",
    "image" : "https://static1.seekingalpha.com/uploads/2020/9/5/saupload_full-7eadbf4ba925753fe35d3e2ab4b8c1ba798e4255.png",
    "site" : "seekingalpha.com",
    "text" : "Despite the recent dip, the S&P 500 doesn't have a great intermediate-term risk/reward profile, based on valuations or technicals.",
    "url" : "https://seekingalpha.com/article/4372997-where-fundamentals-meet-technicals"
  }, {
    "symbol" : "AMZN",
    "publishedDate" : "2020-09-08 07:50:05",
    "title" : "Amazon's Profits, AWS, And Advertising",
    "image" : "https://static2.seekingalpha.com/uploads/2020/9/8/saupload_Misc_slides.001.png",
    "site" : "seekingalpha.com",
    "text" : "The company’s sales keep going up, and it takes a larger and larger share of US retail every year (7-8% in 2019), but it never seems to make any money.",
    "url" : "https://seekingalpha.com/article/4372990-amazons-profits-aws-and-advertising"
  }, ...
]
```
----
## GET /v3/press-releases/{symbol} <a name="0xc34888ff56805321a7c2b650065753485a355c1ffc7e155d493dbe9f8278b30d"></a>

Companies usually communicate important information to the public through press releases. It could be a new product or financial results, for example. When they do this, we keep track of it and return the information from this endpoint.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/press-releases

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc34888ff56805321a7c2b650065753485a355c1ffc7e155d493dbe9f8278b30d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "symbol" : "AAPL",
    "date" : "2020-09-15 16:30:00",
    "title" : "Apple Inc Says New iPad Air Will Be Priced Starting At $599",
    "text" : "APPLE INC ANNOUNCES IPAD 8TH GENERATION STARTING WITH A12 BIONIC.APPLE INC SAYS PRICES OF NEW IPADS START AT $299 FOR EDUCATION CUSTOMERS.APPLE INC SAYS NEW IPAD AIR WILL BE PRICED AT BEGINNING $599.APPLE SAYS WILL RELEASE MAJOR IOS UPDATES ON WEDNESDAY."
  }, {
    "symbol" : "AAPL",
    "date" : "2020-09-08 17:30:00",
    "title" : "Apple Inc Files Counterclaims Against Epic, Seeks Damages",
    "text" : "APPLE INC FILES COUNTERCLAIMS AGAINST EPIC, AND IS SEEKING DAMAGES AND DISGORGEMENT OF EARNINGS, PROFIT COMPENSATION.APPLE INC COUNTERCOMPLAINT SEEKS A PERMANENT INJUNCTION AGAINST CONTINUED OPERATION OF EPIC'S UNAUTHORIZED PAYMENT MECHANISM."
  }, {
    "symbol" : "AAPL",
    "date" : "2020-09-04 01:30:00",
    "title" : "Apple Commits To Freedom Of Speech After Criticism Of China Censorship - FT",
    "text" : "APPLE COMMITS TO FREEDOM OF SPEECH AFTER CRITICISM OF CHINA CENSORSHIP - FT.APPLE IS “COMMITTED TO RESPECTING THE HUMAN RIGHTS OF EVERYONE WHOSE LIVES WE TOUCH  INCLUDING OUR EMPLOYEES, SUPPLIERS, CONTRACTORS AND CUSTOMERS” - FT, CITING DOCUMENT."
  }, ...
]
```
----
## GET /v4/sector_price_earning_ratio <a name="0xea1299fa30035cf94bb01f94d040926e7966747934d394a4f91a3ae207e27813"></a>

Our API calculates sector PE ratios from companies in a specific sector on a daily basis. You can use this to compare other companies to the average pe for their industry.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/sectors-pe-ratio

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xea1299fa30035cf94bb01f94d040926e7966747934d394a4f91a3ae207e27813

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date : YYYY-MM-DD
exchange : String
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "date" : "2021-05-07",
  "sector" : "Basic Materials",
  "exchange" : "NYSE",
  "pe" : "52.5766227276190392"
}, {
  "date" : "2021-05-07",
  "sector" : "Communication Services",
  "exchange" : "NYSE",
  "pe" : "26.2022392285714183"
}, {
  "date" : "2021-05-07",
  "sector" : "Consumer Cyclical",
  "exchange" : "NYSE",
  "pe" : "62.1420462666666751"
}, {
  "date" : "2021-05-07",
  "sector" : "Consumer Defensive",
  "exchange" : "NYSE",
  "pe" : "76.1478811079999645"
}, {
  "date" : "2021-05-07",
  "sector" : "Energy",
  "exchange" : "NYSE",
  "pe" : "152.087980826190488"
}, {
  "date" : "2021-05-07",
  "sector" : "Financial Services",
  "exchange" : "NYSE",
  "pe" : "33.2373039483871153"
}, {
  "date" : "2021-05-07",
  "sector" : "Healthcare",
  "exchange" : "NYSE",
  "pe" : "40.6311915389610405"
}, {
  "date" : "2021-05-07",
  "sector" : "Industrials",
  "exchange" : "NYSE",
  "pe" : "55.3028414118181928"
}, {
  "date" : "2021-05-07",
  "sector" : "Real Estate",
  "exchange" : "NYSE",
  "pe" : "65.8221667666666548"
}, {
  "date" : "2021-05-07",
  "sector" : "Technology",
  "exchange" : "NYSE",
  "pe" : "63.0115322481481428"
}, {
  "date" : "2021-05-07",
  "sector" : "Utilities",
  "exchange" : "NYSE",
  "pe" : "29.8290601925675745"
} ]
```
----
## GET /v4/industry_price_earning_ratio <a name="0x2717b835e234a48fc40947bad9278af346f58e30661175d63b53a0d6803bd8ce"></a>

Industries The PE average is calculated using companies that are grouped by industry. This endpoint is updated on a daily basis, allowing you to look back at historical data. Divide the price by the earnings per share, or EPS, to get the price-to-earnings ratio, or PE.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/industries-pe-ratio

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x2717b835e234a48fc40947bad9278af346f58e30661175d63b53a0d6803bd8ce

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
date : YYYY-MM-DD
exchange : String
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "date" : "2021-05-07",
  "industry" : "Auto Manufacturers",
  "exchange" : "NYSE",
  "pe" : "62.1420462666666751"
}, {
  "date" : "2021-05-07",
  "industry" : "Banks Diversified",
  "exchange" : "NYSE",
  "pe" : "33.2373039483871153"
}, {
  "date" : "2021-05-07",
  "industry" : "Computer Hardware",
  "exchange" : "NYSE",
  "pe" : "63.0115322481481428"
}, {
  "date" : "2021-05-07",
  "industry" : "Drug Manufacturers General",
  "exchange" : "NYSE",
  "pe" : "40.6311915389610405"
}, {
  "date" : "2021-05-07",
  "industry" : "Household & Personal Products",
  "exchange" : "NYSE",
  "pe" : "76.1478811079999645"
}, {
  "date" : "2021-05-07",
  "industry" : "Metals & Mining",
  "exchange" : "NYSE",
  "pe" : "52.5766227276190392"
}, {
  "date" : "2021-05-07",
  "industry" : "Oil & Gas Midstream",
  "exchange" : "NYSE",
  "pe" : "152.087980826190488"
}, {
  "date" : "2021-05-07",
  "industry" : "REIT Diversified",
  "exchange" : "NYSE",
  "pe" : "65.8221667666666548"
}, {
  "date" : "2021-05-07",
  "industry" : "Telecom Services",
  "exchange" : "NYSE",
  "pe" : "26.2022392285714183"
}, {
  "date" : "2021-05-07",
  "industry" : "Trucking",
  "exchange" : "NYSE",
  "pe" : "55.3028414118181928"
}, {
  "date" : "2021-05-07",
  "industry" : "Utilities Diversified",
  "exchange" : "NYSE",
  "pe" : "29.8290601925675745"
} ]
```
----
## GET /v3/sectors-performance <a name="0x1dac39aab45ce2908ef9f8885c7f368c52cce25633f41c42cceb6ae122a6c408"></a>

Check out performance by sector to see which one performs the best. You can find companies in each of the sectors using our stock screener. It's based on the percent change in each sector's companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-market-sector-performance-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x1dac39aab45ce2908ef9f8885c7f368c52cce25633f41c42cceb6ae122a6c408

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "sectorPerformance" : [ {
    "sector" : "Basic Materials",
    "changesPercentage" : "0.0546%"
  }, {
    "sector" : "Communication Services",
    "changesPercentage" : "-0.1645%"
  }, {
    "sector" : "Conglomerates",
    "changesPercentage" : "0.0000%"
  }, {
    "sector" : "Consumer Cyclical",
    "changesPercentage" : "-0.0018%"
  }, {
    "sector" : "Consumer Defensive",
    "changesPercentage" : "-0.1199%"
  }, {
    "sector" : "Energy",
    "changesPercentage" : "-0.6984%"
  }, {
    "sector" : "Financial",
    "changesPercentage" : "0.1233%"
  }, {
    "sector" : "Financial Services",
    "changesPercentage" : "-0.0211%"
  }, {
    "sector" : "Healthcare",
    "changesPercentage" : "-0.1698%"
  }, {
    "sector" : "Industrial Goods",
    "changesPercentage" : "2.2278%"
  }, {
    "sector" : "Industrials",
    "changesPercentage" : "-0.1186%"
  }, {
    "sector" : "Real Estate",
    "changesPercentage" : "0.1093%"
  }, {
    "sector" : "Services",
    "changesPercentage" : "0.0000%"
  }, {
    "sector" : "Technology",
    "changesPercentage" : "0.1022%"
  }, {
    "sector" : "Utilities",
    "changesPercentage" : "0.4557%"
  } ]
}
```
----
## GET /v3/historical-sectors-performance <a name="0xda2e2fbf813778cd01bcf722b2b5871720793e8e0954043185ef620395e14d0d"></a>

Check out performance by sector to see which one performs the best. You can find companies in each of the sectors using our stock screener. It's based on the percent change in each sector's companies.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-market-sector-performance-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xda2e2fbf813778cd01bcf722b2b5871720793e8e0954043185ef620395e14d0d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "sectorPerformance" : [ {
    "sector" : "Basic Materials",
    "changesPercentage" : "0.0546%"
  }, {
    "sector" : "Communication Services",
    "changesPercentage" : "-0.1645%"
  }, {
    "sector" : "Conglomerates",
    "changesPercentage" : "0.0000%"
  }, {
    "sector" : "Consumer Cyclical",
    "changesPercentage" : "-0.0018%"
  }, {
    "sector" : "Consumer Defensive",
    "changesPercentage" : "-0.1199%"
  }, {
    "sector" : "Energy",
    "changesPercentage" : "-0.6984%"
  }, {
    "sector" : "Financial",
    "changesPercentage" : "0.1233%"
  }, {
    "sector" : "Financial Services",
    "changesPercentage" : "-0.0211%"
  }, {
    "sector" : "Healthcare",
    "changesPercentage" : "-0.1698%"
  }, {
    "sector" : "Industrial Goods",
    "changesPercentage" : "2.2278%"
  }, {
    "sector" : "Industrials",
    "changesPercentage" : "-0.1186%"
  }, {
    "sector" : "Real Estate",
    "changesPercentage" : "0.1093%"
  }, {
    "sector" : "Services",
    "changesPercentage" : "0.0000%"
  }, {
    "sector" : "Technology",
    "changesPercentage" : "0.1022%"
  }, {
    "sector" : "Utilities",
    "changesPercentage" : "0.4557%"
  } ]
}
```
----
## GET /v3/gainers <a name="0x0eb26c96bd29e0a63458f325fcf1c61cbd8fe4cca4efa29581dd32f8e8687983"></a>

The biggest percentage change in supported stocks returns the most gainers. As fields, it returns the ticker, name, change, and percentage change. There's a reason those stocks are rising, and you'll probably find it on our news endpoint.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/most-gainers-stock-market-data-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x0eb26c96bd29e0a63458f325fcf1c61cbd8fe4cca4efa29581dd32f8e8687983

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "mostGainerStock" : [
    {
      "ticker" : "NVR",
      "changes" : 15.03,
      "price" : "3782.25",
      "changesPercentage" : "(+0.40%)",
      "companyName" : "NVR Inc."
    }, {
      "ticker" : "WTM",
      "changes" : 8.31,
      "price" : "1113.9",
      "changesPercentage" : "(+0.75%)",
      "companyName" : "White Mountains Insurance Group Ltd."
    }, {
      "ticker" : "TPL",
      "changes" : 8.06,
      "price" : "806.95",
      "changesPercentage" : "(+1.01%)",
      "companyName" : "Texas Pacific Land Trust"
    }, {
      "ticker" : "RUSL",
      "changes" : 5.75,
      "price" : "77.99",
      "changesPercentage" : "(+7.95%)",
      "companyName" : "Direxion Daily Russia Bull 3x Shares"
    }, {
      "ticker" : "CSGP",
      "changes" : 3.54,
      "price" : "645.7",
      "changesPercentage" : "(+0.55%)",
      "companyName" : "CoStar Group Inc."
    }, {
      "ticker" : "FLRU",
      "changes" : 3.15,
      "price" : "30.8",
      "changesPercentage" : "(+11.37%)",
      "companyName" : "Franklin FTSE Russia"
    }, {
      "ticker" : "TSLA",
      "changes" : 1.59,
      "price" : "478.48",
      "changesPercentage" : "(+0.33%)",
      "companyName" : "Tesla Inc."
    }
  ]
}
```
----
## GET /v3/losers <a name="0x392ec92746669d2a0d28730830d9bf1e624d6ab5d5738b80214c80fea4dbbb65"></a>

The most negative percent change of all supported stocks is returned by this endpoint. It returns ticker, name, change, and percentage change as fields. Normal stocks, mutual funds, etfs, and other securities can be among the tickers returned. As a result, 3X Bull/Bear ETFs may occasionally appear on the list.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/most-losers-stock-market-data-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x392ec92746669d2a0d28730830d9bf1e624d6ab5d5738b80214c80fea4dbbb65

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "mostLoserStock" : [
    {
      "ticker" : "SEB",
      "changes" : -23.16,
      "price" : "4165",
      "changesPercentage" : "(-0.55%)",
      "companyName" : "Seaboard Corporation"
    }, {
      "ticker" : "GHC",
      "changes" : -3.76,
      "price" : "615.62",
      "changesPercentage" : "(-0.61%)",
      "companyName" : "Graham Holdings Company"
    }, {
      "ticker" : "NWLI",
      "changes" : -2.98,
      "price" : "283.04",
      "changesPercentage" : "(-1.04%)",
      "companyName" : "National Western Life Group Inc."
    }, {
      "ticker" : "AZO",
      "changes" : -2.89,
      "price" : "1131.86",
      "changesPercentage" : "(-0.25%)",
      "companyName" : "AutoZone Inc."
    }, {
      "ticker" : "MKTX",
      "changes" : -2.49,
      "price" : "362.66",
      "changesPercentage" : "(-0.68%)",
      "companyName" : "MarketAxess Holdings Inc."
    }, {
      "ticker" : "NEU",
      "changes" : -2.38,
      "price" : "458.79",
      "changesPercentage" : "(-0.52%)",
      "companyName" : "NewMarket Corp"
    },
  ]
}
```
----
## GET /v3/actives <a name="0xebf4654d7c1a9224bd1b1ae7a27e0ea9b70f5e16b115d6ecc7803ed46e96b8ab"></a>

The most actively traded stocks are those with the highest volume of trades per day. This endpoint could be used to find hedge funds/mutual funds that are loading up on certain stocks or to find stocks that are trending today.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/most-actives-stock-market-data-free-api

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xebf4654d7c1a9224bd1b1ae7a27e0ea9b70f5e16b115d6ecc7803ed46e96b8ab

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
{
  "mostActiveStock" : [
    {
      "ticker" : "SEB",
      "changes" : -23.16,
      "price" : "4165",
      "changesPercentage" : "(-0.55%)",
      "companyName" : "Seaboard Corporation"
    }, {
      "ticker" : "NVR",
      "changes" : 15.03,
      "price" : "3782.25",
      "changesPercentage" : "(+0.40%)",
      "companyName" : "NVR Inc."
    }, {
      "ticker" : "WTM",
      "changes" : 8.31,
      "price" : "1113.9",
      "changesPercentage" : "(+0.75%)",
      "companyName" : "White Mountains Insurance Group Ltd."
    }, {
      "ticker" : "TPL",
      "changes" : 8.06,
      "price" : "806.95",
      "changesPercentage" : "(+1.01%)",
      "companyName" : "Texas Pacific Land Trust"
    }, {
      "ticker" : "RUSL",
      "changes" : 5.75,
      "price" : "77.99",
      "changesPercentage" : "(+7.95%)",
      "companyName" : "Direxion Daily Russia Bull 3x Shares"
    }, {
      "ticker" : "GHC",
      "changes" : -3.76,
      "price" : "615.62",
      "changesPercentage" : "(-0.61%)",
      "companyName" : "Graham Holdings Company"
    }, ...
  ]
}
```
----
## GET /v4/standard_industrial_classification <a name="0xc34c5cca5d18714d71f6a77b6f35b0a1dd3d018bf9df9aaadada6d84bb5b380a"></a>

SIC is a code given by US government to companies according to their business. Its mosly for US companies but also some other countries adopted this too. SIC is mostly used by SEC. It returns code but also the industry title.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/standard-industrial-classification

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc34c5cca5d18714d71f6a77b6f35b0a1dd3d018bf9df9aaadada6d84bb5b380a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
cik : Number
sic : Number
industryTitle : String
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "name" : "Apple Inc. ",
  "cik" : "0000320193",
  "sicCode" : "3571",
  "industryTitle" : "ELECTRONIC COMPUTERS",
  "businessAdress" : "['ONE APPLE PARK WAY', 'CUPERTINO CA 95014']",
  "phoneNumber" : "(408) 996-1010"
} ]
```
----
## GET /v4/standard_industrial_classification/all <a name="0xbac4d7a5a482602d0a6dddf13b8ec593e7fd554121d102810b930902a148e845"></a>

Every Standard Industrial Classification available.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/standard-industrial-classification

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xbac4d7a5a482602d0a6dddf13b8ec593e7fd554121d102810b930902a148e845

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "name" : "Apple Inc. ",
  "cik" : "0000320193",
  "sicCode" : "3571",
  "industryTitle" : "ELECTRONIC COMPUTERS",
  "businessAdress" : "['ONE APPLE PARK WAY', 'CUPERTINO CA 95014']",
  "phoneNumber" : "(408) 996-1010"
} ]
```
----
## GET /v4/standard_industrial_classification_list <a name="0xe03fe1ca41560488cd4a10dbbbbfa25c980f5e323895d987a3f64557f7f8ffc2"></a>

SIC is a code given by US government to companies according to their business. Its mosly for US companies but also some other countries adopted this too. SIC is mostly used by SEC. It returns code but also the industry title.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/standard-industrial-classification#Standard-Industrial-Classification-List

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xe03fe1ca41560488cd4a10dbbbbfa25c980f5e323895d987a3f64557f7f8ffc2

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
cik : Number
sic : Number
industryTitle : String 
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "name" : "Apple Inc. ",
  "cik" : "0000320193",
  "sicCode" : "3571",
  "industryTitle" : "ELECTRONIC COMPUTERS",
  "businessAdress" : "['ONE APPLE PARK WAY', 'CUPERTINO CA 95014']",
  "phoneNumber" : "(408) 996-1010"
} ]
```
----
## GET /v4/commitment_of_traders_report/list <a name="0x6b60d1199f4ec6b2488b63e4d39fa211753ce6f9b5c4f8897b21ec1ea8487f6e"></a>

Access the full COT report components
You will be able to see all COT components individually to be able to call our the COT report API with specific symbols.
The COT report also give insight about BITCOIN, if you need to have deeper insight about currency you can access it via our Cryptocurrency Free API to get access a list of all major crypto currencies, price are updated in realtime. Major crypto included Bitcoins, Ethereum, Ripple, EOS, Cardano, Bitcoin Cash.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/cot-symbols-list

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6b60d1199f4ec6b2488b63e4d39fa211753ce6f9b5c4f8897b21ec1ea8487f6e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
None
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ 
  {
    "trading_symbol" : "M6",
    "short_name" : "Mexican Peso (M6)"
  }, {
    "trading_symbol" : "NG",
    "short_name" : "Natural Gas (NG)"
  }, {
    "short_name" : "Ultra 10-Year T-Note (TN)",
    "trading_symbol" : "TN"
  }, {
    "trading_symbol" : "A6",
    "short_name" : "Australian Dollar (A6)"
  }, {
    "trading_symbol" : "NQ",
    "short_name" : "Nasdaq 100 E-Mini (NQ)"
  }, {
    "trading_symbol" : "PA",
    "short_name" : "Palladium (PA)"
  }, ...
]
```
----
## GET /v4/commitment_of_traders_report <a name="0xc3677a186218cf337748b18ff482711c3554882872ebab1067e04c2007c97432"></a>

The Commitments of Traders (COT report) is a weekly market report from the Commodity Futures Trading Commission (CFTC) enumerating the holdings of participants in various markets in the United States.
This information is very valuable to understand the Major market players position in futures, Forex and Commodities. 

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/cot-reports

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc3677a186218cf337748b18ff482711c3554882872ebab1067e04c2007c97432

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ 
  {
    "symbol" : "ZW",
    "date" : "2020-12-29 00:00:00",
    "short_name" : "Wheat (ZW)",
    "sector" : "GRAINS",
    "market_and_exchange_names" : "BLACK SEA WHEAT FINANCIAL - CHICAGO BOARD OF TRADE",
    "as_of_date_in_form_yymmdd" : "201229",
    "cftc_contract_market_code" : "00160F",
    "cftc_market_code" : "CBT ",
    "cftc_region_code" : "0",
    "cftc_commodity_code" : "1",
    "open_interest_all" : 22428,
    "noncomm_positions_long_all" : 10497,
    "noncomm_positions_short_all" : 300,
    "noncomm_postions_spread_all" : 593,
    "comm_positions_long_all" : 10093,
    "comm_positions_short_all" : 20487,
    "tot_rept_positions_long_all" : 21183,
    "tot_rept_positions_short_all" : 21380,
    "nonrept_positions_long_all" : 1245,
    "nonrept_positions_short_all" : 1048,
    "open_interest_old" : 18385,
    "noncomm_positions_long_old" : 8913,
    "noncomm_positions_short_old" : 300,
    "noncomm_positions_spread_old" : 0,
    "comm_positions_long_old" : 9102,
    "comm_positions_short_old" : 17365,
    "tot_rept_positions_long_old" : 18015,
    "tot_rept_positions_short_old" : 17665,
    "nonrept_positions_long_old" : 370,
    "nonrept_positions_short_old" : 720,
    "open_interest_other" : 4043,
    "noncomm_positions_long_other" : 2177,
    "noncomm_positions_short_other" : 593,
    "noncomm_positions_spread_other" : 0,
    "comm_positions_long_other" : 991,
    "comm_positions_short_other" : 3122,
    "tot_rept_positions_long_other" : 3168,
    "tot_rept_positions_short_other" : 3715,
    "nonrept_positions_long_other" : 875,
    "nonrept_positions_short_other" : 328,
    "change_in_open_interest_all" : -557,
    "change_in_noncomm_long_all" : -420,
    "change_in_noncomm_short_all" : -209,
    "change_in_noncomm_spead_all" : -332,
    "change_in_comm_long_all" : 3,
    "change_in_comm_short_all" : -300,
    "change_in_tot_rept_long_all" : -749,
    "change_in_tot_rept_short_all" : -841,
    "change_in_nonrept_long_all" : 192,
    "change_in_nonrept_short_all" : 284,
    "pct_of_open_interest_all" : 100,
    "pct_of_oi_noncomm_long_all" : 46.7999999999999972,
    "pct_of_oi_noncomm_short_all" : 1.30000000000000004,
    "pct_of_oi_noncomm_spread_all" : 2.60000000000000009,
    "pct_of_oi_comm_long_all" : 45,
    "pct_of_oi_comm_short_all" : 91.2999999999999972,
    "pct_of_oi_tot_rept_long_all" : 94.4000000000000057,
    "pct_of_oi_tot_rept_short_all" : 95.2999999999999972,
    "pct_of_oi_nonrept_long_all" : 5.59999999999999964,
    "pct_of_oi_nonrept_short_all" : 4.70000000000000018,
    "pct_of_open_interest_ol" : 100,
    "pct_of_oi_noncomm_long_ol" : 48.5,
    "pct_of_oi_noncomm_short_ol" : 1.60000000000000009,
    "pct_of_oi_noncomm_spread_ol" : 0,
    "pct_of_oi_comm_long_ol" : 49.5,
    "pct_of_oi_comm_short_ol" : 94.5,
    "pct_of_oi_tot_rept_long_ol" : 98,
    "pct_of_oi_tot_rept_short_ol" : 96.0999999999999943,
    "pct_of_oi_nonrept_long_ol" : 2,
    "pct_of_oi_nonrept_short_ol" : 3.89999999999999991,
    "pct_of_open_interest_other" : 100,
    "pct_of_oi_noncomm_long_other" : 53.7999999999999972,
    "pct_of_oi_noncomm_short_other" : 14.6999999999999993,
    "pct_of_oi_noncomm_spread_other" : 0,
    "pct_of_oi_comm_long_other" : 24.5,
    "pct_of_oi_comm_short_other" : 77.2000000000000028,
    "pct_of_oi_tot_rept_long_other" : 78.4000000000000057,
    "pct_of_oi_tot_rept_short_other" : 91.9000000000000057,
    "pct_of_oi_nonrept_long_other" : 21.6000000000000014,
    "pct_of_oi_nonrept_short_other" : 8.09999999999999964,
    "traders_tot_all" : 25,
    "traders_noncomm_long_all" : 4,
    "traders_noncomm_short_all" : 1,
    "traders_noncomm_spread_all" : 1,
    "traders_comm_long_all" : 10,
    "traders_comm_short_all" : 18,
    "traders_tot_rept_long_all" : 14,
    "traders_tot_rept_short_all" : 20,
    "traders_tot_ol" : 24,
    "traders_noncomm_long_ol" : 3,
    "traders_noncomm_short_ol" : 1,
    "traders_noncomm_spead_ol" : 0,
    "traders_comm_long_ol" : 8,
    "traders_comm_short_ol" : 17,
    "traders_tot_rept_long_ol" : 11,
    "traders_tot_rept_short_ol" : 18,
    "traders_tot_other" : 13,
    "traders_noncomm_long_other" : 2,
    "traders_noncomm_short_other" : 1,
    "traders_noncomm_spread_other" : 0,
    "traders_comm_long_other" : 5,
    "traders_comm_short_other" : 8,
    "traders_tot_rept_long_other" : 7,
    "traders_tot_rept_short_other" : 9,
    "conc_gross_le_4_tdr_long_all" : 72.2000000000000028,
    "conc_gross_le_4_tdr_short_all" : 35.1000000000000014,
    "conc_gross_le_8_tdr_long_all" : 90.5,
    "conc_gross_le_8_tdr_short_all" : 62.5,
    "conc_net_le_4_tdr_long_all" : 62.2999999999999972,
    "conc_net_le_4_tdr_short_all" : 34.3999999999999986,
    "conc_net_le_8_tdr_long_all" : 72.4000000000000057,
    "conc_net_le_8_tdr_short_all" : 54.3999999999999986,
    "conc_gross_le_4_tdr_long_ol" : 84.2000000000000028,
    "conc_gross_le_4_tdr_short_ol" : 40.1000000000000014,
    "conc_gross_le_8_tdr_long_ol" : 97.0999999999999943,
    "conc_gross_le_8_tdr_short_ol" : 67.2000000000000028,
    "conc_net_le_4_tdr_long_ol" : 72,
    "conc_net_le_4_tdr_short_ol" : 40.1000000000000014,
    "conc_net_le_8_tdr_long_ol" : 79.9000000000000057,
    "conc_net_le_8_tdr_short_ol" : 62.5,
    "conc_gross_le_4_tdr_long_other" : 72.9000000000000057,
    "conc_gross_le_4_tdr_short_other" : 54.5,
    "conc_gross_le_8_tdr_long_other" : 78.4000000000000057,
    "conc_gross_le_8_tdr_short_other" : 87.9000000000000057,
    "conc_net_le_4_tdr_long_other" : 65.4000000000000057,
    "conc_net_le_4_tdr_short_other" : 49.2999999999999972,
    "conc_net_le_8_tdr_long_other" : 65.4000000000000057,
    "conc_net_le_8_tdr_short_other" : 75,
    "contract_units" : "50 Metric Tons"
  }, ...
]
```
----
## GET /v4/commitment_of_traders_report/{symbol} <a name="0x64864439ea51c270825cdd137ac2473f3aa1530d213af05400ca9869c8726fca"></a>

List of reports for specific symbol.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/cot-reports

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x64864439ea51c270825cdd137ac2473f3aa1530d213af05400ca9869c8726fca

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ 
  {
    "symbol" : "ZW",
    "date" : "2020-12-29 00:00:00",
    "short_name" : "Wheat (ZW)",
    "sector" : "GRAINS",
    "market_and_exchange_names" : "BLACK SEA WHEAT FINANCIAL - CHICAGO BOARD OF TRADE",
    "as_of_date_in_form_yymmdd" : "201229",
    "cftc_contract_market_code" : "00160F",
    "cftc_market_code" : "CBT ",
    "cftc_region_code" : "0",
    "cftc_commodity_code" : "1",
    "open_interest_all" : 22428,
    "noncomm_positions_long_all" : 10497,
    "noncomm_positions_short_all" : 300,
    "noncomm_postions_spread_all" : 593,
    "comm_positions_long_all" : 10093,
    "comm_positions_short_all" : 20487,
    "tot_rept_positions_long_all" : 21183,
    "tot_rept_positions_short_all" : 21380,
    "nonrept_positions_long_all" : 1245,
    "nonrept_positions_short_all" : 1048,
    "open_interest_old" : 18385,
    "noncomm_positions_long_old" : 8913,
    "noncomm_positions_short_old" : 300,
    "noncomm_positions_spread_old" : 0,
    "comm_positions_long_old" : 9102,
    "comm_positions_short_old" : 17365,
    "tot_rept_positions_long_old" : 18015,
    "tot_rept_positions_short_old" : 17665,
    "nonrept_positions_long_old" : 370,
    "nonrept_positions_short_old" : 720,
    "open_interest_other" : 4043,
    "noncomm_positions_long_other" : 2177,
    "noncomm_positions_short_other" : 593,
    "noncomm_positions_spread_other" : 0,
    "comm_positions_long_other" : 991,
    "comm_positions_short_other" : 3122,
    "tot_rept_positions_long_other" : 3168,
    "tot_rept_positions_short_other" : 3715,
    "nonrept_positions_long_other" : 875,
    "nonrept_positions_short_other" : 328,
    "change_in_open_interest_all" : -557,
    "change_in_noncomm_long_all" : -420,
    "change_in_noncomm_short_all" : -209,
    "change_in_noncomm_spead_all" : -332,
    "change_in_comm_long_all" : 3,
    "change_in_comm_short_all" : -300,
    "change_in_tot_rept_long_all" : -749,
    "change_in_tot_rept_short_all" : -841,
    "change_in_nonrept_long_all" : 192,
    "change_in_nonrept_short_all" : 284,
    "pct_of_open_interest_all" : 100,
    "pct_of_oi_noncomm_long_all" : 46.7999999999999972,
    "pct_of_oi_noncomm_short_all" : 1.30000000000000004,
    "pct_of_oi_noncomm_spread_all" : 2.60000000000000009,
    "pct_of_oi_comm_long_all" : 45,
    "pct_of_oi_comm_short_all" : 91.2999999999999972,
    "pct_of_oi_tot_rept_long_all" : 94.4000000000000057,
    "pct_of_oi_tot_rept_short_all" : 95.2999999999999972,
    "pct_of_oi_nonrept_long_all" : 5.59999999999999964,
    "pct_of_oi_nonrept_short_all" : 4.70000000000000018,
    "pct_of_open_interest_ol" : 100,
    "pct_of_oi_noncomm_long_ol" : 48.5,
    "pct_of_oi_noncomm_short_ol" : 1.60000000000000009,
    "pct_of_oi_noncomm_spread_ol" : 0,
    "pct_of_oi_comm_long_ol" : 49.5,
    "pct_of_oi_comm_short_ol" : 94.5,
    "pct_of_oi_tot_rept_long_ol" : 98,
    "pct_of_oi_tot_rept_short_ol" : 96.0999999999999943,
    "pct_of_oi_nonrept_long_ol" : 2,
    "pct_of_oi_nonrept_short_ol" : 3.89999999999999991,
    "pct_of_open_interest_other" : 100,
    "pct_of_oi_noncomm_long_other" : 53.7999999999999972,
    "pct_of_oi_noncomm_short_other" : 14.6999999999999993,
    "pct_of_oi_noncomm_spread_other" : 0,
    "pct_of_oi_comm_long_other" : 24.5,
    "pct_of_oi_comm_short_other" : 77.2000000000000028,
    "pct_of_oi_tot_rept_long_other" : 78.4000000000000057,
    "pct_of_oi_tot_rept_short_other" : 91.9000000000000057,
    "pct_of_oi_nonrept_long_other" : 21.6000000000000014,
    "pct_of_oi_nonrept_short_other" : 8.09999999999999964,
    "traders_tot_all" : 25,
    "traders_noncomm_long_all" : 4,
    "traders_noncomm_short_all" : 1,
    "traders_noncomm_spread_all" : 1,
    "traders_comm_long_all" : 10,
    "traders_comm_short_all" : 18,
    "traders_tot_rept_long_all" : 14,
    "traders_tot_rept_short_all" : 20,
    "traders_tot_ol" : 24,
    "traders_noncomm_long_ol" : 3,
    "traders_noncomm_short_ol" : 1,
    "traders_noncomm_spead_ol" : 0,
    "traders_comm_long_ol" : 8,
    "traders_comm_short_ol" : 17,
    "traders_tot_rept_long_ol" : 11,
    "traders_tot_rept_short_ol" : 18,
    "traders_tot_other" : 13,
    "traders_noncomm_long_other" : 2,
    "traders_noncomm_short_other" : 1,
    "traders_noncomm_spread_other" : 0,
    "traders_comm_long_other" : 5,
    "traders_comm_short_other" : 8,
    "traders_tot_rept_long_other" : 7,
    "traders_tot_rept_short_other" : 9,
    "conc_gross_le_4_tdr_long_all" : 72.2000000000000028,
    "conc_gross_le_4_tdr_short_all" : 35.1000000000000014,
    "conc_gross_le_8_tdr_long_all" : 90.5,
    "conc_gross_le_8_tdr_short_all" : 62.5,
    "conc_net_le_4_tdr_long_all" : 62.2999999999999972,
    "conc_net_le_4_tdr_short_all" : 34.3999999999999986,
    "conc_net_le_8_tdr_long_all" : 72.4000000000000057,
    "conc_net_le_8_tdr_short_all" : 54.3999999999999986,
    "conc_gross_le_4_tdr_long_ol" : 84.2000000000000028,
    "conc_gross_le_4_tdr_short_ol" : 40.1000000000000014,
    "conc_gross_le_8_tdr_long_ol" : 97.0999999999999943,
    "conc_gross_le_8_tdr_short_ol" : 67.2000000000000028,
    "conc_net_le_4_tdr_long_ol" : 72,
    "conc_net_le_4_tdr_short_ol" : 40.1000000000000014,
    "conc_net_le_8_tdr_long_ol" : 79.9000000000000057,
    "conc_net_le_8_tdr_short_ol" : 62.5,
    "conc_gross_le_4_tdr_long_other" : 72.9000000000000057,
    "conc_gross_le_4_tdr_short_other" : 54.5,
    "conc_gross_le_8_tdr_long_other" : 78.4000000000000057,
    "conc_gross_le_8_tdr_short_other" : 87.9000000000000057,
    "conc_net_le_4_tdr_long_other" : 65.4000000000000057,
    "conc_net_le_4_tdr_short_other" : 49.2999999999999972,
    "conc_net_le_8_tdr_long_other" : 65.4000000000000057,
    "conc_net_le_8_tdr_short_other" : 75,
    "contract_units" : "50 Metric Tons"
  }, ...
]
```
----
## GET /v4/commitment_of_traders_report_analysis <a name="0x7253ff38494d9dd0e61427a1962dc8bf78625d68eac17d154f028481822bb81d"></a>

The Commitments of Traders (COT report) Analysis is a complete analysis of the COT reports.
This analysis is done weekly as soon as the Commitments of Traders is published. 

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/cot-reports-analysis

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x7253ff38494d9dd0e61427a1962dc8bf78625d68eac17d154f028481822bb81d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
from : YYYY-MM-DD
to : YYYY-MM-DD
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ 
  {
    "symbol" : "E6",
    "date" : "2020-12-29 00:00:00",
    "name" : "Euro FX (E6)",
    "sector" : "CURRENCIES",
    "exchange" : "EURO FX - CHICAGO MERCANTILE EXCHANGE",
    "currentLongMarketSituation" : 73.6400000000000006,
    "currentShortMarketSituation" : 26.3599999999999994,
    "marketSituation" : "Bullish",
    "previousLongMarketSituation" : 73.9099999999999966,
    "previousShortMarketSituation" : 26.0899999999999999,
    "previousMarketSituation" : "Bullish",
    "netPostion" : 143076,
    "previousNetPosition" : 143902,
    "changeInNetPosition" : -0.569999999999999951,
    "marketSentiment" : "Increasing Bearish",
    "reversalTrend" : false
  }, {
    "symbol" : "LS",
    "date" : "2020-12-29 00:00:00",
    "name" : "Lumber (LS)",
    "sector" : "SOFTS",
    "exchange" : "RANDOM LENGTH LUMBER - CHICAGO MERCANTILE EXCHANGE",
    "currentLongMarketSituation" : 64.9500000000000028,
    "currentShortMarketSituation" : 35.0499999999999972,
    "marketSituation" : "Bullish",
    "previousLongMarketSituation" : 64.6800000000000068,
    "previousShortMarketSituation" : 35.3200000000000003,
    "previousMarketSituation" : "Bullish",
    "netPostion" : 319,
    "previousNetPosition" : 321,
    "changeInNetPosition" : -0.619999999999999996,
    "marketSentiment" : "Increasing Bearish",
    "reversalTrend" : false
  }, ...
]
```
----
## GET /v4/commitment_of_traders_report_analysis/{symbol} <a name="0xde76a38d22c137626be9db37420ed7e5e6f9fadebd2a0c83fc0434d4723331f3"></a>

Analysis of reports for trading symbol.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/cot-reports-analysis

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xde76a38d22c137626be9db37420ed7e5e6f9fadebd2a0c83fc0434d4723331f3

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "symbol" : "E6",
    "date" : "2020-12-29 00:00:00",
    "name" : "Euro FX (E6)",
    "sector" : "CURRENCIES",
    "exchange" : "EURO FX - CHICAGO MERCANTILE EXCHANGE",
    "currentLongMarketSituation" : 73.6400000000000006,
    "currentShortMarketSituation" : 26.3599999999999994,
    "marketSituation" : "Bullish",
    "previousLongMarketSituation" : 73.9099999999999966,
    "previousShortMarketSituation" : 26.0899999999999999,
    "previousMarketSituation" : "Bullish",
    "netPostion" : 143076,
    "previousNetPosition" : 143902,
    "changeInNetPosition" : -0.569999999999999951,
    "marketSentiment" : "Increasing Bearish",
    "reversalTrend" : false
  }, {
    "symbol" : "LS",
    "date" : "2020-12-29 00:00:00",
    "name" : "Lumber (LS)",
    "sector" : "SOFTS",
    "exchange" : "RANDOM LENGTH LUMBER - CHICAGO MERCANTILE EXCHANGE",
    "currentLongMarketSituation" : 64.9500000000000028,
    "currentShortMarketSituation" : 35.0499999999999972,
    "marketSituation" : "Bullish",
    "previousLongMarketSituation" : 64.6800000000000068,
    "previousShortMarketSituation" : 35.3200000000000003,
    "previousMarketSituation" : "Bullish",
    "netPostion" : 319,
    "previousNetPosition" : 321,
    "changeInNetPosition" : -0.619999999999999996,
    "marketSentiment" : "Increasing Bearish",
    "reversalTrend" : false
  }, ...
]
```
----
## GET /v4/social-sentiment <a name="0x6d3844f911ef24504d3fd4096923dbe90043c3c8cc8ecc020dd1ba1731422531"></a>

With this endpoint, you can keep track of what people are saying about individual stocks on social media. Reddit, Yahoo, StockTwits, and Twitter are among the sites monitored. Absolute index field indicates how much people are talking about the stock, relative index also indicates it  but relative to previous day. Sentiment field indicates overall percentage of positive activity, while general perception indicates whether people are more positive or negative than usual. This endpoint is updated with new data every hour, but it also contains previous data.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/social-sentiment

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x6d3844f911ef24504d3fd4096923dbe90043c3c8cc8ecc020dd1ba1731422531

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Symbol : Company Symbol, ex. AAPL
Limit : Number
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2021-09-09 19:35:05",
    "symbol" : "AAPL",
    "absoluteIndex" : 0.826211001642036202,
    "relativeIndex" : 1.40558558491621555,
    "generalPerception" : 0.976730914047170162,
    "sentiment" : 0.918290043290043156,
    "redditPostMentions" : 0,
    "redditPostSentiment" : null,
    "redditCommentMentions" : 2,
    "redditCommentSentiment" : 1,
    "tweetMentions" : 132,
    "tweetSentiment" : 0.886363636363636354,
    "stocktwitsPostMentions" : 75,
    "stocktwitsPostSentiment" : 0.809523809523809534,
    "yahooFinanceCommentMentions" : 17,
    "yahooFinanceCommentSentiment" : 1
  }, {
    "date" : "2021-09-09 18:35:08",
    "symbol" : "AAPL",
    "absoluteIndex" : 1.00888067870826492,
    "relativeIndex" : 1.36144467850889694,
    "generalPerception" : 0.976181779294421625,
    "sentiment" : 0.738720398344397178,
    "redditPostMentions" : 1,
    "redditPostSentiment" : 0,
    "redditCommentMentions" : 5,
    "redditCommentSentiment" : 0.599999999999999978,
    "tweetMentions" : 139,
    "tweetSentiment" : 0.776978417266187105,
    "stocktwitsPostMentions" : 95,
    "stocktwitsPostSentiment" : 0.773584905660377409,
    "yahooFinanceCommentMentions" : 24,
    "yahooFinanceCommentSentiment" : 0.91666666666666663
  }, ...
]
```
----
## GET /v3/grade/{symbol} <a name="0xc722594cd6883e15aa8929123f66ce0f4102c5869d23db8479c08b171095ce6e"></a>

This endpoint keeps track of the grades given to companies by hedge funds, investment firms and analysts. It includes both the previous and new grade. Because companies frequently maintain their grade, both of those fields can be the same at times.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/stock-grade

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0xc722594cd6883e15aa8929123f66ce0f4102c5869d23db8479c08b171095ce6e

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
Limit : Number 
Symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "symbol" : "AAPL",
    "date" : "2020-09-22",
    "gradingCompany" : "Raymond James",
    "previousGrade" : "Outperform",
    "newGrade" : "Outperform"
  }, {
    "symbol" : "AAPL",
    "date" : "2020-09-21",
    "gradingCompany" : "Citigroup",
    "previousGrade" : "Buy",
    "newGrade" : "Buy"
  }, {
    "symbol" : "AAPL",
    "date" : "2020-09-17",
    "gradingCompany" : "Jefferies",
    "previousGrade" : "Buy",
    "newGrade" : "Buy"
  }, ...
]
```
----
## GET /v3/earnings-surprises/{symbol} <a name="0x5def20718185062e609800c5edc04770a490b4e41035ec69112b4b368420ef8a"></a>

For stocks, this endpoint returns historical EPS earnings. It includes fields such as estimated and actual EPS. You can look at our earnings calendar, which includes fields such as revenue and expected revenue.

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/earnings-surprises

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x5def20718185062e609800c5edc04770a490b4e41035ec69112b4b368420ef8a

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
    "date" : "2020-06-30",
    "symbol" : "AAPL",
    "actualEarningResult" : 0.645,
    "estimatedEarning" : 0.5211078
  }, {
    "date" : "2020-03-31",
    "symbol" : "AAPL",
    "actualEarningResult" : 0.6375,
    "estimatedEarning" : 0.5765856
  }, {
    "date" : "2019-12-31",
    "symbol" : "AAPL",
    "actualEarningResult" : 1.2475,
    "estimatedEarning" : 1.159587
  }, {
    "date" : "2019-09-30",
    "symbol" : "AAPL",
    "actualEarningResult" : 0.7575,
    "estimatedEarning" : 0.7240368
  }, ...
]
```
----
## GET /v3/analyst-estimates/{symbol} <a name="0x4e12bccc65fefc1c8e7c1dd36cb5b71264e89be188c28a5f1cf52c0617566e9d"></a>

Get ratings and recommendations from FMP analysts, we use CAGR formula to predict and analyse stocks.
You will access all the key financial figures estimated. We use compound annual growth rate to estimate revenue as we found it gives the most accurate result. 

**Web2 Docs:** https://financialmodelingprep.com/developer/docs/analyst-estimates

You'll need the **Endpoint ID** to call this endpoint.

**Endpoint ID:** 0x4e12bccc65fefc1c8e7c1dd36cb5b71264e89be188c28a5f1cf52c0617566e9d

[Request Parameters](https://docs.api3.org/pre-alpha/protocols/request-response/request.html#request-parameters)

```solidity
limit : Number
period : annual | quarterly
symbol : Company Symbol, ex. AAPL
```

[Response](https://docs.api3.org/pre-alpha/airnode/specifications/reserved-parameters.html#path)

```json
[ {
  "symbol" : "AAPL",
  "date" : "2023-12-31",
  "estimatedRevenueLow" : 306907763421,
  "estimatedRevenueHigh" : 460361645134,
  "estimatedRevenueAvg" : 383634704278,
  "estimatedEbitdaLow" : 86145170339,
  "estimatedEbitdaHigh" : 129217755510,
  "estimatedEbitdaAvg" : 107681462925,
  "estimatedEbitLow" : 77432425549,
  "estimatedEbitHigh" : 116148638325,
  "estimatedEbitAvg" : 96790531937,
  "estimatedNetIncomeLow" : 100718671926,
  "estimatedNetIncomeHigh" : 67145781283,
  "estimatedNetIncomeAvg" : 83932226605,
  "estimatedSgaExpenseLow" : 16860504331,
  "estimatedSgaExpenseHigh" : 25290756496,
  "estimatedSgaExpenseAvg" : 21075630414,
  "estimatedEpsAvg" : 4.04,
  "estimatedEpsHigh" : 4.85,
  "estimatedEpsLow" : 3.23,
  "numberAnalystEstimatedRevenue" : 12,
  "numberAnalystsEstimatedEps" : 12
}, {
  "symbol" : "AAPL",
  "date" : "2022-12-31",
  "estimatedRevenueLow" : 279007057656,
  "estimatedRevenueHigh" : 418510586486,
  "estimatedRevenueAvg" : 348758822071,
  "estimatedEbitdaLow" : 78313791218,
  "estimatedEbitdaHigh" : 117470686828,
  "estimatedEbitdaAvg" : 97892239023,
  "estimatedEbitLow" : 70393114137,
  "estimatedEbitHigh" : 105589671206,
  "estimatedEbitAvg" : 87991392672,
  "estimatedNetIncomeLow" : 91562429025,
  "estimatedNetIncomeHigh" : 61041619349,
  "estimatedNetIncomeAvg" : 76302024187,
  "estimatedSgaExpenseLow" : 15327731211,
  "estimatedSgaExpenseHigh" : 22991596816,
  "estimatedSgaExpenseAvg" : 19159664014,
  "estimatedEpsAvg" : 3.665,
  "estimatedEpsHigh" : 4.3999999999999995,
  "estimatedEpsLow" : 2.93,
  "numberAnalystEstimatedRevenue" : 8,
  "numberAnalystsEstimatedEps" : 8
}, ...
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