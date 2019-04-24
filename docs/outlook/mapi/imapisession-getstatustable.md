---
title: Имаписессионжетстатустабле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338764"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице Status (таблица), в которой содержатся сведения обо всех ресурсах MAPI в сеансе.
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих формат столбцов, которые являются символьными строками. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строковые столбцы представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строковые столбцы представлены в формате ANSI.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу состояния.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица была успешно возвращена.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPISession:: жетстатустабле** предоставляет доступ к таблице состояния, которая содержит сведения обо всех ресурсах MAPI в сеансе. В таблице есть одна строка для сведений о подсистеме MAPI, одна строка для диспетчера очереди MAPI, одна строка для встроенной адресной книги и одна строка для каждого поставщика услуг в профиле. 
  
Полный список обязательных и необязательных столбцов в таблице состояние представлен в статье [Status Tables](status-tables.md). 
  
Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) . Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онстатустабле  <br/> |MFCMAPI использует метод **IMAPISession:: жетстатустабле** , чтобы получить таблицу состояния для отображения.  <br/> |
   
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

