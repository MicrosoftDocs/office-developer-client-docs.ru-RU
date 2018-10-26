---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570879"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск последнего вхождения знака в string символом null. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null для поиска. 
    
 _Кан_
  
> [in] Знак для поиска.
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindLastCh** возвращает указатель на последнего вхождения знаков в строке. Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Замечания

Функция **SzFindLastCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия. Поиск в формате Юникод и DBCS поддерживаются. 
  

