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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581981"
---
# <a name="scduppropset"></a>ScDupPropset

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Дублирует массива значение свойства в один блок памяти MAPI, объединяя операции функции [ScCopyProps](sccopyprops.md) и [ScCountProps](sccountprops.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a>Параметры

 _cprop_
  
> [in] Число значений свойств в массива, указанного в параметре _rgprop_ . 
    
 _rgprop_
  
> [in] Указатель на массив структур [SPropValue](spropvalue.md) определение значения свойств дублирование. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти для повторяющихся массива. 
    
 _prgprop_
  
> [out] Указатель на начальное положение в памяти хранения дублируемые возвращенный массив структур **SPropValue** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    

