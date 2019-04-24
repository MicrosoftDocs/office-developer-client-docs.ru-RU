---
title: GetInstance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetInstance
api_type:
- COM
ms.assetid: cb432d52-6c96-45d2-bbde-45b0de3f915c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 936a20c4236ab76e5acdb178737c3044d3f53bfe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299547"
---
# <a name="getinstance"></a>GetInstance

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует одно значение из многозначного свойства в свойство с одним значением того же типа. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |МАПИУТИЛ. Высоты  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Параметры

 _Пвалмв_
  
> возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую многозначное свойство. 
    
 _Пвалсв_
  
> возврата Указатель на свойство с одним значением, чтобы получить данные. 
    
 _Улиинст_
  
> возврата Номер экземпляра (то есть, элемент массива) значения копируется из структуры, указанной параметром _пвалмв_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если копируемое значение слишком велико для выделенной памяти, функция **GetInstance** копирует только указатели вместо выделения новой памяти. 
  

