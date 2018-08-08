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
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808807"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Относится к**: Outlook 
  
Обновляет объект таблицы MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Используйте один из следующих значений: 
    
нуль (0)
  
> Используйте значение член **ulRowFlags** структуры [ROWENTRY](rowentry.md) . 
    
ACLTABLE_FREEBUSY
  
> Задает новый правами.
    
frightsFreeBusyDetailed
  
> При передаче ACLTABLE_FREEBUSY предоставляет подробное отображение новые права сведениям о доступности.
    
frightsFreeBusySimple
  
> При передаче ACLTABLE_FREEBUSY предоставляет простого отображения новые права сведениям о доступности.
    
ROWLIST_REPLACE
  
> Замените все строки в таблице.
    
 _lpMods_
  
> [in] Указывает на [ROWLIST](rowlist.md) структура, содержащая свойства для объекта в таблице. 
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |Mfcmapi (en) использует метод **IExchangeModifyTable::ModifyTable** для обратной записи измененные правила в таблице правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

