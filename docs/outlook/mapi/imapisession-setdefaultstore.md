---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587847"
---
# <a name="imapisessionsetdefaultstore"></a>IMAPISession::SetDefaultStore

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для сеанса.
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который управляет параметром хранилище сообщений по умолчанию. Следующие флаги являются взаимоисключающими; можно задать только один из следующих флагов:
    
MAPI_DEFAULT_STORE
  
> Устанавливает хранилище сообщений по умолчанию сеанса. Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
MAPI_PRIMARY_STORE
  
> Устанавливает хранилище сообщений в качестве хранилища для использования при входе в систему. Если хранилище сообщений не хранилище по умолчанию, клиенты должны сделать по умолчанию. Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_PRIMARY_STORE в столбце **PR_RESOURCE_FLAGS** . 
    
MAPI_SECONDARY_STORE
  
> Устанавливает хранилище сообщений в качестве хранилища для использования при входе в систему, если хранилище основных сообщений не поддерживается. Если клиент не может открыть основного хранилища, его открытие дополнительного хранилища и сохранить его как значение по умолчанию. Обновляет строку в таблице состояния хранилища сообщений, установив флажок STATUS_SECONDARY_STORE в столбце **PR_RESOURCE_FLAGS** . 
    
MAPI_SIMPLE_STORE_PERMANENT
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилища сообщений, его состояние строки в таблице, строка таблицы хранилища сообщений, а в профиле сеанса. 
    
MAPI_SIMPLE_STORE_TEMPORARY
  
> Задает флаг STATUS_SIMPLE_STORE в свойстве **PR_RESOURCE_FLAGS** хранилище сообщений в строке в таблице состояния и строка таблицы хранилища сообщений. Профиль не изменяется. 
    
 _cbEntryID_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Указатель на идентификатор записи хранилища сообщений, предназначенного по умолчанию. Если клиент передает значение NULL в _lpEntryID_, без хранилища сообщений будет установлен по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::SetDefaultStore** устанавливает хранилища сообщений как один из следующих: 
  
- Хранилище сообщений по умолчанию для сеанса.
    
- Хранилище основных сообщений для сеанса.
    
- Хранилище дополнительного сообщения для сеанса.
    
Чтобы установить хранилище сообщений по умолчанию, хранилища сообщений необходимо иметь следующие флаги, задайте в своем свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
  
- STORE_SUBMIT_OK
    
- STORE_CREATE_OK
    
- STORE_MODIFY_OK
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно определить хранилище сообщений по умолчанию для сеанса, получение состояния и поиск состояние флага STATUS_DEFAULT_STORE в столбце **PR_RESOURCE_FLAGS** . Строку, которая содержит этот параметр представляет хранилища сообщений, которое используется в качестве сеанса по умолчанию. 
  
Если MAPI_DEFAULT_STORE или флаг MAPI_SIMPLE_STORE_PERMANENT, MAPI обновляет профилей, таблицы хранилища сообщений и состояния в таблице. 
  
При внесении изменений в хранилище сообщений по умолчанию, создаются следующие уведомления:
  
- Уведомление о событии **fnevTableModified** отправляется для каждой затронутых строки в обоих хранилища и состояние таблицы сообщений. 
    
- Внутренних уведомлений отправляется в очередь MAPI. Операции в уже начатую завершены без изменения; новые операций на хранилище сообщений по умолчанию, например загрузку сообщений обрабатываются для новое хранилище по умолчанию.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSetDefaultStore  <br/> |Mfcmapi (en) используется метод **IMAPISession::SetDefaultStore** для определения выбранного магазина как хранилище по умолчанию.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceFlags](pidtagresourceflags-canonical-property.md)
  
[Каноническое свойство PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

