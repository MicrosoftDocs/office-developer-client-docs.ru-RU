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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808654"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Применимо к**: Outlook 
  
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

## <a name="parameters"></a>Parameters

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

