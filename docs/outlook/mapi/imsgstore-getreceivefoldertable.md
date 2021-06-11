---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421356"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к таблице приемных папок, которая содержит сведения обо всех папках получения для магазина сообщений.
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют доступ к таблице. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **GetReceiveFolderTable** успешно вернуться, возможно, до того, как таблица будет полностью доступна вызываемой. Если таблица недоступна полностью, последующий вызов таблицы может привести к ошибке. 
    
MAPI_UNICODE 
  
> Возвращенные строки находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу папки получения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица папки получения успешно возвращена.
    
## <a name="remarks"></a>Примечания

Метод **IMsgStore::GetReceiveFolderTable** предоставляет доступ к таблице, в которую показаны параметры свойств для всех папок в хранилище сообщений. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Список необходимых столбцов в таблице папки получения см. в [статье Получение таблиц папок.](receive-folder-tables.md) 
  
Реализуйте таблицы папки получения для поддержки установки ограничений свойств **для свойства PR_RECORD_KEY** [(PidTagRecordKey).](pidtagrecordkey-canonical-property.md) Это позволяет легко получить доступ к определенным папкам получения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Установка флага MAPI_UNICODE в параметре _ulFlags_ влияет на формат столбцов, возвращаемых из методов [IMAPITable::QueryColumns](imapitable-querycolumns.md) и [IMAPITable::QueryRows.](imapitable-queryrows.md) Этот флаг также управляет типами свойств в порядке сортировки, возвращаемом методом [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI использует **метод IMsgStore::GetReceiveFolderTable** для отображения таблицы папки получения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

