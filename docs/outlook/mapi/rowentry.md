---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812166"
---
# <a name="rowentry"></a>ROWENTRY

**Относится к**: Outlook 
  
Содержит строку и операцию, выполняемую с этой строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> Один из следующих операций выполняется на данные. 
    
  - ROW_ADD: Добавление данных в таблицу как новую строку.
      
  - ROW_MODIFY: Изменение этой строки в таблице.
      
  - ROW_REMOVE: Удаление этой строки в таблице.
      
  - ROW_EMPTY: Не добавляйте строку данных в таблицу. (Строка является пустым.)
    
**cValues**
  
> Количество значений свойств в **rgPropvals**.
    
**rgPropVals**
  
> Массив структур [SPropValue](spropvalue.md) , представляющих значения столбцов для вставки в таблице. 
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Используются для формирования список выбранных правил для последующих действий **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>См. также
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Структуры MAPI](mapi-structures.md)

