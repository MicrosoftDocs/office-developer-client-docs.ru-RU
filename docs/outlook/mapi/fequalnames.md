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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334883"
---
# <a name="fequalnames"></a>FEqualNames

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, совпадают ли два именованных свойства MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FEqualNames(
  LPMAPINAMEID lpName1,
  LPMAPINAMEID lpName2
);
```

## <a name="parameters"></a>Параметры

 _lpName1_
  
> возврата Указатель на структуру [мапинамеид](mapinameid.md) , описывающую первое именованное свойство. 
    
 _lpName2_
  
> возврата Указатель на структуру **мапинамеид** , описывающую второе именованное свойство. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Два имени свойств совпадают. 
    
FALSE 
  
> Два имени свойств не равны.
    
## <a name="remarks"></a>Комментарии

Функция **фекуалнамес** полезна, так как структура **мапинамеид** содержит [GUID](guid.md) и может представлять имя свойства более одного способа. Это означает, что две структуры не могут сравниваться простыми двоичными методами. 
  
В процессе тестирования учитывается регистр для строк имени свойства. 
  

