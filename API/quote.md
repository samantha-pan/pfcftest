---  
nav_order: 4
parent: API Reference  
title: "quote"
--- 
內期行情
註冊接收即時和查詢

<a id="dquote.DQuote"></a>

## DQuote Objects

```python
class DQuote()
```

<a id="dquote.DQuote.on_error"></a>

#### on\_error

錯誤事件

<a id="dquote.DQuote.on_connected"></a>

#### on\_connected

連線成功事件

<a id="dquote.DQuote.on_disonnected"></a>

#### on\_disonnected

斷線事件

<a id="dquote.DQuote.on_tick_data_trade"></a>

#### on\_tick\_data\_trade

成交價事件..傳入物件:DTickDataTrade

<a id="dquote.DQuote.on_tick_data_high_low"></a>

#### on\_tick\_data\_high\_low

最高最低價事件..傳入物件:DTickDataHighLow

<a id="dquote.DQuote.on_index_data"></a>

#### on\_index\_data

現貨價事件..傳入物件:DIndexData

<a id="dquote.DQuote.on_tick_data_bid_offer"></a>

#### on\_tick\_data\_bid\_offer

五檔事件..傳入物件:DTickDataBidOffer

<a id="dquote.DQuote.on_tick_data_before_trade"></a>

#### on\_tick\_data\_before\_trade

試搓成交價事件..傳入物件:DTickDataBeforeTrade

<a id="dquote.DQuote.on_tick_data_before_bid_offer"></a>

#### on\_tick\_data\_before\_bid\_offer

試搓五檔事件..傳入物件:DTickDataBeforeBidOffer

<a id="dquote.DQuote.on_tick_data_open"></a>

#### on\_tick\_data\_open

開盤價事件..傳入物件:DTickDataOpen

<a id="dquote.DQuote.get_current_server"></a>

#### get\_current\_server

```python
def get_current_server()
```

目前連結主機IP 和 PORT
##### Returns 

| Name | Type | Description |
| ------ | ------ | ------------- |
| host | str | 主機IP |    
| port | str | 主機Port |

<a id="dquote.DQuote.get_server_list"></a>

#### get\_server\_list

```python
def get_server_list()
```

透過可連結主機
##### Returns dict[Server]

| Name | Type | Description |
| ------ | ------ | ------------- |
| key | str | servername |    
| value | Server | Server ip:str / port:int |

<a id="dquote.DQuote.set_sever_by_name"></a>

#### set\_sever\_by\_name

```python
def set_sever_by_name(servername) -> Tuple[bool, str]
```

透過主機名稱連結主機
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| servername | str | 主機名稱 |

<a id="dquote.DQuote.get_subscribe_trade_bid_offer"></a>

#### get\_subscribe\_trade\_bid\_offer

```python
def get_subscribe_trade_bid_offer()
```

查詢已註冊成交.賣賣價量 商品

<a id="dquote.DQuote.get_subscribe_highlow"></a>

#### get\_subscribe\_highlow

```python
def get_subscribe_highlow()
```

查詢已註冊最高最低價

<a id="dquote.DQuote.get_subscribe_index_data"></a>

#### get\_subscribe\_index\_data

```python
def get_subscribe_index_data()
```

查詢已註冊現貨 商品

<a id="dquote.DQuote.get_subscribe_open"></a>

#### get\_subscribe\_open

```python
def get_subscribe_open()
```

查詢已註冊開盤價 商品

<a id="dquote.DQuote.query_tick_data_trade"></a>

#### query\_tick\_data\_trade

```python
def query_tick_data_trade(productid) -> DTickDataTradeResponse
```

查詢最後成交價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |    

##### Returns  
TickDataTradeResponse

<a id="dquote.DQuote.query_tick_data_high_low"></a>

#### query\_tick\_data\_high\_low

```python
def query_tick_data_high_low(productid) -> DTickDataHighLowResponse
```

查詢最高(低)價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |    

##### Returns 

TickDataHighLowResponse

<a id="dquote.DQuote.query_tick_data_before_trade"></a>

#### query\_tick\_data\_before\_trade

