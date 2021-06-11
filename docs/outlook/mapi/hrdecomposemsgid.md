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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отделяет представление ASCII сложного идентификатора входа объекта, обычно сообщения в хранилище сообщений, в идентификатор входа этого объекта в магазине и идентификатор входа в хранилище. 
  
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

## <a name="parameters"></a>Parameters

 _psession_
  
> [in] Указатель на сеанс, который используется клиентом приложения. 
    
 _szMsgID_
  
> [in] Строка, представляющая идентификатор входа объекта. 
    
 _pcbStoreEID_
  
> [вышел] Указатель на возвращенный размер, в bytes, идентификатор входа в хранилище сообщений, который содержит объект. Если параметр  _szMsgID указывает_ на строку идентификатора некомпонентной записи, то параметр  _pcbStoreEID_ указывает на ноль. 
    
 _ppStoreEID_
  
> [вышел] Указатель на указатель на возвращенный идентификатор входа в хранилище сообщений, содержащий объект. Если _параметр szMsgID_ указывает на идентификатор некомпонентной записи, NULL возвращается в _параметре ppStoreEID._ 
    
 _pcbMsgEID_
  
> [вышел] Указатель на возвращенный размер в bytes идентификатора входа объекта в его хранилище. Если параметр _szMsgID_ указывает на строку идентификатора некомпонентной записи, то параметр _pcbMsgEID_ равен значению параметра _cbEID._ 
    
 _ppMsgEID_
  
> [вышел] Указатель на указатель на строку идентификатора возвращаемого входа объекта в магазине. Если параметр  _szMsgID_ указывает на идентификатор некомпонентной записи,  _ppMsgEID_ указывает на указатель на преобразованную копию идентификатора некомпонентной записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Если идентификатор, указанный  _параметром szMsgID,_ является составным, он преобразуется из ASCII и делится на идентификатор входа объекта в хранилище сообщений и идентификатор входа магазина. Строки идентификатора некомпонентной записи просто преобразуются и копируется. Выделенная строка идентификатора соединения обычно создается функцией [HrComposeMsgID.](hrcomposemsgid.md) 
  
Вызов **функции HrDecomposeMsgID** эквивалентен вызову функции [HrEntryIDFromSz,](hrentryidfromsz.md) а затем [функции HrDecomposeEID.](hrdecomposeeid.md) 
  

