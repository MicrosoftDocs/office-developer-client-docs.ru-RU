---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421944"
---
# <a name="szfindch"></a>SzFindCh
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поиск первого появления символа в строке с null-terminated. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Parameters

_lpsz_
  
> [in] Указатель на строку null-terminated, которая будет искаться. 
    
_ch_
  
> [in] Символ, который нужно искать.
    
## <a name="return-value"></a>Возвращаемое значение

**SzFindCh** возвращает указатель на первое появление символа в строке. Если символ не встречается нигде в строке, или если параметр  _lpsz_ является NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Примечания

Функция **SzFindCh** ищет только точный совпадение; он чувствителен к различиям в случае и диакритических различиях. Поддерживаются поиски в форматах Unicode и DBCS. 
  

