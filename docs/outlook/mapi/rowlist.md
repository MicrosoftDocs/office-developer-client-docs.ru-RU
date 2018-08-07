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
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812164"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Относится к**: Outlook 
  
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

