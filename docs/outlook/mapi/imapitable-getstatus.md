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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает состояние и тип таблицы.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Параметры

 _lpulTableStatus_
  
> [out] Указатель на значение, указывающее состояние таблицы. Может быть возвращено одно из следующих значений:
    
TBLSTAT_COMPLETE 
  
> Операции не находятся в процессе выполнения.
    
TBLSTAT_QCHANGED 
  
> Содержимое таблицы было значительно изменено. Это значение состояния не возвращается для изменений, которые являются результатом операций сортировки или ограничений.
    
TBLSTAT_RESTRICT_ERROR 
  
> Во время операции [IMAPITable::Restrict произошла](imapitable-restrict.md) ошибка. 
    
TBLSTAT_RESTRICTING 
  
> Идет **операция IMAPITable::Restrict.** 
    
TBLSTAT_SETCOL_ERROR 
  
> Во время операции [IMAPITable::SetColumns произошла](imapitable-setcolumns.md) ошибка. 
    
TBLSTAT_SETTING_COLS 
  
> Идет **операция IMAPITable::SetColumns.** 
    
TBLSTAT_SORT_ERROR 
  
> Во время операции [IMAPITable::SortTable произошла](imapitable-sorttable.md) ошибка. 
    
TBLSTAT_SORTING 
  
> Идет **операция IMAPITable::SortTable.** 
    
 _lpulTableType_
  
> [out] Указатель на значение, которое указывает тип таблицы. Может быть возвращен один из следующих трех типов таблиц:
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы является динамическим; значения строк и столбцов могут изменяться по мере изменения данных.
    
TBLTYPE_KEYSET 
  
> Строки в таблице являются фиксированными, но значения столбцов в этих строках являются динамическими и могут изменяться по мере изменения данных.
    
TBLTYPE_SNAPSHOT 
  
> Таблица является статической, и ее содержимое не меняется при изменении данных.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние таблицы было успешно возвращено.
    
## <a name="remarks"></a>Примечания

Метод **IMAPTable::GetStatus** извлекает сведения о типе таблицы и текущем состоянии. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

**GetStatus** можно использовать в сочетании с тремя другими методами **IMAPITable** для отслеживания состояния этих операций и определения влияния на таблицу. Вызовите **GetStatus** после одного из следующих вызовов **IMAPITable:** 
  
- [IMAPITable::Restrict](imapitable-restrict.md) to set a restriction. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) для создания порядка сортировки. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI использует метод **IMAPITable::GetStatus** для отчета о состоянии таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

