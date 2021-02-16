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
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424065"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает строку ASCII, представляющую составной идентификатор записи для объекта, обычно сообщения в хранилище сообщений. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
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
  
> [in] Указатель на сеанс, который использует клиентский приложение. 
    
 _cbStoreRecordKey_
  
> [in] Размер (в bytes) ключа записи в хранилище сообщений, которое содержит сообщение или другой объект. Если в параметре  _cbStoreRecordKey_ передается ноль, параметр  _pszMsgID_ указывает на копию идентификатора записи, преобразованного в текст. 
    
 _pStoreRecordKey_
  
> [in] Указатель на ключ записи в хранилище сообщений, которое содержит сообщение или другой объект. 
    
 _cbMsgEID_
  
> [in] Размер (в bytes) идентификатора записи сообщения или другого объекта. 
    
 _pMsgEID_
  
> [in] Указатель на идентификатор записи объекта. 
    
 _pszMsgID_
  
> [out] Указатель на возвращенную строку ASCII. Если параметр  _cbStoreRecordKey больше_ нуля, параметр  _pszMsgID_ указывает на составной идентификатор записи, преобразованный в текст. Если  _cbStoreRecordKey_ имеет нулевое значение,  _pszMsgID_ указывает на некомпонентный идентификатор записи, преобразованный в текст. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Если сообщение или другой объект, для которого создается идентификатор составной записи, находится в хранилище сообщений, строка идентификатора создается из идентификатора записи объекта и ключа записи магазина. Если объект не находится в хранилище, то есть если количество вбайтов для ключа записи магазина, переданного в параметр  _cbStoreRecordKey,_ — ноль, идентификатор записи объекта просто копируется и преобразуется в строку. 
  
Вызов **функции HrComposeMsgID** эквивалентен вызову функции [HrComposeEID,](hrcomposeeid.md) а затем [функции HrSzFromEntryID.](hrszfromentryid.md) 
  
 **HrComposeMsgID** позволяет клиентские приложения работать с объектами в нескольких хранилищах с помощью составных идентификаторов записей. Приложение может вызвать функцию [HrDecomposeMsgID,](hrdecomposemsgid.md) чтобы разделить идентификатор составной записи на исходные составляющие. 
  

