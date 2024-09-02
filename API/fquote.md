---  
nav_order: 5
parent: API Reference  
title: "fquote"
--- 
<link rel="stylesheet" href="{ '/assets/css/just-the-docs-custom.css' | relative_url }">
外期行情
註冊接收即時和查詢

<a id="fquote.FQuote"></a>

## FQuote Objects

```python
class FQuote()
```

<a id="fquote.FQuote.on_error"></a>

#### on\_error

錯誤事件

<a id="fquote.FQuote.on_connected"></a>

#### on\_connected

連線成功事件

<a id="fquote.FQuote.on_disonnected"></a>

#### on\_disonnected

斷線事件

<a id="fquote.FQuote.on_tick_data_trade"></a>

#### on\_tick\_data\_trade

成交價事件..傳入物件:FTickDataTrade

<a id="fquote.FQuote.on_tick_data_bid"></a>

#### on\_tick\_data\_bid

最佳買價量事件..傳入物件:FTickDataBid

<a id="fquote.FQuote.on_tick_data_offer"></a>

#### on\_tick\_data\_offer

最佳賣價量事件..傳入物件:FTickDataOffer

<a id="fquote.FQuote.on_tick_data_implied"></a>

#### on\_tick\_data\_implied

隱含價事件..傳入物件:FTickDataImplied

<a id="fquote.FQuote.on_tick_data_high_low"></a>

#### on\_tick\_data\_high\_low

最高最低價事件..傳入物件:FTickDataHighLow

<a id="fquote.FQuote.on_tick_data_open_close"></a>

#### on\_tick\_data\_open\_close

開盤價事件..傳入物件:FTickDataOpenclose

<a id="fquote.FQuote.on_tick_data_settle"></a>

#### on\_tick\_data\_settle

結算價事件..傳入物件:FTickDataOpen

<a id="fquote.FQuote.get_current_server"></a>

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

<a id="fquote.FQuote.get_server_list"></a>

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

<a id="fquote.FQuote.set_sever_by_name"></a>

#### set\_sever\_by\_name

```python
def set_sever_by_name(servername)
```

透過主機名稱連結主機
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| servername | str | 主機名稱 |

<a id="fquote.FQuote.get_subscribe"></a>

#### get\_subscribe

```python
def get_subscribe()
```

查詢已註冊商品

<a id="fquote.FQuote.query_tick_data_trade"></a>

#### query\_tick\_data\_trade

```python
def query_tick_data_trade(exchange, symbol, ym, strike,
                          cp) -> FTickDataTradeResponse
```

查詢最後成交價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |    

##### Returns 
FTickDataTradeResponse

<a id="fquote.FQuote.query_tick_data_bid"></a>

#### query\_tick\_data\_bid

```python
def query_tick_data_bid(exchange, symbol, ym, strike,
                        cp) -> FTickDataBidResponse
```

查詢最佳買進報價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |    

##### Returns 

FTickDataBidResponse

<a id="fquote.FQuote.query_tick_data_offer"></a>

#### query\_tick\_data\_offer

```python
def query_tick_data_offer(exchange, symbol, ym, strike,
                          cp) -> FTickDataOfferResponse
```

最佳賣出報價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |    

##### Returns 

FTickDataOfferResponse

<a id="fquote.FQuote.query_tick_data_implied"></a>

#### query\_tick\_data\_implied

```python
def query_tick_data_implied(exchange, symbol, ym, strike,
                            cp) -> FTickDataImpliedResponse
```

隱含買賣價量
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |  

##### Returns 

FTickDataImpliedResponse

<a id="fquote.FQuote.query_tick_data_open_close"></a>

#### query\_tick\_data\_open\_close

```python
def query_tick_data_open_close(exchange, symbol, ym, strike,
                               cp) -> FTickDataOpencloseResponse
```

查詢開收盤價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |  

##### Returns 

FTickDataOpencloseResponse

<a id="fquote.FQuote.query_tick_data_high_low"></a>

#### query\_tick\_data\_high\_low

```python
def query_tick_data_high_low(exchange, symbol, ym, strike,
                             cp) -> FTickDataHighLowResponse
```

查詢最高最低價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |    

##### Returns 

FTickDataHighLowResponse

<a id="fquote.FQuote.query_tick_data_settle"></a>

#### query\_tick\_data\_settle

```python
def query_tick_data_settle(exchange, symbol, ym, strike,
                           cp) -> FTickDataSettleResponse
```

查詢結算價
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |   

##### Returns 

FTickDataSettleResponse

<a id="fquote.FQuote.subscribe"></a>

#### subscribe

```python
def subscribe(exchange: str, symbol: str, ym: str, cp: str,
              strike: str) -> Tuple[bool, str]
```

註冊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |    

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="fquote.FQuote.unsubscribe"></a>

#### unsubscribe

