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
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436246"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на интерфейс для объекта таблицы MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Зарезервировано; должно быть 0 (ноль).
    
ACLTABLE_FREEBUSY
  
> Задает новые права.
    
frightsFreeBusyDetailed
  
> При ACLTABLE_FREEBUSY предоставляет подробные сведения о новых правах на сведения о занятости.
    
frightsFreeBusySimple
  
> При ACLTABLE_FREEBUSY данные отображаются новые права занятости.
    
 _lppTable_
  
> [out] Указывает на [интерфейс IMAPITable : IUnknown,](imapitableiunknown.md) содержащий объект таблицы. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI использует метод **IExchangeModifyTable::GetTable** для получения таблицы правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

