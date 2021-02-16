---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404437"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отделяет представление ASCII составного идентификатора записи объекта ( обычно сообщения в хранилище сообщений) в идентификатор записи этого объекта в хранилище и идентификатор записи в хранилище. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a>Параметры

 _psession_
  
> [in] Указатель на сеанс, который использует клиентский приложение. 
    
 _szMsgID_
  
> [in] Строка, представляющая идентификатор записи объекта. 
    
 _pcbStoreEID_
  
> [out] Указатель на возвращенный размер (в bytes) идентификатора записи в хранилище сообщений, которое содержит объект. Если параметр  _szMsgID_ указывает на несочетаемую строку идентификатора записи, параметр  _pcbStoreEID_ указывает на ноль. 
    
 _ppStoreEID_
  
> [out] Указатель на указатель на возвращенный идентификатор записи в хранилище сообщений, содержаном объект. Если параметр  _szMsgID_ указывает на несовершенный идентификатор записи, в параметре  _ppStoreEID_ возвращается NULL. 
    
 _pcbMsgEID_
  
> [out] Указатель на возвращенный размер (в bytes) идентификатора записи объекта в его хранилище. Если параметр _szMsgID_ указывает на несочетаемую строку идентификатора записи, то параметр _pcbMsgEID_ равен значению параметра _cbEID._ 
    
 _ppMsgEID_
  
> [out] Указатель на указатель на возвращенную строку идентификатора записи объекта в его хранилище. Если параметр  _szMsgID_ указывает на несовершенный идентификатор записи,  _ppMsgEID_ указывает на указатель на преобразованную копию несовершенного идентификатора записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Если идентификатор, указанный параметром  _szMsgID,_ является составным, он преобразуется из ASCII и делится на идентификатор записи объекта в хранилище сообщений и идентификатор записи в хранилище. Строки идентификатора несочетаемой записи просто преобразуются и копируется. Составная строка идентификатора, которая должна быть разделена, обычно создается функцией [HrComposeMsgID.](hrcomposemsgid.md) 
  
Вызов **функции HrDecomposeMsgID эквивалентен** вызову функции [HrEntryIDFromSz,](hrentryidfromsz.md) а затем [— функции HrDecomposeEID.](hrdecomposeeid.md) 
  

