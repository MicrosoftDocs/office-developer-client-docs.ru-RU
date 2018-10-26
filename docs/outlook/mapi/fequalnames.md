---
title: FEqualNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FEqualNames
api_type:
- COM
ms.assetid: 4dd58b0b-dc39-4782-a9ec-05e353c90927
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 09c6540f2a224b7dc89a62c34cfb0c867cef4632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570851"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, одинаковы ли два MAPI с именем свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Параметры

 _lpName1_
  
> [in] Указатель на структуру [MAPINAMEID](mapinameid.md) , описывающий первый именованное свойство. 
    
 _lpName2_
  
> [in] Указатель на структуру **MAPINAMEID** , описывающее второй именованное свойство. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Имена двух свойство равны. 
    
FALSE 
  
> Имена двух свойств не совпадают.
    
## <a name="remarks"></a>Замечания

Функция **FEqualNames** полезен, так как структура **MAPINAMEID** содержит [идентификатор GUID](guid.md) и может представлять имя свойства в несколько способов. Это означает, что две структуры нельзя сравнивать простой двоичные методами. 
  
Процесс тестирования задается с учетом регистра для строк имя свойства. 
  

