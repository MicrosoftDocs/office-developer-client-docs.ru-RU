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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, определяемая форматом столбцов, которые являются строками символов. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Столбцы строк находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, столбцы строк находятся в формате ANSI.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблице хранения сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица успешно возвращена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Флаг MAPI_UNICODE и сеанс не поддерживает Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::GetMsgStoresTable** извлекает указатель на таблицу хранения сообщений, таблицу, поддерживаемую MAPI, которая содержит сведения о каждом хранилище открытых сообщений в профиле. 
  
Полный список необходимых и необязательных столбцов в таблице хранения сообщений см. в статье [Таблицы хранения сообщений.](message-store-tables.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Поскольку MAPI обновляет таблицу хранения сообщений во время  сеанса при всех изменениях, вызывайте метод Advise таблицы хранения сообщений для регистрации, чтобы получить уведомление об этих изменениях. Возможные изменения включают добавление новых магазинов сообщений, удаление существующих магазинов и изменения в хранилище по умолчанию. 
  
Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI использует метод **IMAPISession::GetMsgStoresTable** для получения таблицы хранения сообщений, чтобы она была отрисовка в главном диалоговом окне MFCMAPI.  <br/> |
   
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
  
[Таблицы магазина сообщений](message-store-tables.md)

