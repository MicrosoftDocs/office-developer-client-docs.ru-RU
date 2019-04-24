---
title: Иексчанжемодифитаблежеттабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336619"
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

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Резервирования должен иметь значение 0 (ноль).
    
АКЛТАБЛЕ_ФРИБУСИ
  
> Задает новые права.
    
Фригхтсфрибусидетаилед
  
> Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете просмотреть подробные сведения о новых правах на сведения о доступности.
    
Фригхтсфрибусисимпле
  
> Когда АКЛТАБЛЕ_ФРИБУСИ передается, вы можете легко отобразить новые права на доступ к сведениям о доступности.
    
 _Лпптабле_
  
> вышли Указывает на [IMAPITable: интерфейс IUnknown](imapitableiunknown.md) , содержащий объект Table. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Рулесдлг. cpp  <br/> |Крулесдлг:: Онрефрешвиев  <br/> |MFCMAPI использует метод **иексчанжемодифитабле:: table** для получения таблицы правил.  <br/> |
   
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

