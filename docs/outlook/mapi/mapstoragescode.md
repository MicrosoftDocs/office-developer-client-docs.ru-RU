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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357633"
---
# <a name="mapstoragescode"></a>MapStorageSCode

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сопоставляет возвращаемое значение SCODE из объекта OLE Storage с типом HRESULT. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |IMessage. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE MapStorageSCode(
  SCODE StgSCode
);
```

## <a name="parameters"></a>Параметры

 _Стгскоде_
  
> возврата SCODE MAPI возвращает значение из объекта OLE Storage, которое должно быть сопоставлено со значением HRESULT.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и возвращено ожидаемое значение.
    
МАПИ_Е_КАЛЛ_ФАИЛЕД 
  
> Функции не удается найти совпадающее значение.
    
## <a name="remarks"></a>Примечания

MAPI предоставляет функцию **мапсторажескоде** для внутреннего использования компонентами MAPI, которые основаны на их реализациях сообщений в DLL сообщений. Так как эти компоненты самостоятельно открывают хранилище OLE, они должны иметь возможность сопоставлять значения ошибок, возвращаемые для проблем с хранилищем OLE, со значением HRESULT. 
  
Более подробную информацию можно узнать в разделе [структурированНое хранилище](structured-storage-in-mapi.md). 
  

