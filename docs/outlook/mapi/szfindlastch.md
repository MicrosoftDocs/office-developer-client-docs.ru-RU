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
ms.openlocfilehash: f22d30c1bc7c797834f58bcd1306b14ac2542c6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345138"
---
# <a name="szfindlastch"></a>SzFindLastCh

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Ищет последнее вхождение символа в строке с завершающим нулем. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindLastCh(
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

 **Сзфиндластч** возвращает указатель на последнее вхождение символа в строке. Если символ не встречается в строке или параметр _лпсз_ имеет значение null, возвращается значение null. 
  
## <a name="remarks"></a>Комментарии

Функция **сзфиндластч** выполняет поиск только точного совпадения; Это зависит от регистра и диакритических различий. Поисковые запросы поддерживаются в форматах Юникод и DBCS. 
  

