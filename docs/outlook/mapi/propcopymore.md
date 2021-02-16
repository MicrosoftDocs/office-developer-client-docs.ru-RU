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
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404472"
---
# <a name="propcopymore"></a>PropCopyMore

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует одно значение свойства из источника в расположение назначения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
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
  
> [out] Указатель на расположение, в которое эта функция записывает [структуру SPropValue,](spropvalue.md) определяя значение скопированных свойств. 
    
 _lpSPropValueSrc_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) которая содержит значение свойства, которое необходимо скопировать. 
    
 _lpfAllocMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти, если расположение назначения недостаточно велико для скопации свойства. 
    
 _lpvObject_
  
> [in] Указатель на объект, для которого **MAPIAllocateMore выделяет** пространство при необходимости. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Значение одного свойства было успешно скопировано.
    
MAPI_E_NO_SUPPORT
  
> Был известен неизвестный тип свойства.
    
## <a name="remarks"></a>Примечания

Клиентские приложения или поставщик службы могут использовать функцию **PropCopyMore** для копирования свойства из таблицы, которая будет освобождена, чтобы использовать его в другом месте. 
  
 **PropCopyMore** не нужно выделять память, если скопированные значения свойства не соответствуют типу, например PT_STRING8, который не помещается в структуру [SPropValue.](spropvalue.md) Для этих больших свойств функция выделяет память с помощью функции [MAPIAllocateMore,](mapiallocatemore.md) в которую указатель передается в _параметре lpfAllocMore._ 
  
Неправиленное использование **памяти фрагментов PropCopyMore;** вместо этого можно [использовать функцию ScCopyProps.](sccopyprops.md) 
  

