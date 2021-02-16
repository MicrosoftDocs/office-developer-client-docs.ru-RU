---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432235"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Находит локальный путь, аналог заданного UNC-пути. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Параметры

 _szUNC_
  
> [in] Путь в формате [ сервер ] путь ] файла \\  \[ или \[ каталога.
    
 _szLocal_
  
> [out] Путь в формате [ _диск:_ путь ] того же файла или каталога, что и для параметра \[  _szUNC._ 
    
 _cchLocal_
  
> [in] Размер буфера для строки вывода.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Локальный путь успешно расположен.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ не был достаточно большим для удержания результата. 
    
S_FALSE
  
> Строка UNC уже была локальным путем.
    
MAPI_E_NOT_FOUND
  
> Локальный путь не найден.
    
## <a name="see-also"></a>См. также



[ScUNCFromLocalPath](scuncfromlocalpath.md)

