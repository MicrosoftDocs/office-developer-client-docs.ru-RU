---
title: MapStorageSCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MapStorageSCode
api_type:
- COM
ms.assetid: f686a2bc-aba5-4ea3-9963-76d0e96eab50
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5dce5de820c07e1fa7b25b87d87993a30961b3f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416526"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сопоирует возвращаемого значения SCODE из объекта хранилища OLE с типом HRESULT. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Imessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Параметры

 _StgSCode_
  
> [in] MapI SCODE return value from an OLE storage object to be mapped to a HRESULT value.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвращен ожидаемое значение.
    
MAPI_E_CALL_FAILED 
  
> Функция не может найти совпадающие значения.
    
## <a name="remarks"></a>Примечания

MAPI предоставляет **функцию MapStorageSCode** для внутреннего использования компонентов MAPI, которые базируют свои реализации сообщений на DLL сообщения. Так как эти компоненты открывают хранилище OLE самостоятельно, они должны иметь возможность соедооставить значения ошибок, возвращенные при проблемах с хранилищем OLE, со значением HRESULT. 
  
Дополнительные сведения см. в [подстройки "Структурированное хранилище".](structured-storage-in-mapi.md) 
  

