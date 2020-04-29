---
title: имапитаблежетстатус
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

 _лпултаблестатус_
  
> вышли Указатель на значение, указывающее состояние таблицы. Можно возвратить одно из следующих значений:
    
TBLSTAT_COMPLETE 
  
> Ни одна операция не выполняется.
    
TBLSTAT_QCHANGED 
  
> Содержимое таблицы изменилось с експектантли. Это значение состояния не возвращается для изменений, вызванных операциями сортировки или ограничения.
    
TBLSTAT_RESTRICT_ERROR 
  
> Произошла ошибка при выполнении операции [IMAPITable:: restrict](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> В процессе **IMAPITable:: выполняется операция restrict** . 
    
TBLSTAT_SETCOL_ERROR 
  
> Произошла ошибка при выполнении операции [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) . 
    
TBLSTAT_SETTING_COLS 
  
> Выполняется операция **IMAPITable:: метода SetColumns** . 
    
TBLSTAT_SORT_ERROR 
  
> Произошла ошибка при выполнении операции [IMAPITable:: сорттабле](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Выполняется операция **IMAPITable:: сорттабле** . 
    
 _лпултаблетипе_
  
> вышли Указатель на значение, указывающее тип таблицы. Можно вернуть один из следующих трех типов таблицы:
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы является динамическим; значения строк и столбцов могут изменяться при изменении базовых данных.
    
TBLTYPE_KEYSET 
  
> Строки в таблице фиксированы, но значения столбцов в этих строках являются динамическими и могут изменяться при изменении базовых данных.
    
TBLTYPE_SNAPSHOT 
  
> Таблица является статической, и ее содержимое не изменяется при изменении базовых данных.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Состояние таблицы было успешно возвращено.
    
## <a name="remarks"></a>Примечания

Метод **имаптабле::** не получает сведений о типе таблицы и текущем состоянии. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать методического **состояния** в сочетании с тремя другими методами **IMAPITable** для отслеживания состояния этих операций и определения их применения к таблице. Call с параметром "/ **состояние** " после выполнения одного из следующих вызовов **IMAPITable** : 
  
- [IMAPITable:: restrict](imapitable-restrict.md) to set Restriction. 
    
- [IMAPITable:: сорттабле](imapitable-sorttable.md) для установки порядка сортировки. 
    
- [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстаблелистктрл. cpp  <br/> |Кконтентстаблелистктрл::/Status  <br/> |MFCMAPI использует метод **IMAPITable::** , чтобы сообщить о состоянии таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

