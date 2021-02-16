---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406341"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск указанного свойства в наборе свойств.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _rgprop_
  
> [in] Массив структур [SPropValue,](spropvalue.md) которые определяют свойства для поиска. 
    
 _cprop_
  
> [in] Количество свойств в наборе свойств, указанных _параметром rgprop._ 
    
 _ulPropTag_
  
> [in] Тег свойства для свойства, который требуется найти в наборе свойств, указанных _параметром rgprop._ 
    
## <a name="return-value"></a>Возвращаемое значение

 **PpropFindProp** возвращает [структуру SPropValue,](spropvalue.md) определяя свойство, которое соответствует тегу входного свойства, или NULL, если совпадений нет. 
  
## <a name="remarks"></a>Примечания

Если указанный тег свойства указывает свойство типа PT_UNSPECIFIED, функция **PpropFindProp** находит совпадение только для идентификатора свойства в теге. В противном случае он находит совпадение для всего тега свойства, включая тип свойства, и возвращает идентифицированное свойство. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI использует метод **PpropFindProp** для поиска свойств в наборе свойств, добавляемом в список.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