```python
def query_tick_data_before_trade(productid) -> DTickDataBeforeTradeResponse
```

查詢最後盤前成交價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |    

##### Returns 
TickDataBeforeTradeResponse

<a id="dquote.DQuote.query_tick_data_open"></a>

#### query\_tick\_data\_open

```python
def query_tick_data_open(productid) -> DTickDataOpenResponse
```

查詢開盤價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

TickDataOpenResponse

<a id="dquote.DQuote.query_index_data"></a>

#### query\_index\_data

```python
def query_index_data(productid) -> DIndexDataResponse
```

查詢現貨成交價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 
IndexDataResponse

<a id="dquote.DQuote.query_tick_data_bid_offer"></a>

#### query\_tick\_data\_bid\_offer

```python
def query_tick_data_bid_offer(productid) -> DTickDataBidOfferResponse
```

查詢最後五檔
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

TickDataBidOfferResponse

<a id="dquote.DQuote.query_tick_data_before_bid_offer"></a>

#### query\_tick\_data\_before\_bid\_offer

```python
def query_tick_data_before_bid_offer(
        productid) -> DTickDataBeforeBidOfferResponse
```

查詢最後盤前五檔
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

TickDataBeforeBidOfferResponse

<a id="dquote.DQuote.subscribe_trade_bid_offer"></a>

#### subscribe\_trade\_bid\_offer

```python
def subscribe_trade_bid_offer(productid) -> Tuple[bool, str]
```

註冊成交.賣賣價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.unsubscribe_trade_bid_offer"></a>

#### unsubscribe\_trade\_bid\_offer

```python
def unsubscribe_trade_bid_offer(productid) -> Tuple[bool, str]
```

反註冊成交.賣賣價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.subscribe_high_low"></a>

#### subscribe\_high\_low

```python
def subscribe_high_low(productid) -> Tuple[bool, str]
```

註冊最高最低價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.unsubscribe_high_low"></a>

#### unsubscribe\_high\_low

```python
def unsubscribe_high_low(productid) -> Tuple[bool, str]
```

反註冊最高最低價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 | 

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.subscribe_open"></a>

#### subscribe\_open

```python
def subscribe_open(productid) -> Tuple[bool, str]
```

註冊開盤價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.unsubscribe_open"></a>

#### unsubscribe\_open

```python
def unsubscribe_open(productid) -> Tuple[bool, str]
```

反註冊開盤價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| productid | str | 商品代碼 |  

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.subscribe_index_data"></a>

#### subscribe\_index\_data

```python
def subscribe_index_data(kind, index) -> Tuple[bool, str]
```

註冊現貨價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| index | str | 商品代碼 |    

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.unsubscribe_index_data"></a>

#### unsubscribe\_index\_data

```python
def unsubscribe_index_data(kind, index) -> Tuple[bool, str]
```

反註冊現貨價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| index | str | 商品代碼 |    

##### Returns 

| Type | Description |
| ------ | ------------- |
| bool | 是否成功 |    
| str | 錯誤訊息 |

<a id="dquote.DQuote.close"></a>

#### close

```python
def close()
```

關閉物件

<a id="dquote.Format"></a>

## Format Objects

```python
class Format()
```

<a id="dquote.Format.I020_HEAD"></a>

#### I020\_HEAD

成交價揭示

<a id="dquote.Format.I021_HEAD"></a>

#### I021\_HEAD

最高最低價揭示

<a id="dquote.Format.I022_HEAD"></a>

#### I022\_HEAD

盤前揭示成交價揭示

<a id="dquote.Format.I023_HEAD"></a>

#### I023\_HEAD

定時開盤價量揭示

<a id="dquote.Format.I060_HEAD"></a>

#### I060\_HEAD

現貨價

<a id="dquote.Format.I080_HEAD"></a>

#### I080\_HEAD

委託簿揭示

<a id="dquote.Format.I082_HEAD"></a>

#### I082\_HEAD

盤前委託簿揭示

<a id="dquote.Format.I020"></a>

#### I020

成交價揭示

<a id="dquote.Format.I021"></a>

#### I021

最高最低價揭示

