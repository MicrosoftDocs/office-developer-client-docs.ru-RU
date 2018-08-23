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
ms.openlocfilehash: 335fac38ff3f084195a000ad32a27adcb85c1cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564817"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор составные запись для объекта, обычно сообщения в банке сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
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
  
> [in] Указатель на сеанс используется клиентским приложением. 
    
 _cbStoreRecordKey_
  
> [in] Размер, в байтах, ключ записи хранилища сообщений, удерживая сообщение или другой объект. Если нулевой передается в параметре _cbStoreRecordKey_ , параметр _ppEID_ указывает на копию идентификатором записи. 
    
 _pStoreRecordKey_
  
> [in] Указатель на ключ записи хранилища сообщений, который содержит сообщение или другой объект. 
    
 _cbMsgEID_
  
> [in] Размер, в байтах, идентификатор записи сообщение или другой объект. 
    
 _pMsgEID_
  
> [in] Указатель на запись идентификатор объекта. 
    
 _pcbEID_
  
> [out] Указатель на размер, в байтах, возвращенный идентификатор. 
    
 _ppEID_
  
> [out] Указатель на указатель на идентификатор, возвращенного элемента. Если значение параметра _cbStoreRecordKey_ больше нуля, параметр _ppEID_ указывает указатель на идентификатор составные записи, которая создается. Если _cbStoreRecordKey_ равно нулю, _ppEID_ указывает указатель на копию идентификатором записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если сообщение или другой объект, для которого создается идентификатор составные записи находится в хранилище сообщений, идентификатор создается идентификатор объекта записи и хранения записи ключа. Если объект не в хранилище, то есть, если количество байтов для ключа записи хранилища, переданные в _cbStoreRecordKey_ равно нулю, идентификатор объекта записи просто скопирован. 
  
Функция **HrComposeEID** позволяет приложениям для работы с объектами в нескольких хранилищ посредством использования идентификаторы составные записей. Приложение может вызвать функцию [HrDecomposeEID](hrdecomposeeid.md) для разделения идентификатор составные записи в его исходное деловых партнеров. 
  
## <a name="see-also"></a>См. также



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

