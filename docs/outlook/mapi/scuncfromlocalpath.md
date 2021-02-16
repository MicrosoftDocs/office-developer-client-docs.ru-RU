---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414538"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Находит аналог UNC-пути для данного локального пути.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Параметры

 _szLocal_
  
> [in] Путь в формате [ _диск:_ путь ] файла \[ или каталога.
    
 _szUNC_
  
> [out] Путь в формате [ сервер ] путь ] того же файла или каталога, что и для \\  \[  \[  _параметра szLocal._ 
    
 _cchUNC_
  
> [in] Размер буфера для строки вывода.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Аналог UNC-пути успешно расположен.
    
MAPI_E_INVALID_PARAMETER
  
> Один или несколько параметров недопустимы.
    
MAPI_E_TOO_BIG
  
>  _SzUNC_ не был достаточно большим для удержания результата. 
    
S_FALSE
  
> Локальный путь уже был строкой UNC.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)

