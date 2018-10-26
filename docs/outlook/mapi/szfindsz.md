---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0075db0a515166c5185657daf3fc6b1e121d6672
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585124"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поиск первого вхождения подстроки символом null в строку символом null. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null для поиска. Параметр _lpsz_ не должен превышать 65536 символов. 
    
 _lpszKey_
  
> [in] Указатель на подстроки символом null для поиска. Параметр _lpszKey_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindSz** возвращает указатель на первый символ первого вхождения подстроки в строке. Если подстрока не происходит в строке, в любом месте, если _lpszKey_ больше, чем _lpsz_или один из параметров имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Замечания

Функция **SzFindSz** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия. Поиск в форматах Юникод и DBCS поддерживаются. Ограничение длины на оба параметра — в символы, не обязательно в байтах. 
  

