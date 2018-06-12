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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: f65f047a73a2c06ca02251c554e5dca42352b6c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808550"
---
# <a name="getinstance"></a>GetInstance

  
  
**Применимо к**: Outlook 
  
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

## <a name="parameters"></a>Parameters

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
  

