---
title: IMAPIContainerGetContentsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9fb8919287420038b5c9165bb14b7d33d1ad2fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578866"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на таблицу содержимого контейнера.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как возвращается в таблице содержимое. Можно задать следующие флажки:
    
MAPI_ASSOCIATED 
  
> Таблица связанного содержимого контейнера должны быть возвращены вместо стандартного содержимое таблицы. Этот флаг используется только для папок. Сообщения, которые включены в таблицу связанного содержимого были созданы с флагом MAPI_ASSOCIATED, задайте в вызове метода [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . Клиенты обычно используется в таблице связанное содержимое для получения форм, представлений и другие скрытые сообщения. 
    
ACLTABLE_FREEBUSY
  
> Обеспечивает доступ к frightsFreeBusySimple и frightsFreeBusyDetailed правами в **PR_MEMBER_RIGHTS**.
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** может вернуть успешно, возможно перед таблице можно сделать доступной для вызывающего абонента. Если в таблице не поддерживается, вызов последующие таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Запросы, которые столбцы, которые содержат строковые данные возвращаются в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Отображает элементы, которые в настоящее время помечены как программных удалены, то есть, они находятся в хранения удаленных элементов этап времени.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу содержимого.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В таблице содержимое был успешно извлечен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер не имеет содержимого и не могут предоставить таблицу содержимого.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIContainer::GetContentsTable** возвращает указатель на таблицу содержимого контейнера. Содержимое таблицы содержит сводную информацию о объектов в контейнере. 
  
Содержимое таблицы имеют наборов длительным столбца. Полный список обязательные и дополнительные столбцы в таблицах содержимое [Содержимое](contents-tables.md)см. 
  
Существует возможность для некоторых контейнеров для без содержимого. Эти контейнеры возврата MAPI_E_NO_SUPPORT из их реализации **GetContentsTable**.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу содержимого для контейнера, необходимо выполнить следующее:
  
- Поддерживает вызовы метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия свойство **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Возвращает **PR_CONTAINER_CONTENTS** в ответ на звонок в контейнер 
    
    Методы [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
    
Реализация поставщика транспорта удаленного этот метод должен возвращать указатель [IMAPITable: IUnknown](imapitableiunknown.md) интерфейса с помощью параметра _ppTable_ , передаваемый в метод **GetContentsTable** . Если ваш поставщик транспорта существующей таблицы содержимое, достаточно возвращает указатель на него. Если не, этот метод должен создать новый [IMAPITable: IUnknown](imapitableiunknown.md) объекта, заполните таблицу с заголовками сообщения (если они доступны) и возвращает указатель для новой таблицы. Метод [ITableData::HrGetView](itabledata-hrgetview.md) может использоваться для создания возвращаемого значения и хранения указатель таблицы с помощью параметра _ppTable_ . В таблице содержимого должна поддерживать по крайней мере следующие столбцы свойств: 
  
- **PR_ENTRYID** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Строка и двоичный столбцов таблицы содержимое может быть усечен. Как правило поставщики возвращать 255 символов. Так как не известно, заранее ли таблицы включает в себя усеченных столбцы, предполагается, что столбец усекается, если длина столбца — 255 или 510 байт. Всегда можно будет извлечь полное значение усеченных столбца, при необходимости непосредственно из объекта с помощью его идентификатор записи чтобы его открыть, затем вызвать метод **IMAPIProp::GetProps** . 
  
В зависимости от реализации поставщика, ограничения и операции сортировки можно применять ко всем строки или усеченных версии этой строки.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |Класс **CContentsTableDlg** **GetContentsTable** используется для получения записей в таблицу.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

