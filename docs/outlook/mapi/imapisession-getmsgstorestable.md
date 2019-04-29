---
title: Имаписессионжетмсгсторестабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428139"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице хранилища сообщений, в которой содержатся сведения обо всех хранилищах сообщений в профиле сеанса.
  
```cpp
HRESULT GetMsgStoresTable(
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
  
> вышли Указатель на указатель на таблицу хранилища сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица была успешно возвращена.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен флаг МАПИ_УНИКОДЕ, а сеанс не поддерживает Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession:: жетмсгсторестабле** извлекает указатель на таблицу хранилища сообщений, таблицу, поддерживаемую MAPI, которая содержит сведения о каждом открытом хранилище сообщений в профиле. 
  
Полный список обязательных и необязательных столбцов в таблице хранилища сообщений представлен в статье [Message Store Tables](message-store-tables.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Так как MAPI обновляет таблицу хранилища сообщений во время сеанса, когда происходит изменение, вызовите метод **advise** таблицы хранилища сообщений, чтобы зарегистрировать уведомления об этих изменениях. Возможные изменения включают добавление новых хранилищ сообщений, удаление существующих хранилищ и изменения в хранилище по умолчанию. 
  
Установка флага МАПИ_УНИКОДЕ в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable:: куериколумнс](imapitable-querycolumns.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md) . Этот флаг также контролирует типы свойств в порядке сортировки, возвращаемом методом [IMAPITable:: куерисортордер](imapitable-querysortorder.md) . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Маиндлг. cpp  <br/> |Кмаиндлг:: Онопенмессажесторетабле  <br/> |MFCMAPI использует метод **IMAPISession:: жетмсгсторестабле** , чтобы получить таблицу хранилища сообщений, чтобы ее можно было отобразить в главном диалоговом окне MFCMAPI.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Таблицы хранилища сообщений](message-store-tables.md)

