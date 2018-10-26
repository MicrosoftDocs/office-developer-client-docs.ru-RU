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
ms.openlocfilehash: 8dbb871a234d94f8bb2e21b15ce5de6f0db0e4ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581834"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Карты SCODE возвращать значение из объекта хранилища OLE к типу HRESULT. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Параметры

 _StgSCode_
  
> [in] Возвращаемое значение MAPI SCODE из объекта хранения для сопоставления с значение HRESULT.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и возвращается ожидаемым значением.
    
MAPI_E_CALL_FAILED 
  
> Невозможно найти соответствующее значение.
    
## <a name="remarks"></a>Замечания

MAPI предоставляет функцию **MapStorageSCode** для внутреннего использования компоненты MAPI, базовый реализаций сообщений в окне сообщения DLL-Библиотеку. Так как эти компоненты хранилище OLE сами, они должны иметь возможность сопоставления значений ошибок, возвращаемых для решения проблем с использованием хранилища OLE значение HRESULT. 
  
Для получения дополнительных сведений см [Структурированного хранилища](structured-storage-in-mapi.md). 
  

