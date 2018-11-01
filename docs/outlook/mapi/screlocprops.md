---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576850"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Регулировка указатели в массиве [SPropValue](spropvalue.md) после массива и его данные были скопированы или перемещены в новое расположение. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _cprop_
  
> [in] Число свойств в массиве указывает параметр _rgprop_ . 
    
 _rgprop_
  
> [in] Указатель на массив структур [SPropValue](spropvalue.md) , для которых должны быть настроены указатели. 
    
 _pvBaseOld_
  
> [in] Указатель на исходный базовый адрес массива, на который указывает параметр _rgprop_ . 
    
 _pvBaseNew_
  
> [in] Указатель на новый базовый адрес массива, на который указывает параметр _rgprop_ . 
    
 _печатной_
  
> [in, out] Необязательный указатель на размер, в байтах, массива, указанного в параметре _pvBaseNew_ . Если это не имеет значение NULL, параметр _печатной_ число байтов, сохраненных в параметре _pvD_ . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Указатели были настроены успешно.
    
MAPI_E_INVALID_PARAMETER
  
> Один или оба параметра были недопустимый или обнаружен неизвестный тип свойства.
    
## <a name="remarks"></a>Замечания

Функция **ScRelocProps** работает предполагается, что массива значение свойства, для которого настроены указатели сначала выделенная в один вызов следующего вызова функции **ScCopyProps** . Если клиентское приложение или поставщик услуг работает со значением свойства, построенного из несвязанное блоки памяти, его следует использовать [ScCopyProps](sccopyprops.md) для копирования вместо этого свойства. 
  
 **ScRelocProps** позволяет сохранить целостность указатели в массиве [SPropValue](spropvalue.md) . Для обеспечения допустимости указатели при такой массив для записи и чтения с диска, выполните следующие операции: 
  
1. Прежде чем записи массива и данных на диск, вызовите **ScRelocProps** массива с параметром _pvBaseNew_ , например с указанием некоторые стандартные нулевые значения. 
    
2. После прочтения массива и данных с диска, вызовите **ScRelocProps** массива с помощью параметра _pvBaseOld_ равно значению же standard используется в шаге 1. Массив и данных необходимо прочитать в буфер, созданных с помощью за одну операцию. 
    
3. Это необязательный параметр _печатной_ для **ScRelocProps** . 
    
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