<a id="dquote.Format.I022"></a>

#### I022

盤前揭示成交價揭示

<a id="dquote.Format.I023"></a>

#### I023

定時開盤價量揭示

<a id="dquote.Format.I060"></a>

#### I060

現貨價

<a id="dquote.Format.I080"></a>

#### I080

委託簿揭示

<a id="dquote.Format.I082"></a>

#### I082

盤前委託簿揭示

<a id="dquote.Format.X010"></a>

#### X010

商品基本資料訊息

<a id="dquote.Format.X020"></a>

#### X020

成交價量揭示訊息

<a id="dquote.Format.X021"></a>

#### X021

盤中最高低價揭示訊息

<a id="dquote.Format.X060"></a>

#### X060

現貨標的資訊

<a id="dquote.Format.X080"></a>

#### X080

委託簿揭示訊息

---  
nav_order: 4
parent: API Reference  
title: "quote"
--- 
內期行情物件

<a id="ddata.DTickDataTrade"></a>

## DTickDataTrade Objects

```python
class DTickDataTrade()
```

成交價揭示

<a id="ddata.DTickDataTrade.commodityid"></a>

#### commodityid

商品代號 str

<a id="ddata.DTickDataTrade.infotime"></a>

#### infotime

期交所送出時間 str

<a id="ddata.DTickDataTrade.matchprice"></a>

#### matchprice

成交價格 float

<a id="ddata.DTickDataTrade.matchquantity"></a>

#### matchquantity

成交量 int

<a id="ddata.DTickDataTrade.matchtotalqty"></a>

#### matchtotalqty

成交總量 int

<a id="ddata.DTickDataTrade.matchbuycnt"></a>

#### matchbuycnt

成交買量 int

<a id="ddata.DTickDataTrade.matchsellcnt"></a>

#### matchsellcnt

成交賣量 int

<a id="ddata.DTickDataTrade.matchtime"></a>

#### matchtime

成交時間 str

<a id="ddata.DTickDataHighLow"></a>

## DTickDataHighLow Objects

```python
class DTickDataHighLow()
```

最高最低價揭示

<a id="ddata.DTickDataHighLow.commodityid"></a>

#### commodityid

商品代碼 str

<a id="ddata.DTickDataHighLow.showtime"></a>

#### showtime

時間 str

<a id="ddata.DTickDataHighLow.dayhighprice"></a>

#### dayhighprice

最高價 float

<a id="ddata.DTickDataHighLow.daylowprice"></a>

#### daylowprice

最低價 float

<a id="ddata.DTickDataBeforeTrade"></a>

## DTickDataBeforeTrade Objects

```python
class DTickDataBeforeTrade()
```

盤前揭示成交價揭示

<a id="ddata.DTickDataBeforeTrade.commodityid"></a>

#### commodityid

商品代號 str

<a id="ddata.DTickDataBeforeTrade.infotime"></a>

#### infotime

期交所送出時間 str

<a id="ddata.DTickDataBeforeTrade.matchprice"></a>

#### matchprice

成交價格 int

<a id="ddata.DTickDataBeforeTrade.matchquantity"></a>

#### matchquantity

成交量 int

<a id="ddata.DTickDataBeforeTrade.matchtotalqty"></a>

#### matchtotalqty

成交總量 int

<a id="ddata.DTickDataBeforeTrade.matchbuycnt"></a>

#### matchbuycnt

成交買量 int

<a id="ddata.DTickDataBeforeTrade.matchsellcnt"></a>

#### matchsellcnt

成交賣量 int

<a id="ddata.DTickDataBeforeTrade.matchtime"></a>

#### matchtime

成交時間 str

<a id="ddata.DIndexData"></a>

## DIndexData Objects

```python
class DIndexData()
```

現貨價

<a id="ddata.DIndexData.index_kind"></a>

#### index\_kind

現貨代碼 str

<a id="ddata.DIndexData.index_time"></a>

#### index\_time

現貨統計時間 str

<a id="ddata.DIndexData.index_value"></a>

#### index\_value

現貨價 float

<a id="ddata.DTickDataBidOffer"></a>

