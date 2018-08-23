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
ms.openlocfilehash: c4e5d2847b53988fb75e23fc6c4dfc386ea678f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579265"
---
# <a name="getinstance"></a>GetInstance

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Копирует одно значение в рамках свойством одним значением свойства одного типа. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIUTIL. H  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
VOID GetInstance(
  LPSPropValue pvalMv,
  LPSPropValue pvalSv,
  ULONG uliInst
);
```

## <a name="parameters"></a>Параметры

 _pvalMv_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) определения многозначные свойства. 
    
 _pvalSv_
  
> [in] Указатель на поддерживающий одно свойство для получения данных. 
    
 _uliInst_
  
> [in] Номер экземпляра, который является, элемент массива копируются из структуры, указанное с помощью параметра _pvalMv_ значения. 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Если значение копируются слишком велик для выделенной памяти, функция **GetInstance** копирует только указателей вместо выделения памяти. 
  

