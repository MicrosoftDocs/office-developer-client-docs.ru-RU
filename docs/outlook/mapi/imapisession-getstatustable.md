---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 48a69fa49735014dcbfffad0673f1d4da62452e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594833"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице состояния, таблицу, содержащую сведения обо всех ресурсах MAPI в сеансе.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет формат для столбцов, которые являются строками символов. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строку, в формате Юникод. Если флаг MAPI_UNICODE не установлен, столбцы строку, в формате ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель в таблице состояния.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Таблица успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::GetStatusTable** предоставляет доступ к таблице состояния, который содержит сведения обо всех ресурсах MAPI в сеансе. Существует одна строка в таблице сведения о подсистемы MAPI, одна строка для очереди MAPI, одна строка для встроенной адресной книги и одной строке для каждого поставщика служб в профиле. 
  
Полный список обязательные и дополнительные столбцы в таблице состояния видеть [Состояние таблицы](status-tables.md). 
  
Установка флага MAPI_UNICODE с помощью параметра _ulFlags_ влияет на формат столбцов, возвращаемых с помощью методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows](imapitable-queryrows.md) . Этот флаг также определяет типы свойств в порядке сортировки, возвращенный методом [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |Mfcmapi (en) использует метод **IMAPISession::GetStatusTable** для получения состояния таблицы для отображения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Таблицы состояния](status-tables.md)

