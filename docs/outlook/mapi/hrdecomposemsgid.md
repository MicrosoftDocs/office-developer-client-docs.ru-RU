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
ms.openlocfilehash: 3095907498b1ce7ae6b3666e0678dd0c5f76c23e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808657"
---
# <a name="hrdecomposemsgid"></a>HrDecomposeMsgID

  
  
**Относится к**: Outlook 
  
Разделяет представления ASCII составные запись идентификатор объекта, обычно сообщения в банке сообщений в идентификатор записи этого объекта в хранилище и идентификатор записи хранилища. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
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
  
> [in] Указатель на сеанс используется клиентским приложением. 
    
 _szMsgID_
  
> [in] Строка, представляющая запись идентификатор объекта. 
    
 _pcbStoreEID_
  
> [out] Указатель на возвращаемый размер, в байтах, идентификатор записи хранилища сообщение, содержащее объект. Если параметр _szMsgID_ указывает идентификатор noncompound записи строка, затем указывает параметр _pcbStoreEID_ присваивается значение 0. 
    
 _ppStoreEID_
  
> [out] Указатель на указатель на идентификатор возвращенного элемента хранилища сообщение, содержащее объект. Если параметр _szMsgID_ указывает идентификатор noncompound записи, с помощью параметра _ppStoreEID_ возвращается значение NULL. 
    
 _pcbMsgEID_
  
> [out] Указатель на возвращаемый размер, в байтах, запись идентификатор объекта в его хранилище. Если параметр _szMsgID_ указывает строка идентификатора noncompound запись, параметр _pcbMsgEID_ равно значению параметра _cbEID_ . 
    
 _ppMsgEID_
  
> [out] Указатель на указатель строки идентификатора возвращенного элемента объекта в его хранилище. Если параметр _szMsgID_ указывает идентификатор noncompound записи, _ppMsgEID_ указывает указатель преобразованной копии идентификатор noncompound записи. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если идентификатор, указанный в параметре _szMsgID_ составные, преобразованных из ASCII и разделены на идентификатор записи объекта в его хранилища сообщений и идентификатор записи хранилища. Строки идентификатора noncompound запись просто преобразуются и копируются. Составные идентификатор строку, которую нужно разделить — это обычно один создан с помощью функции [HrComposeMsgID](hrcomposemsgid.md) . 
  
Вызов функции **HrDecomposeMsgID** эквивалентен вызову функции [HrEntryIDFromSz](hrentryidfromsz.md) , а затем функцию [HrDecomposeEID](hrdecomposeeid.md) . 
  

