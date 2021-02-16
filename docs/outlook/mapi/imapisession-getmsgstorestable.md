---
title: IMAPISessionGetMsgStoresTable
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
  
Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.
  
```cpp
HRESULT GetMsgStoresTable(
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
  
> [out] Указатель на указатель на таблицу хранения сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица успешно возвращена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Флаг MAPI_UNICODE установлен, а сеанс не поддерживает Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::GetMsgStoresTable** извлекает указатель на таблицу хранения сообщений, таблицу, поддерживаемую MAPI, которая содержит сведения о каждом открытом хранилище сообщений в профиле. 
  
Полный список необходимых и необязательных столбцов в таблице хранения сообщений см. в [таблицах магазина сообщений.](message-store-tables.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Так как MAPI обновляет таблицу хранения сообщений во время сеанса при внесении изменений, вызовите метод **Advise** таблицы магазина сообщений, чтобы получить уведомление об этих изменениях. Возможные изменения включают добавление новых хранилищ сообщений, удаление существующих хранилищ и изменение хранилища по умолчанию. 
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых методами [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI использует метод **IMAPISession::GetMsgStoresTable** для получения таблицы хранения сообщений, чтобы ее можно было отрисовки в главном диалоговом окне MFCMAPI.  <br/> |
   
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
  
[Таблицы для хранения сообщений](message-store-tables.md)