```python
def unsubscribe(exchange: str, symbol: str, ym: str, cp: str,
                strike: str) -> Tuple[bool, str]
```

反註冊
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |    
| symbol | str | 商品代號 |    
| ym | str | 年月 |    
| cp | str | CP |    
| strike | str | 履約價 |   

##### Returns 

| Type | Description |
|------|-------------|
|bool|是否成功|    
|str|錯誤訊息|

<a id="fquote.FQuote.close"></a>

#### close

```python
def close()
```

關閉物件

<a id="fquote.Format"></a>

## Format Objects

```python
class Format()
```

<a id="fquote.Format.I020_HEAD"></a>

#### I020\_HEAD

成交價揭示

<a id="fquote.Format.I021_HEAD"></a>

#### I021\_HEAD

最高最低價揭示

<a id="fquote.Format.I022_HEAD"></a>

#### I022\_HEAD

盤前揭示成交價揭示

<a id="fquote.Format.I060_HEAD"></a>

#### I060\_HEAD

現貨價

<a id="fquote.Format.I080_HEAD"></a>

#### I080\_HEAD

委託簿揭示

<a id="fquote.Format.I082_HEAD"></a>

#### I082\_HEAD

盤前委託簿揭示

<a id="fquote.Format.TICKDATATRADE"></a>

#### TICKDATATRADE

即時成交價量

<a id="fquote.Format.TICKDATABID"></a>

#### TICKDATABID

即時最佳買進報價

<a id="fquote.Format.TICKDATAOFFER"></a>

#### TICKDATAOFFER

即時最佳賣出報價

<a id="fquote.Format.TICKDATAIMPLIED"></a>

#### TICKDATAIMPLIED

即時隱含買賣價量

<a id="fquote.Format.TICKDATAHIGHLOW"></a>

#### TICKDATAHIGHLOW

即時最高最低價

<a id="fquote.Format.TICKDATAOPENCLOSE"></a>

#### TICKDATAOPENCLOSE

即時開收盤價

<a id="fquote.Format.TICKDATASETTLE"></a>

#### TICKDATASETTLE

即時結算價

---  
nav_order: 5
parent: API Reference  
title: "fquote"
--- 
<link rel="stylesheet" href="{ '/assets/css/just-the-docs-custom.css' | relative_url }">
外期行情物件

<a id="fdata.FContract"></a>

## FContract Objects

```python
@dataclass
class FContract()
```

<a id="fdata.FContract.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FContract.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FContract.ym"></a>

#### ym

年月 str

<a id="fdata.FContract.strike"></a>

#### strike

履約價 str

<a id="fdata.FContract.cp"></a>

#### cp

CP str

<a id="fdata.FContract.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FContract.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataTrade"></a>

## FTickDataTrade Objects

```python
class FTickDataTrade()
```

即時成交價量

<a id="fdata.FTickDataTrade.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataTrade.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataTrade.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataTrade.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataTrade.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataTrade.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataTrade.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataTrade.total"></a>

#### total

總量 int

<a id="fdata.FTickDataTrade.lastprice"></a>

#### lastprice

成交價 float

<a id="fdata.FTickDataTrade.lastvolume"></a>

#### lastvolume

成交量 int

<a id="fdata.FTickDataTrade.time"></a>

#### time

成交時間

<a id="fdata.FTickDataBid"></a>

## FTickDataBid Objects

```python
class FTickDataBid()
```

即時最佳買進報價

<a id="fdata.FTickDataBid.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataBid.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataBid.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataBid.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataBid.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataBid.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataBid.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataBid.BidDOM1Price"></a>

#### BidDOM1Price

最佳買價1 float

<a id="fdata.FTickDataBid.BidDOM1Volume"></a>

#### BidDOM1Volume

最佳買量1 int

<a id="fdata.FTickDataBid.BidDOM2Price"></a>

#### BidDOM2Price

最佳買價2 float

<a id="fdata.FTickDataBid.BidDOM2Volume"></a>

#### BidDOM2Volume

最佳買量2 int

<a id="fdata.FTickDataBid.BidDOM3Price"></a>

#### BidDOM3Price

最佳買價3 float

<a id="fdata.FTickDataBid.BidDOM3Volume"></a>

#### BidDOM3Volume

最佳買量3

<a id="fdata.FTickDataBid.BidDOM4Price"></a>

#### BidDOM4Price

最佳買價4 float

<a id="fdata.FTickDataBid.BidDOM4Volume"></a>

#### BidDOM4Volume

最佳買量4 int

<a id="fdata.FTickDataBid.BidDOM5Price"></a>

#### BidDOM5Price

最佳買價5 float

<a id="fdata.FTickDataBid.BidDOM5Volume"></a>

#### BidDOM5Volume

最佳買量5 int

<a id="fdata.FTickDataBid.BidDOM6Price"></a>

