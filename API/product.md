---  
nav_order: 1
parent: API Reference  
title: "product"
--- 
<a id="domesticcontract.DomesticContract"></a>

## DomesticContract Objects

```python
class DomesticContract()
```

內期商品合約檔

<a id="domesticcontract.DomesticContract.prod_id"></a>

#### prod\_id

商品代號

<a id="domesticcontract.DomesticContract.month"></a>

#### month

年月

<a id="domesticcontract.DomesticContract.cp"></a>

#### cp

CP

<a id="domesticcontract.DomesticContract.stikeprice"></a>

#### stikeprice

履約價

<a id="domesticcontract.DomesticContract.maxprice"></a>

#### maxprice

漲停價

<a id="domesticcontract.DomesticContract.minprice"></a>

#### minprice

跌停價

<a id="domesticcontract.DomesticContract.premium"></a>

#### premium

參考價

---  
nav_order: 1
parent: API Reference  
title: "product"
--- 
<a id="domesticproduct.DomesticProduct"></a>

## DomesticProduct Objects

```python
class DomesticProduct()
```

內期商品

<a id="domesticproduct.DomesticProduct.kind_id"></a>

#### kind\_id

商品類別

<a id="domesticproduct.DomesticProduct.name"></a>

#### name

商品名稱

<a id="domesticproduct.DomesticProduct.stock_id"></a>

#### stock\_id

股票代碼

<a id="domesticproduct.DomesticProduct.subtype"></a>

#### subtype

類別

<a id="domesticproduct.DomesticProduct.contract_size"></a>

#### contract\_size

合約基數

<a id="domesticproduct.DomesticProduct.strike_price_decimal_locator"></a>

#### strike\_price\_decimal\_locator

選擇權履約價小數位

---  
nav_order: 1
parent: API Reference  
title: "product"
--- 
<a id="foreigncontract.ForeignContract"></a>

## ForeignContract Objects

```python
class ForeignContract()
```

外期商品合約檔

<a id="foreigncontract.ForeignContract.exchange"></a>

#### exchange

交易所

<a id="foreigncontract.ForeignContract.symbol"></a>

#### symbol

商品代碼

<a id="foreigncontract.ForeignContract.type"></a>

#### type

類型(期貨:F 選擇權:O)

<a id="foreigncontract.ForeignContract.monthyear"></a>

#### monthyear

年月

<a id="foreigncontract.ForeignContract.strikeprice"></a>

#### strikeprice

履約價

<a id="foreigncontract.ForeignContract.cp"></a>

#### cp

call put

<a id="foreigncontract.ForeignContract.lasttradedate"></a>

#### lasttradedate

最後交易日

---  
nav_order: 1
parent: API Reference  
title: "product"
--- 
<a id="foreignproduct.ForeignProduct"></a>

## ForeignProduct Objects

```python
class ForeignProduct()
```

外期商品

<a id="foreignproduct.ForeignProduct.exchange"></a>

#### exchange

交易所

<a id="foreignproduct.ForeignProduct.symbol"></a>

#### symbol

商品代碼

<a id="foreignproduct.ForeignProduct.type"></a>

#### type

類型(期貨:F 選擇權:O)

<a id="foreignproduct.ForeignProduct.name"></a>

#### name

中文名稱

<a id="foreignproduct.ForeignProduct.shortname"></a>

#### shortname

中文簡稱

<a id="foreignproduct.ForeignProduct.country"></a>

#### country

區域

<a id="foreignproduct.ForeignProduct.currency"></a>

#### currency

幣別

---  
nav_order: 1
parent: API Reference  
title: "product"
--- 
<a id="exchange.EXCHANGE"></a>

## EXCHANGE Objects

```python
class EXCHANGE()
```

外期交易所物件

<a id="exchange.EXCHANGE.exchange"></a>

#### exchange

交易所

<a id="exchange.EXCHANGE.name"></a>

#### name

中文名稱

<a id="exchange.EXCHANGE.country"></a>

#### country

區域

<a id="exchange.EXCHANGE.currency"></a>

#### currency

幣別

