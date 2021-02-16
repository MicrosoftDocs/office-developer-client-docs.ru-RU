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
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419186"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит массив структур [ROWENTRY,](rowentry.md) представляющих строки, и операции, выполняемые с этими строками в таблице с помощью интерфейса [IExchangeModifyTable.](iexchangemodifytableiunknown.md) 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>"Участники"

 **cEntries**
  
> Количество записей в массиве, указанном членом **aEntries.** 
    
 **aEntries[MAPI_DIM]**
  
> Массив структур **ROWENTRY,** содержащий строки и операции, выполняемые с этими строками в таблице. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Используется для создания списка выбранных правил для последующих действий **ModifyTable.**  <br/> |
   
## <a name="see-also"></a>См. также



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Структуры MAPI](mapi-structures.md)