## DTickDataBidOffer Objects

```python
class DTickDataBidOffer()
```

委託簿揭示

<a id="ddata.DTickDataBidOffer.commodityid"></a>

#### commodityid

商品代碼 str

<a id="ddata.DTickDataBidOffer.bp1"></a>

#### bp1

第一檔委買價格 float

<a id="ddata.DTickDataBidOffer.bp2"></a>

#### bp2

第二檔委買價格 float

<a id="ddata.DTickDataBidOffer.bp3"></a>

#### bp3

第三檔委買價格 float

<a id="ddata.DTickDataBidOffer.bp4"></a>

#### bp4

第四檔委買價格 float

<a id="ddata.DTickDataBidOffer.bp5"></a>

#### bp5

第五檔委買價格 float

<a id="ddata.DTickDataBidOffer.bq1"></a>

#### bq1

第一檔委買數量 int

<a id="ddata.DTickDataBidOffer.bq2"></a>

#### bq2

第二檔委買數量 int

<a id="ddata.DTickDataBidOffer.bq3"></a>

#### bq3

第三檔委買數量 int

<a id="ddata.DTickDataBidOffer.bq4"></a>

#### bq4

第四檔委買數量 int

<a id="ddata.DTickDataBidOffer.bq5"></a>

#### bq5

第五檔委買數量 int

<a id="ddata.DTickDataBidOffer.sp1"></a>

#### sp1

第一檔委賣價格 float

<a id="ddata.DTickDataBidOffer.sp2"></a>

#### sp2

第二檔委賣價格 float

<a id="ddata.DTickDataBidOffer.sp3"></a>

#### sp3

第三檔委賣價格 float

<a id="ddata.DTickDataBidOffer.sp4"></a>

#### sp4

第四檔委賣價格 float

<a id="ddata.DTickDataBidOffer.sp5"></a>

#### sp5

第五檔委賣價格 float

<a id="ddata.DTickDataBidOffer.sq1"></a>

#### sq1

第一檔委買數量 int

<a id="ddata.DTickDataBidOffer.sq2"></a>

#### sq2

第二檔委賣數量 int

<a id="ddata.DTickDataBidOffer.sq3"></a>

#### sq3

第三檔委賣數量 int

<a id="ddata.DTickDataBidOffer.sq4"></a>

#### sq4

第四檔委賣數量 int

<a id="ddata.DTickDataBidOffer.sq5"></a>

#### sq5

第五檔委賣數量 int

<a id="ddata.DTickDataBeforeBidOffer"></a>

## DTickDataBeforeBidOffer Objects

```python
class DTickDataBeforeBidOffer()
```

盤前委託簿揭示

<a id="ddata.DTickDataBeforeBidOffer.commodityid"></a>

#### commodityid

商品代碼 str

<a id="ddata.DTickDataBeforeBidOffer.bp1"></a>

#### bp1

第一檔委買價格 float

<a id="ddata.DTickDataBeforeBidOffer.bp2"></a>

#### bp2

第二檔委買價格 float

<a id="ddata.DTickDataBeforeBidOffer.bp3"></a>

#### bp3

第三檔委買價格 float

<a id="ddata.DTickDataBeforeBidOffer.bp4"></a>

#### bp4

第四檔委買價格 float

<a id="ddata.DTickDataBeforeBidOffer.bp5"></a>

#### bp5

第五檔委買價格 float

<a id="ddata.DTickDataBeforeBidOffer.bq1"></a>

#### bq1

第一檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.bq2"></a>

#### bq2

第二檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.bq3"></a>

#### bq3

第三檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.bq4"></a>

#### bq4

第四檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.bq5"></a>

#### bq5

第五檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.sp1"></a>

#### sp1

第一檔委賣價格 float

<a id="ddata.DTickDataBeforeBidOffer.sp2"></a>

#### sp2

第二檔委賣價格 float

<a id="ddata.DTickDataBeforeBidOffer.sp3"></a>

#### sp3

第三檔委賣價格 float

<a id="ddata.DTickDataBeforeBidOffer.sp4"></a>

#### sp4

第四檔委賣價格 float

