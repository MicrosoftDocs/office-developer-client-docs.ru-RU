---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418178"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обновляет объект таблицы MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Используйте одно из следующих значений: 
    
0 (ноль)
  
> Используйте значение члена **ulRowFlags** структуры [ROWENTRY.](rowentry.md) 
    
ACLTABLE_FREEBUSY
  
> Задает новые права.
    
frightsFreeBusyDetailed
  
> При ACLTABLE_FREEBUSY предоставляет подробные сведения о новых правах на сведения о занятости.
    
frightsFreeBusySimple
  
> При ACLTABLE_FREEBUSY данные отображаются новые права занятости.
    
ROWLIST_REPLACE
  
> Замените все строки в таблице.
    
 _lpMods_
  
> [in] Указывает на [структуру ROWLIST,](rowlist.md) содержащую свойства объекта таблицы. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI использует метод **IExchangeModifyTable::ModifyTable** для записи измененного правила обратно в таблицу правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

