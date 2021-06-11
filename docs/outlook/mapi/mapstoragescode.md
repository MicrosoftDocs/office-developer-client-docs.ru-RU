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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Карты возвращаемого значения SCODE из объекта хранения OLE в тип HRESULT. 
  
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

## <a name="parameters"></a>Parameters

 _StgSCode_
  
> [in] Возвращаемая стоимость SCODE MAPI с объекта хранения OLE, который должен быть соизмелен со значением HRESULT.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение.
    
MAPI_E_CALL_FAILED 
  
> Функция не может найти совпадающие значения.
    
## <a name="remarks"></a>Примечания

MAPI предоставляет **функцию MapStorageSCode** для внутреннего использования компонентов MAPI, которые базируют реализацию сообщений на DLL сообщения. Поскольку эти компоненты сами открывают хранилище OLE, они должны иметь возможность составить карту значений ошибок, возвращающихся из-за проблем с хранилищем OLE, к значению HRESULT. 
  
Дополнительные сведения см. в [служба хранилища.](structured-storage-in-mapi.md) 
  

