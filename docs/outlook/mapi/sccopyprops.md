---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411010"
---
# <a name="sccopyprops"></a>ScCopyProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Копирует свойства, определенные массивом [структур SPropValue,](spropvalue.md) в новое назначение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Количество скопированные свойства. 
    
 _rgprop_
  
> [in] Указатель на массив [структур SPropValue,](spropvalue.md) которые определяют скопированные свойства. Параметр  _rgprop_ не должен указать на начало массива, но он должен указать на начало одной из структур **SPropValue** в массиве. 
    
 _pvDst_
  
> [in] Указатель на исходное положение в памяти, в которое эта функция копирует свойства. 
    
 _pcb_
  
> [вышел] Необязательный указатель на размер в bytes блока памяти, указываемого параметром _pvDst._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Свойства были успешно скопированы.
    
MAPI_E_INVALID_PARAMETER
  
> Неизвестен тип свойства.
    
## <a name="remarks"></a>Примечания

Новый массив и его данные находятся в буфере, созданном с одним выделением, и для настройки указателей в отдельных структурах [SPropValue](spropvalue.md) можно использовать функцию [ScRelocProps.](screlocprops.md) До этой корректировки указатели действительны. 
  
 **ScCopyProps** поддерживает исходный порядок свойств для скопированного массива свойств. 
  
Параметр _PCB_ необязателен; если это не NULL, оно задано для количества bytes, хранимого в _параметре pvDst._ 
  
## <a name="see-also"></a>См. также



[ScDupPropset](scduppropset.md)

