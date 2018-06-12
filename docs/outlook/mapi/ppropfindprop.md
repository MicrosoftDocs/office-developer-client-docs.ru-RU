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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812073"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Применимо к**: Outlook 
  
Настройка поиска для указанного свойства в свойстве.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameters

 _rgprop_
  
> [in] Массив структур [SPropValue](spropvalue.md) , которые определяют свойства для поиска. 
    
 _cprop_
  
> [in] Число свойств в набор свойств, указанное с помощью параметра _rgprop_ . 
    
 _ulPropTag_
  
> [in] Свойство tag для свойства для поиска в набор свойств, указанное с помощью параметра _rgprop_ . 
    
## <a name="return-value"></a>������������ ��������

 **PpropFindProp** возвращает структуру [SPropValue](spropvalue.md) , определяющего свойство, соответствующий тег ввода свойство или значение NULL, если нет соответствия. 
  
## <a name="remarks"></a>Замечания

Если данное свойство tag указывает свойство типа PT_UNSPECIFIED, функция **PpropFindProp** будет выполняться только для идентификатора свойства в теге. В противном случае находит соответствие для тега всего свойства, включая тип свойства и возвращает свойство определяемую. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |Mfcmapi (en) использует метод **PpropFindProp** для поиска набора свойств в свойство, добавляемого в список.  <br/> |
   
## <a name="see-also"></a>См. также



[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

