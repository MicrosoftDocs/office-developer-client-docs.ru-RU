---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4cbaf08c58a98be45ad33aebb8f230fb53c234f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577662"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [ROWENTRY](rowentry.md) , представляющее строк и операции, выполняемые на соответствующие строки в таблице через интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Число записей в массива, указанного параметром члена **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Массив структур **ROWENTRY** , содержащий строки и операции, выполняемые на соответствующие строки в таблице. 
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Используются для формирования список выбранных правил для последующих действий **ModifyTable** .  <br/> |
   
## <a name="see-also"></a>См. также



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Структуры MAPI](mapi-structures.md)

