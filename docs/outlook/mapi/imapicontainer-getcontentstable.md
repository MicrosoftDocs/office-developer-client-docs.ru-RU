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
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431108"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель в таблицу содержимого контейнера.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которая управляет тем, как возвращается таблица контента. Можно установить следующие флаги:
    
MAPI_ASSOCIATED 
  
> Связанная таблица содержимого контейнера должна быть возвращена вместо стандартной таблицы содержимого. Этот флаг используется только в папках. Сообщения, включенные в связанную таблицу содержимого, были созданы с флагом MAPI_ASSOCIATED в вызове метода [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Обычно клиенты используют связанную таблицу контента для получения форм, представлений и других скрытых сообщений. 
    
ACLTABLE_FREEBUSY
  
> Включает доступ к правам frightsFreeBusySimple и frightsFreeBusyDetailed **в PR_MEMBER_RIGHTS.**
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** может успешно вернуться, возможно, до того, как таблица будет доступна вызываемой. Если таблица недоступна, при последующем вызове таблицы может быть допущена ошибка. 
    
MAPI_UNICODE 
  
> Запрашивает, чтобы столбцы, содержащие данные строки, возвращались в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Показывает элементы, которые в настоящее время помечены как мягкие удаленные, то есть они находятся на этапе времени хранения удаленных элементов.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу содержимого.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица содержимого была успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер не имеет содержимого и не может предоставить таблицу содержимого.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetContentsTable** возвращает указатель в таблицу содержимого контейнера. В таблице содержимого содержатся сводные сведения о объектах в контейнере. 
  
Таблицы контента имеют длительные наборы столбцов. Полный список необходимых и необязательных столбцов в таблицах контента см. в [статье Contents Tables.](contents-tables.md) 
  
Некоторые контейнеры могут не иметь содержимого. Эти контейнеры возвращают MAPI_E_NO_SUPPORT из реализации **GetContentsTable.**
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу контента для контейнера, необходимо также сделать следующее:
  
- Поддержка вызовов для метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия **свойства** [PR_CONTAINER_CONTENTS (PidTagContainerContents).](pidtagcontainercontents-canonical-property.md)
    
- Возвращение **PR_CONTAINER_CONTENTS** в ответ на вызов контейнера 
    
    [Методы IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
Реализация этого метода удаленным поставщиком транспорта должна вернуть указатель в [интерфейс IMAPITable : IUnknown](imapitableiunknown.md) в параметре _ppTable,_ переданном в **метод GetContentsTable.** Если у поставщика транспорта есть существующая таблица содержимого, достаточно вернуть указатель к ней. Если нет, этот метод должен создать новый [объект IMAPITable : IUnknown,](imapitableiunknown.md) заполнить таблицу заголовщиками сообщений (если таковые имеются) и вернуть указатель в новую таблицу. Метод [ITableData::HrGetView](itabledata-hrgetview.md) полезен для создания возвращаемого значения и хранения указателя таблицы в параметре _ppTable._ Таблица контента должна поддерживать по крайней мере следующие столбцы свойств: 
  
- **PR_ENTRYID** [(PidTagEntryID)](pidtagentryid-canonical-property.md)
    
- **PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)
    
- **PR_SENT_REPRESENTING_NAME** [(PidTagSentRepresentingName)](pidtagsentrepresentingname-canonical-property.md)
    
- **PR_DISPLAY_TO** [(PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)
    
- **PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)
    
- **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)
    
- **PR_MESSAGE_FLAGS** [(PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)
    
- **PR_MESSAGE_SIZE** [(PidTagMessageSize)](pidtagmessagesize-canonical-property.md)
    
- **PR_PRIORITY** [(PidTagPriority)](pidtagpriority-canonical-property.md)
    
- **PR_IMPORTANCE** [(PidTagImportance)](pidtagimportance-canonical-property.md)
    
- **PR_SENSITIVITY** [(PidTagSensitivity)](pidtagsensitivity-canonical-property.md)
    
- **PR_MESSAGE_DELIVERY_TIME** [(PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)
    
- **PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)
    
- **PR_MESSAGE_DOWNLOAD_TIME** [(PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)
    
- **PR_HASATTACH** [(PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)
    
- **PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    
- **PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
    
- **PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Столбцы таблицы строк и двоичного содержимого можно усечено. Обычно поставщики возвращают 255 символов. Поскольку вы не можете заранее узнать, включает ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes. При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно с объекта с помощью его идентификатора входа, чтобы открыть его, а затем позвонить по методу **IMAPIProp::GetProps.** 
  
В зависимости от реализации поставщика ограничения и операции сортировки могут применяться к всем строкам или к усеченной версии этой строки.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |Класс **CContentsTableDlg** использует **GetContentsTable** для получения записей в таблице контента.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

