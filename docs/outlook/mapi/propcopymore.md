---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 635525a1c2c3234d724534d225eb07022afc9956
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592124"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует значения одного свойства из исходного расположения в месте назначения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValueDest_
  
> [out] Указатель на место, к которому эта функция записывает структуру [SPropValue](spropvalue.md) определение значение скопированные свойства. 
    
 _lpSPropValueSrc_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) , которое содержит значение свойства для копирования. 
    
 _lpfAllocMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , можно использовать для выделения дополнительной памяти, если в месте назначения недостаточно для хранения свойства для копирования. 
    
 _lpvObject_
  
> [in] Указатель на объект, для которого **MAPIAllocateMore** будет выделить пространство, если это необходимо. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Копирование значения одного свойства было выполнено успешно.
    
MAPI_E_NO_SUPPORT
  
> Обнаружен неизвестный тип свойства.
    
## <a name="remarks"></a>Замечания

Клиентское приложение или поставщик услуг можно использовать функцию **PropCopyMore** для копирования свойство из таблицы, который должен освободить для использования в других местах. 
  
 **PropCopyMore** не нужно выделить память, пока скопированы значение свойства типа, например PT_STRING8, который не помещается в структуре [SPropValue](spropvalue.md) . Для этих свойств больших функцию выделение памяти, с помощью функции [MAPIAllocateMore](mapiallocatemore.md) , к которому передается указатель в параметре _lpfAllocMore_ . 
  
Injudicious использования памяти фрагментов **PropCopyMore** ; Рекомендуется использовать функцию [ScCopyProps](sccopyprops.md) . 
  

