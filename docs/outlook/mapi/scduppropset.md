---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406019"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Дублирует массив значений свойств в одном блоке памяти MAPI, сочетающий операции функций [ScCopyProps](sccopyprops.md) и [ScCountProps.](sccountprops.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Количество значений свойств в массиве, указанных _параметром rgprop._ 
    
 _rgprop_
  
> [in] Указатель на массив [структур SPropValue,](spropvalue.md) определяющих повторяющиеся значения свойств. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти для дубликатного массива. 
    
 _prgprop_
  
> [вышел] Указатель на исходное положение в памяти, где хранится возвращаемая дублированная массива структур **SPropValue.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    

