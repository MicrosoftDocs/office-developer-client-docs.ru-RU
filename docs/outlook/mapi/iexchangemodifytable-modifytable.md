---
title: Иексчанжемодифитаблемодифитабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350843"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обновляет объект таблицы MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Используйте одно из следующих значений: 
    
0 (ноль)
  
> Используйте значение члена **улровфлагс** структуры [ровентри](rowentry.md) . 
    
АКЛТАБЛЕ_ФРИБУСИ
  
> Задает новые права.
    
Фригхтсфрибусидетаилед
  
> Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете просмотреть подробные сведения о новых правах на сведения о доступности.
    
Фригхтсфрибусисимпле
  
> Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете легко отобразить новые права на доступ к сведениям о доступности.
    
РОВЛИСТ_РЕПЛАЦЕ
  
> Замените все строки в таблице.
    
 _Лпмодс_
  
> возврата Указывает на структуру [ровлист](rowlist.md) , содержащую свойства для объекта Table. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Рулесдлг. cpp  <br/> |Крулесдлг:: Онмодифиселектедитем  <br/> |MFCMAPI использует метод **иексчанжемодифитабле:: модифитабле** для записи измененного правила обратно в таблицу правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

