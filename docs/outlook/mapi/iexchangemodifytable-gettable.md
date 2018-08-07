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
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808819"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Относится к**: Outlook 
  
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
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |Mfcmapi (en) использует метод **IExchangeModifyTable::GetTable** для получения таблицы правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

