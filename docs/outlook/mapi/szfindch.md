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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345243"
---
# <a name="szfindch"></a>SzFindCh
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Ищет первое вхождение символа в строке с завершающим нулем. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a>Параметры

_лпсз_
  
> возврата Указатель на строку с завершающим нулем для поиска. 
    
_CH_
  
> возврата Символ, для которого необходимо выполнить поиск.
    
## <a name="return-value"></a>Возвращаемое значение

**Сзфиндч** возвращает указатель на первое вхождение символа в строке. Если символ не встречается в строке или параметр _лпсз_ имеет значение null, возвращается значение null. 
  
## <a name="remarks"></a>Комментарии

Функция **сзфиндч** выполняет поиск только точного совпадения; Это зависит от регистра и диакритических различий. Поисковые запросы поддерживаются в форматах Юникод и DBCS. 
  

