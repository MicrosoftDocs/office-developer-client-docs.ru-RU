---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588148"
---
# <a name="fbadrglpnameid"></a>FBadRglpNameID

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Проверяет массив структур, которые описывают с именем свойства и проверяет их выделении. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a>Параметры

 _lppNameId_
  
> [in] Указатель на массив структур [MAPINAMEID](mapinameid.md) , описывающее именованных свойств. 
    
 _записи CNAME_
  
> [in] Число структур именованное свойство в массиве указывает параметр _lppNameId_ . 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Один или несколько структур имя указанного свойства является недопустимым. 
    
FALSE 
  
> Структуры имя указанного свойства являются допустимыми.
    
## <a name="remarks"></a>Замечания

Функция **FBadRglpNameID** можно использовать при настройке для вызова [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) или [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md). 
  

