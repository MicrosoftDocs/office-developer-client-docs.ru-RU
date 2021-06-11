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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427348"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Освобождает функции утилиты, прямо называемые функцией [ScInitMapiUtil](scinitmapiutil.md) или неявно функцией [MAPIInitialize.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Параметры

Нет 
  
## <a name="return-value"></a>Возвращаемое значение

Нет 
  
## <a name="remarks"></a>Примечания

Функции **выпуска функций DeinitMapiUtil,** инициализированные [с помощью ScInitMapiUtil](scinitmapiutil.md) или [MAPIInitialize.](mapiinitialize.md) 
  
Когда использование функций, называемых **ScInitMapiUtil,** завершено, **deinitMapiUtil** должен быть явно вызван, чтобы освободить их. Напротив, [MAPIUninitialize](mapiuninitialize.md) неявно вызывает **DeinitMapiUtil**. 
  

