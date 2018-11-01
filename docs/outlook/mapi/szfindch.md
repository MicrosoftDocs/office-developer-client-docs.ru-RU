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
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573525"
---
# <a name="szfindch"></a>SzFindCh
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск первого вхождения знака в string символом null. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
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

**SzFindCh** возвращает указатель на первого появления знаков в строке. Если кодировка не происходит в любом месте в строке или параметр _lpsz_ имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Замечания

Функция **SzFindCh** выполняется поиск точного совпадения. Это зависит от регистра и диакритических различия. Поиск в формате Юникод и DBCS поддерживаются. 
  

