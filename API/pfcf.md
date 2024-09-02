---  
nav_order: 0
parent: API Reference  
title: "pfcf"
--- 
<link rel="stylesheet" href="/assets/css/just-the-docs-custom.css">
統一期貨API元件

<a id="pfcf.LoginResponse"></a>

## LoginResponse Objects

```python
@dataclass
class LoginResponse()
```

登入回覆物件

<a id="pfcf.LoginResponse.ok"></a>

#### ok

是否成功

<a id="pfcf.LoginResponse.error"></a>

#### error

錯誤訊息

<a id="pfcf.Pfcf"></a>

## Pfcf Objects

```python
class Pfcf()
```

<a id="pfcf.Pfcf.login_status_flag"></a>

#### login\_status\_flag

登入旗標 True:登入 False:未登入

<a id="pfcf.Pfcf.dtrade"></a>

#### dtrade

內期交易元件(必需登入才可以使用)

<a id="pfcf.Pfcf.ftrade"></a>

#### ftrade

外期交易元件(必需登入才可以使用)

<a id="pfcf.Pfcf.dquote"></a>

#### dquote

內期報價元件(必需登入才可以使用)

<a id="pfcf.Pfcf.fquote"></a>

#### fquote

外期報價元件(必需登入才可以使用)

<a id="pfcf.Pfcf.daccount"></a>

#### daccount

內期帳務元件(必需登入才可以使用)

<a id="pfcf.Pfcf.faccount"></a>

#### faccount

外期帳務元件(必需登入才可以使用)

<a id="pfcf.Pfcf.on_error"></a>

#### on\_error

錯誤事件

<a id="pfcf.Pfcf.login"></a>

#### login

```python
def login(url, userid, password, ca_path, ca_password) -> LoginResponse
```

登入
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| url|str | 主機 |     
| userid | str | 帳號 |  
| password | str | 密碼 |  
| ca_path | str | 憑證路徑 |   
| ca_password | str | 憑證密碼 |  

##### Returns LoginResponse

| Type | Description |
| ------ | ------------- |
| bool | True 成功 /False 失敗 |    
| str | 錯誤訊息 |

<a id="pfcf.Pfcf.logout"></a>

#### logout

```python
def logout()
```

登出

<a id="pfcf.Pfcf.get_domestic_products"></a>

#### get\_domestic\_products

```python
def get_domestic_products()
```

取得內期商品檔
##### Returns DomesticProducts

<a id="pfcf.Pfcf.get_foreign_products"></a>

#### get\_foreign\_products

```python
def get_foreign_products()
```

取得外期商品檔
##### Returns ForeignProducts

<a id="pfcf.Pfcf.get_exchanges"></a>

#### get\_exchanges

```python
def get_exchanges()
```

取得外期交易所
##### Returns EXCHANGE

<a id="pfcf.Pfcf.get_domestic_contracts"></a>

#### get\_domestic\_contracts

```python
def get_domestic_contracts(symbol, type) -> DomesticContractResponse
```

取得內期合約檔
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| symbol | str | 商品代碼 |         
| type | str | 類別 F期貨 O選擇權 |  

##### Returns DomesticContractResponse

| Type | Description |
| ------ | ------------- |
| bool | True 成功 /False 失敗 |    
| str | 錯誤訊息 |    
| DomesticContract | 商品合約資料 |

<a id="pfcf.Pfcf.get_foreign_contracts"></a>

#### get\_foreign\_contracts

```python
def get_foreign_contracts(exchange, symbol, type) -> ForeignContractResponse
```

取得外期商品檔
##### Parameters 

| Name | Type | Description |
| ------ | ------ | ------------- |
| exchange | str | 交易所 |         
| symbol |str | 商品 |         
| type | str | 類別 F期貨 O選擇權 |         

##### Returns ForeignContractResponse

| Type | Description |
| ------ | ------------- |
| bool | True 成功 /False 失敗 |    
| str | 錯誤訊息 |    
| ForeignContract | 商品合約資料 |

<a id="pfcf.Pfcf.get_accounts"></a>

#### get\_accounts

```python
def get_accounts()
```

取得交易帳號

