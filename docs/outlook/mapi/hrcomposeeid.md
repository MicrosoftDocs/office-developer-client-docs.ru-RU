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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор сложной записи для объекта, как правило, сообщения в хранилище сообщений. 
  
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

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Указатель на сеанс, который используется клиентом приложения. 
    
 _cbStoreRecordKey_
  
> [in] Размер в bytes ключа записи в хранилище сообщений с сообщением или другим объектом. Если в  _параметре cbStoreRecordKey_ передается ноль, параметр  _ppEID_ указывает на копию идентификатора входа объекта. 
    
 _pStoreRecordKey_
  
> [in] Указатель на ключ записи в хранилище сообщений, содержащий сообщение или другой объект. 
    
 _cbMsgEID_
  
> [in] Размер в bytes идентификатора входа сообщения или другого объекта. 
    
 _pMsgEID_
  
> [in] Указатель на идентификатор входа объекта. 
    
 _pcbEID_
  
> [вышел] Указатель на размер в bytes возвращенного идентификатора. 
    
 _ppEID_
  
> [вышел] Указатель на указатель на возвращенный идентификатор записи. Если значение параметра  _cbStoreRecordKey_ больше нуля, параметр  _ppEID_ указывает на указатель на созданный идентификатор входной записи. Если  _значение cbStoreRecordKey_ нулевое,  _ppEID_ указывает на указатель на копию идентификатора входа объекта. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Если сообщение или другой объект, для которого создается идентификатор входного соединения, находится в хранилище сообщений, идентификатор создается из идентификатора входа объекта и ключа записи магазина. Если объект не находится в магазине, то есть если количество byte для ключа записи магазина, переданного  _в cbStoreRecordKey,_ ноль, идентификатор входа объекта просто копируется. 
  
Функция **HrComposeEID** позволяет приложениям работать с объектами в нескольких хранилищах с помощью идентификаторов сложных входов. Приложение может вызвать функцию [HrDecomposeEID,](hrdecomposeeid.md) чтобы разделить идентификатор входного соединения на исходные составляющие. 
  
## <a name="see-also"></a>См. также



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

