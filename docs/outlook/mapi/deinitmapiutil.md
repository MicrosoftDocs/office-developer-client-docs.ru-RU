---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336843"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освобождает функции служебных программ, которые вызываются явно функцией [сЦинитмапиутил](scinitmapiutil.md) , или неявно функцией [мапиинитиализе](mapiinitialize.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Параметры

Нет 
  
## <a name="return-value"></a>Возвращаемое значение

Нет 
  
## <a name="remarks"></a>Комментарии

Функции выпуска функции **деинитмапиутил** , инициализированные с помощью [сЦинитмапиутил](scinitmapiutil.md) или [мапиинитиализе](mapiinitialize.md). 
  
При завершении использования функций, вызываемых **сЦинитмапиутил** , **деинитмапиутил** необходимо явно вызывать, чтобы освободить их. В отличие от этого, [мапиунинитиализе](mapiuninitialize.md) неявно вызывает **деинитмапиутил**. 
  

