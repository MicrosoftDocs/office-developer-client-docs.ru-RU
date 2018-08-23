---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582044"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает строку ASCII, представляющий идентификатор составные записи для объекта, обычно сообщения в банке сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Параметры

 _psession_
  
> [in] Указатель на сеанс используется клиентским приложением. 
    
 _cbStoreRecordKey_
  
> [in] Размер, в байтах, ключ записи хранилища сообщений, который содержит сообщение или другой объект. Если нулевой передается в параметре _cbStoreRecordKey_ , указывает параметр _pszMsgID_ на копию идентификатор записи преобразуется в текст. 
    
 _pStoreRecordKey_
  
> [in] Указатель на ключ записи хранилища сообщений, который содержит сообщение или другой объект. 
    
 _cbMsgEID_
  
> [in] Размер, в байтах, идентификатор записи сообщение или другой объект. 
    
 _pMsgEID_
  
> [in] Указатель на запись идентификатор объекта. 
    
 _pszMsgID_
  
> [out] Указатель на Возвращенная строка ASCII. Если параметр _cbStoreRecordKey_ больше нуля, указывает параметр _pszMsgID_ на идентификатор составные записи преобразуется в текст. Если _cbStoreRecordKey_ равно нулю, _pszMsgID_ указывает идентификатор noncompound записи преобразуется в текст. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если сообщение или другой объект, для которого создается идентификатор составные записи находится в хранилище сообщений, строка идентификатора создается идентификатор объекта записи и хранения записи ключа. Если объект не в хранилище, то есть, если количество байтов для ключа записи хранилища, переданной в параметре _cbStoreRecordKey_ равно нулю, идентификатор объекта записи просто копируется и преобразован в строку. 
  
Вызов функции **HrComposeMsgID** эквивалентен вызову функции [HrComposeEID](hrcomposeeid.md) , а затем функцию [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** позволяет клиентским приложениям для работы с объектами в нескольких хранилищ посредством использования идентификаторы составные записей. Приложение может вызвать функцию [HrDecomposeMsgID](hrdecomposemsgid.md) для разделения идентификатор составные записи в его исходное деловых партнеров. 
  