#### BidDOM6Price

最佳買價6 float

<a id="fdata.FTickDataBid.BidDOM6Volume"></a>

#### BidDOM6Volume

最佳買量6 int

<a id="fdata.FTickDataBid.BidDOM7Price"></a>

#### BidDOM7Price

最佳買價7 float

<a id="fdata.FTickDataBid.BidDOM7Volume"></a>

#### BidDOM7Volume

最佳買量7 int

<a id="fdata.FTickDataBid.BidDOM8Price"></a>

#### BidDOM8Price

最佳買價8 float

<a id="fdata.FTickDataBid.BidDOM8Volume"></a>

#### BidDOM8Volume

最佳買量8 int

<a id="fdata.FTickDataBid.BidDOM9Price"></a>

#### BidDOM9Price

最佳買價9 float

<a id="fdata.FTickDataBid.BidDOM9Volume"></a>

#### BidDOM9Volume

最佳買量9 int

<a id="fdata.FTickDataBid.BidDOM10Price"></a>

#### BidDOM10Price

最佳買價10 float

<a id="fdata.FTickDataBid.BidDOM10Volume"></a>

#### BidDOM10Volume

最佳買量10 int

<a id="fdata.FTickDataOffer"></a>

## FTickDataOffer Objects

```python
class FTickDataOffer()
```

即時最佳買進報價

<a id="fdata.FTickDataOffer.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataOffer.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataOffer.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataOffer.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataOffer.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataOffer.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataOffer.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataOffer.OfferDOM1Price"></a>

#### OfferDOM1Price

最佳賣價1 float

<a id="fdata.FTickDataOffer.OfferDOM1Volume"></a>

#### OfferDOM1Volume

最佳賣量1 int

<a id="fdata.FTickDataOffer.OfferDOM2Price"></a>

#### OfferDOM2Price

最佳賣價2 float

<a id="fdata.FTickDataOffer.OfferDOM2Volume"></a>

#### OfferDOM2Volume

最佳賣量2 int

<a id="fdata.FTickDataOffer.OfferDOM3Price"></a>

#### OfferDOM3Price

最佳賣價3 float

<a id="fdata.FTickDataOffer.OfferDOM3Volume"></a>

#### OfferDOM3Volume

最佳賣量3 int

<a id="fdata.FTickDataOffer.OfferDOM4Price"></a>

#### OfferDOM4Price

最佳賣價4 float

<a id="fdata.FTickDataOffer.OfferDOM4Volume"></a>

#### OfferDOM4Volume

最佳賣量4 int

<a id="fdata.FTickDataOffer.OfferDOM5Price"></a>

#### OfferDOM5Price

最佳賣價5 float

<a id="fdata.FTickDataOffer.OfferDOM5Volume"></a>

#### OfferDOM5Volume

最佳賣量5 int

<a id="fdata.FTickDataOffer.OfferDOM6Price"></a>

#### OfferDOM6Price

最佳賣價6 float

<a id="fdata.FTickDataOffer.OfferDOM6Volume"></a>

#### OfferDOM6Volume

最佳賣量6 int

<a id="fdata.FTickDataOffer.OfferDOM7Price"></a>

#### OfferDOM7Price

最佳賣價7 float

<a id="fdata.FTickDataOffer.OfferDOM7Volume"></a>

#### OfferDOM7Volume

最佳賣量7 int

<a id="fdata.FTickDataOffer.OfferDOM8Price"></a>

#### OfferDOM8Price

最佳賣價8 float

<a id="fdata.FTickDataOffer.OfferDOM8Volume"></a>

#### OfferDOM8Volume

最佳賣量8 int

<a id="fdata.FTickDataOffer.OfferDOM9Price"></a>

#### OfferDOM9Price

最佳賣價9 float

<a id="fdata.FTickDataOffer.OfferDOM9Volume"></a>

#### OfferDOM9Volume

最佳賣量9 int

<a id="fdata.FTickDataOffer.OfferDOM10Price"></a>

#### OfferDOM10Price

最佳賣價10 float

<a id="fdata.FTickDataOffer.OfferDOM10Volume"></a>

#### OfferDOM10Volume

最佳賣量10 int

<a id="fdata.FTickDataImplied"></a>

## FTickDataImplied Objects

```python
class FTickDataImplied()
```

即時隱含買賣價量

<a id="fdata.FTickDataImplied.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataImplied.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataImplied.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataImplied.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataImplied.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataImplied.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataImplied.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataImplied.ImpliedBidPrice"></a>

#### ImpliedBidPrice

隱含買價  float

<a id="fdata.FTickDataImplied.ImpliedBidVolume"></a>

#### ImpliedBidVolume

隱含買量 int

<a id="fdata.FTickDataImplied.ImpliedOfferPrice"></a>

