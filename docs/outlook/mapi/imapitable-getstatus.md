---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434335"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает состояние и тип таблицы.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Parameters

 _lpulTableStatus_
  
> [вышел] Указатель на значение, указывающее состояние таблицы. Одно из следующих значений можно вернуть:
    
TBLSTAT_COMPLETE 
  
> Нет операций в процессе.
    
TBLSTAT_QCHANGED 
  
> Содержимое таблицы значительно изменилось. Это значение состояния не возвращается для изменений, которые происходят в результате операций сортировки или ограничения.
    
TBLSTAT_RESTRICT_ERROR 
  
> Ошибка произошла во время [операции IMAPITable::Restrict.](imapitable-restrict.md) 
    
TBLSTAT_RESTRICTING 
  
> Операция **IMAPITable::Restrict** продолжается. 
    
TBLSTAT_SETCOL_ERROR 
  
> Ошибка произошла во время [операции IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
TBLSTAT_SETTING_COLS 
  
> Операция **IMAPITable::SetColumns** продолжается. 
    
TBLSTAT_SORT_ERROR 
  
> Ошибка произошла во время [операции IMAPITable::SortTable.](imapitable-sorttable.md) 
    
TBLSTAT_SORTING 
  
> Операция **IMAPITable::SortTable** продолжается. 
    
 _lpulTableType_
  
> [вышел] Указатель на значение, которое указывает тип таблицы. Один из следующих трех типов таблицы можно вернуть:
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы динамическое; значения строк и столбцов могут изменяться по мере изменения данных.
    
TBLTYPE_KEYSET 
  
> Строки в таблице фиксируются, но значения столбцов в этих строках динамически и могут изменяться по мере изменения данных.
    
TBLTYPE_SNAPSHOT 
  
> Таблица статична, и ее содержимое не меняется при изменении данных.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние таблицы было успешно возвращено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPTable::GetStatus** извлекает сведения о типе таблицы и текущем состоянии. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать **GetStatus** совместно с тремя другими методами **IMAPITable** для мониторинга состояния этих операций и определения эффекта на таблице. Вызов **GetStatus** после одного из следующих вызовов **IMAPITable:** 
  
- [IMAPITable:::Restrict](imapitable-restrict.md) to set a restriction. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) для создания порядка сортировки. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI использует **метод IMAPITable::GetStatus** для отчета о состоянии таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

