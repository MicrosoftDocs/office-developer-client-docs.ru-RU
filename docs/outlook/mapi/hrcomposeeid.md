---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429049"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор составной записи для объекта, обычно сообщения в хранилище сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Параметры

 _psession_
  
> [in] Указатель на сеанс, который использует клиентский приложение. 
    
 _cbStoreRecordKey_
  
> [in] Размер (в bytes) ключа записи в хранилище сообщений, которое хранит сообщение или другой объект. Если в параметре  _cbStoreRecordKey_ передается ноль, параметр  _ppEID_ указывает на копию идентификатора записи объекта. 
    
 _pStoreRecordKey_
  
> [in] Указатель на ключ записи в хранилище сообщений, которое содержит сообщение или другой объект. 
    
 _cbMsgEID_
  
> [in] Размер (в bytes) идентификатора записи сообщения или другого объекта. 
    
 _pMsgEID_
  
> [in] Указатель на идентификатор записи объекта. 
    
 _pcbEID_
  
> [out] Указатель на размер возвращаемого идентификатора (в bytes). 
    
 _ppEID_
  
> [out] Указатель на указатель на возвращенный идентификатор записи. Если значение параметра  _cbStoreRecordKey_ больше нуля, параметр  _ppEID_ указывает на указатель на созданный идентификатор составной записи. Если  _cbStoreRecordKey_ имеет нулевое значение,  _ppEID_ указывает на указатель на копию идентификатора записи объекта. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Если сообщение или другой объект, для которого создается составной идентификатор записи, находится в хранилище сообщений, идентификатор создается из идентификатора записи объекта и ключа записи магазина. Если объект находится не в хранилище, то есть если количество вбайтов для ключа записи магазина, переданного  _в cbStoreRecordKey,_ — ноль, идентификатор записи объекта просто копируется. 
  
Функция **HrComposeEID** позволяет приложениям работать с объектами в нескольких хранилищах с помощью составных идентификаторов записей. Приложение может вызвать функцию [HrDecomposeEID,](hrdecomposeeid.md) чтобы разделить идентификатор составной записи на исходные составляющие. 
  
## <a name="see-also"></a>См. также



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

