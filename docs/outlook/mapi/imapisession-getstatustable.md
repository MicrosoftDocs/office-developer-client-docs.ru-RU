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
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407139"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице состояния, которая содержит сведения обо всех ресурсах MAPI в сеансе.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая определяет формат столбцов, которые являются строками символов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки столбцов в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки столбцов имеют формат ANSI.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу состояния.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::GetStatusTable** предоставляет доступ к таблице состояния, которая содержит сведения обо всех ресурсах MAPI в сеансе. В таблице есть одна строка для сведений о подсистеме MAPI, одна строка для пула MAPI, одна строка для интегрированной адресной книги и одна строка для каждого поставщика услуг в профиле. 
  
Полный список необходимых и необязательных столбцов в таблице состояния см. в [таблицах состояния.](status-tables.md) 
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI использует метод **IMAPISession::GetStatusTable** для получения отрисовки таблицы состояния.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Таблицы состояния](status-tables.md)

