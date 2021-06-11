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
ms.openlocfilehash: 8f71b30bd02af8f768da86218456feadda8ea1b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414804"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, являются ли два свойства MAPI одинаковыми. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Parameters

 _lpName1_
  
> [in] Указатель на [структуру MAPINAMEID](mapinameid.md) с описанием первого имени свойства. 
    
 _lpName2_
  
> [in] Указатель на **структуру MAPINAMEID** с описанием второго имени свойства. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Два имени свойств равны. 
    
FALSE 
  
> Два имени свойств не являются равными.
    
## <a name="remarks"></a>Примечания

Функция **FEqualNames** полезна, так как структура **MAPINAMEID** содержит [GUID](guid.md) и может представлять само имя свойства несколько способов. Это означает, что две структуры нельзя сравнивать простыми двоичными методами. 
  
Процесс тестирования является конфиденциальным для строк имени свойства. 
  

