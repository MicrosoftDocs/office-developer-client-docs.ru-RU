---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578992"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на интерфейс для объекта таблицы MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Зарезервировано; должен иметь значение 0 (ноль).
    
ACLTABLE_FREEBUSY
  
> Задает новый правами.
    
frightsFreeBusyDetailed
  
> При передаче ACLTABLE_FREEBUSY предоставляет подробное отображение новые права сведениям о доступности.
    
frightsFreeBusySimple
  
> При передаче ACLTABLE_FREEBUSY предоставляет простого отображения новые права сведениям о доступности.
    
 _lppTable_
  
> [out] Указывает на [IMAPITable: IUnknown](imapitableiunknown.md) интерфейс, содержащий объект таблицы. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |Mfcmapi (en) использует метод **IExchangeModifyTable::GetTable** для получения таблицы правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

