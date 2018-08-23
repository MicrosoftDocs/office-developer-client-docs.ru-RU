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
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571152"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает состояние в таблице и тип.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Параметры

 _lpulTableStatus_
  
> [out] Указатель на значение, указывающее состояние таблицы. Можно получить одно из следующих значений:
    
TBLSTAT_COMPLETE 
  
> Нет операций находятся в процессе выполнения.
    
TBLSTAT_QCHANGED 
  
> Содержимое таблицы expectantly были изменены. Это значение состояния для изменения, в результате операций сортировки или ограничения не возвращается.
    
TBLSTAT_RESTRICT_ERROR 
  
> Произошла ошибка во время операции [IMAPITable::Restrict](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> Операция **IMAPITable::Restrict** — в стадии разработки. 
    
TBLSTAT_SETCOL_ERROR 
  
> Произошла ошибка во время операции [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
TBLSTAT_SETTING_COLS 
  
> Операция **IMAPITable::SetColumns** — в стадии разработки. 
    
TBLSTAT_SORT_ERROR 
  
> Произошла ошибка во время операции [IMAPITable::SortTable](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Операция **IMAPITable::SortTable** — в стадии разработки. 
    
 _lpulTableType_
  
> [out] Указатель на значение, которое указывает тип таблицы. Можно получить одно из следующих типов три таблицы:
    
TBLTYPE_DYNAMIC 
  
> Содержимое таблицы динамических; строки и столбцы можно изменить при изменении базовых данных.
    
TBLTYPE_KEYSET 
  
> Исправленные строки в таблице, но значения столбцов в следующих строках динамических и можно изменить при изменении базовых данных.
    
TBLTYPE_SNAPSHOT 
  
> В таблице является статическим, и его содержимое не изменяются при изменении базовых данных.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Состояние таблицы успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPTable::GetStatus** получает сведения о типе и текущее состояние таблицы. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Совместно с тремя другие методы **IMAPITable** **GetStatus** можно использовать для отслеживания состояния выполнения этих операций и определить влияние на таблицу. Вызовите **GetStatus** после внесения одного из следующих **IMAPITable** вызовов: 
  
- Чтобы задать ограничение [IMAPITable::Restrict](imapitable-restrict.md) . 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) , чтобы установить порядок сортировки. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) для определения набора столбцов. 
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |Mfcmapi (en) использует метод **IMAPITable::GetStatus** для отчет о состоянии таблицы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