<a id="ddata.DTickDataBeforeBidOffer.sp5"></a>

#### sp5

第五檔委賣價格 float

<a id="ddata.DTickDataBeforeBidOffer.sq1"></a>

#### sq1

第一檔委買數量 int

<a id="ddata.DTickDataBeforeBidOffer.sq2"></a>

#### sq2

第二檔委賣數量 int

<a id="ddata.DTickDataBeforeBidOffer.sq3"></a>

#### sq3

第三檔委賣數量 int

<a id="ddata.DTickDataBeforeBidOffer.sq4"></a>

#### sq4

第四檔委賣數量 int

<a id="ddata.DTickDataBeforeBidOffer.sq5"></a>

#### sq5

第五檔委賣數量 int

<a id="ddata.DTickDataOpen"></a>

## DTickDataOpen Objects

```python
class DTickDataOpen()
```

開盤價揭示

<a id="ddata.DTickDataOpen.commodityid"></a>

#### commodityid

商品代碼

<a id="ddata.DTickDataOpen.opentime"></a>

#### opentime

開盤時間

<a id="ddata.DTickDataOpen.openprice"></a>

#### openprice

開盤價

<a id="ddata.DTickDataOpen.openquantity"></a>

#### openquantity

開盤量

<a id="ddata.DTickDataTradeResponse"></a>

## DTickDataTradeResponse Objects

```python
@dataclass
class DTickDataTradeResponse()
```

成交價量查詢回覆物件

<a id="ddata.DTickDataTradeResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataTradeResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataTradeResponse.data"></a>

#### data

回覆物件 TickDataTrade

<a id="ddata.DTickDataBeforeTradeResponse"></a>

## DTickDataBeforeTradeResponse Objects

```python
@dataclass
class DTickDataBeforeTradeResponse()
```

試搓成交價量查詢回覆物件

<a id="ddata.DTickDataBeforeTradeResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataBeforeTradeResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataBeforeTradeResponse.data"></a>

#### data

回覆物件 TickDataBeforeTrade

<a id="ddata.DTickDataHighLowResponse"></a>

## DTickDataHighLowResponse Objects

```python
@dataclass
class DTickDataHighLowResponse()
```

最高最低價查詢回覆物件

<a id="ddata.DTickDataHighLowResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataHighLowResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataHighLowResponse.data"></a>

#### data

回覆物件 TickDataHighLow

<a id="ddata.DTickDataOpenResponse"></a>

## DTickDataOpenResponse Objects

```python
@dataclass
class DTickDataOpenResponse()
```

開盤價查詢回覆物件

<a id="ddata.DTickDataOpenResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataOpenResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataOpenResponse.data"></a>

#### data

回覆物件 TickDataOpen

<a id="ddata.DIndexDataResponse"></a>

## DIndexDataResponse Objects

```python
@dataclass
class DIndexDataResponse()
```

現貨價格查詢回覆物件

<a id="ddata.DIndexDataResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DIndexDataResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DIndexDataResponse.data"></a>

#### data

回覆物件 IndexData

<a id="ddata.DTickDataBidOfferResponse"></a>

## DTickDataBidOfferResponse Objects

```python
@dataclass
class DTickDataBidOfferResponse()
```

最佳買賣價查詢回覆物件

<a id="ddata.DTickDataBidOfferResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataBidOfferResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataBidOfferResponse.data"></a>

#### data

回覆物件 TickDataBidOffer

<a id="ddata.DTickDataBeforeBidOfferResponse"></a>

## DTickDataBeforeBidOfferResponse Objects

```python
@dataclass
class DTickDataBeforeBidOfferResponse()
```

試搓最佳買賣價查詢回覆物件

<a id="ddata.DTickDataBeforeBidOfferResponse.ok"></a>

#### ok

是否成功 bool

<a id="ddata.DTickDataBeforeBidOfferResponse.error"></a>

#### error

錯誤訊息 str

<a id="ddata.DTickDataBeforeBidOfferResponse.data"></a>

#### data

回覆物件 TickDataBeforeBidOffer

