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
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436036"
---
# <a name="rowentry"></a>ROWENTRY

**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит строку и операцию, выполняемую с этой строкой в таблице через интерфейс [IExchangeModifyTable.](iexchangemodifytableiunknown.md) 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>"Участники"

**ulRowFlags**
  
> Одна из следующих операций, выполняемая с данными: 
    
  - ROW_ADD. Добавьте данные в таблицу в качестве новой строки.
      
  - ROW_MODIFY. Измените эту строку в таблице.
      
  - ROW_REMOVE. Удалите эту строку из таблицы.
      
  - ROW_EMPTY: не добавляйте данные строк в таблицу. (Строка пуста.)
    
**cValues**
  
> Количество значений свойств **в rgPropvals.**
    
**rgPropVals**
  
> Массив структур [SPropValue,](spropvalue.md) представляющих значения столбцов, которые необходимо вставить в таблицу. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Используется для создания списка выбранных правил для последующих действий **ModifyTable.**  <br/> |
   
## <a name="see-also"></a>См. также
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Структуры MAPI](mapi-structures.md)