#### ImpliedOfferPrice

隱含賣價  float

<a id="fdata.FTickDataImplied.ImpliedOfferVolume"></a>

#### ImpliedOfferVolume

隱含賣量 int

<a id="fdata.FTickDataHighLow"></a>

## FTickDataHighLow Objects

```python
class FTickDataHighLow()
```

即時最高最低價

<a id="fdata.FTickDataHighLow.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataHighLow.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataHighLow.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataHighLow.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataHighLow.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataHighLow.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataHighLow.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataHighLow.High"></a>

#### High

最高價 float

<a id="fdata.FTickDataHighLow.Low"></a>

#### Low

最低價 float

<a id="fdata.FTickDataOpenclose"></a>

## FTickDataOpenclose Objects

```python
class FTickDataOpenclose()
```

即時開收盤價

<a id="fdata.FTickDataOpenclose.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataOpenclose.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataOpenclose.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataOpenclose.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataOpenclose.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataOpenclose.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataOpenclose.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataOpenclose.Opening"></a>

#### Opening

開盤價 float

<a id="fdata.FTickDataOpenclose.Closing"></a>

#### Closing

收盤價 float

<a id="fdata.FTickDataSettle"></a>

## FTickDataSettle Objects

```python
class FTickDataSettle()
```

即時結算價

<a id="fdata.FTickDataSettle.exchage"></a>

#### exchage

交易所 str

<a id="fdata.FTickDataSettle.symbol"></a>

#### symbol

商品代號 str

<a id="fdata.FTickDataSettle.ym"></a>

#### ym

年月 str

<a id="fdata.FTickDataSettle.cp"></a>

#### cp

CP str

<a id="fdata.FTickDataSettle.strike"></a>

#### strike

履約價 str

<a id="fdata.FTickDataSettle.display_denominator"></a>

#### display\_denominator

分母 float

<a id="fdata.FTickDataSettle.display_multiply"></a>

#### display\_multiply

倍率 float

<a id="fdata.FTickDataSettle.CurrStl"></a>

#### CurrStl

目前結算價

<a id="fdata.FTickDataSettle.NewStl"></a>

#### NewStl

最新結算價

<a id="fdata.FTickDataTradeResponse"></a>

## FTickDataTradeResponse Objects

```python
@dataclass
class FTickDataTradeResponse()
```

成交價量查詢回覆物件

<a id="fdata.FTickDataTradeResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataTradeResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataTradeResponse.data"></a>

#### data

回覆物件 TickDataTrade

<a id="fdata.FTickDataBidResponse"></a>

## FTickDataBidResponse Objects

```python
@dataclass
class FTickDataBidResponse()
```

最佳買價量查詢回覆物件

<a id="fdata.FTickDataBidResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataBidResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataBidResponse.data"></a>

#### data

回覆物件 TickDataBid

<a id="fdata.FTickDataOfferResponse"></a>

## FTickDataOfferResponse Objects

```python
@dataclass
class FTickDataOfferResponse()
```

最佳賣價量查詢回覆物件

<a id="fdata.FTickDataOfferResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataOfferResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataOfferResponse.data"></a>

#### data

回覆物件 TickDataOffer

<a id="fdata.FTickDataImpliedResponse"></a>

## FTickDataImpliedResponse Objects

```python
@dataclass
class FTickDataImpliedResponse()
```

隱含價量查詢回覆物件

<a id="fdata.FTickDataImpliedResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataImpliedResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataImpliedResponse.data"></a>

#### data

回覆物件 TickDataImplied

<a id="fdata.FTickDataHighLowResponse"></a>

## FTickDataHighLowResponse Objects

```python
@dataclass
class FTickDataHighLowResponse()
```

最高最低價查詢回覆物件

<a id="fdata.FTickDataHighLowResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataHighLowResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataHighLowResponse.data"></a>

#### data

回覆物件 TickDataHighLow

<a id="fdata.FTickDataOpencloseResponse"></a>

## FTickDataOpencloseResponse Objects

```python
@dataclass
class FTickDataOpencloseResponse()
```

開收盤價查詢回覆物件

<a id="fdata.FTickDataOpencloseResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataOpencloseResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataOpencloseResponse.data"></a>

#### data

回覆物件 TickDataOpenclose

<a id="fdata.FTickDataSettleResponse"></a>

## FTickDataSettleResponse Objects

```python
@dataclass
class FTickDataSettleResponse()
```

結算價查詢回覆物件

<a id="fdata.FTickDataSettleResponse.ok"></a>

#### ok

是否成功 bool

<a id="fdata.FTickDataSettleResponse.error"></a>

#### error

錯誤訊息 str

<a id="fdata.FTickDataSettleResponse.data"></a>

#### data

回覆物件 TickDataSettle

