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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на таблицу содержимого контейнера.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет возвратом таблицы содержимого. Можно установить следующие флаги:
    
MAPI_ASSOCIATED 
  
> Связанную с контейнером таблицу содержимого следует возвращать вместо стандартной таблицы содержимого. Этот флаг используется только с папками. Сообщения, включенные в связанную таблицу содержимого, были созданы с флагом MAPI_ASSOCIATED, установленным в вызове метода [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) Клиенты обычно используют связанную таблицу содержимого для получения форм, представлений и других скрытых сообщений. 
    
ACLTABLE_FREEBUSY
  
> Включает доступ к правам frightsFreeBusySimple и frightsFreeBusyDetailed в **PR_MEMBER_RIGHTS.**
    
MAPI_DEFERRED_ERRORS 
  
> **GetContentsTable** может успешно вернуться, возможно, до того, как таблица будет доступна вызываемой. Если таблица недоступна, последующий вызов таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Запрашивает, чтобы столбцы, содержащие строку данных, возвращались в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Отображает элементы, которые в настоящее время помечены как "мягкие", то есть находятся на этапе хранения удаленных элементов.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу содержимого.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица содержимого успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер не имеет содержимого и не может предоставить таблицу содержимого.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetContentsTable** возвращает указатель на таблицу содержимого контейнера. В таблице содержимого содержится сводная информация об объектах в контейнере. 
  
Таблицы содержимого имеют длинные наборы столбцов. Полный список необходимых и необязательных столбцов в таблицах содержимого см. в [таблицах содержимого.](contents-tables.md) 
  
Некоторые контейнеры могут не иметь содержимого. Эти контейнеры MAPI_E_NO_SUPPORT из своих реализаций **GetContentsTable.**
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу содержимого для контейнера, необходимо также сделать следующее:
  
- Поддержка вызовов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия **свойства PR_CONTAINER_CONTENTS** ([PidTagContainerContents).](pidtagcontainercontents-canonical-property.md)
    
- Возврат **PR_CONTAINER_CONTENTS** в ответ на вызов контейнера 
    
    [Методы IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
    
Реализация этого метода удаленным поставщиком транспорта должна возвращать указатель на [интерфейс IMAPITable : IUnknown](imapitableiunknown.md) в параметре _ppTable,_ переданном в метод **GetContentsTable.** Если ваш поставщик транспорта имеет существующую таблицу содержимого, достаточно вернуть на нее указатель. В этом случае этот метод должен создать новый объект [IMAPITable : IUnknown,](imapitableiunknown.md) заполнить таблицу заголовщиками сообщений (если таковые имеются) и вернуть указатель на новую таблицу. Метод [ITableData::HrGetView](itabledata-hrgetview.md) полезен для создания возвращаемого значения и хранения указателя таблицы в параметре _ppTable._ Таблица содержимого должна поддерживать по крайней мере следующие столбцы свойств: 
  
- **PR_ENTRYID** ([PidTagEntryID)](pidtagentryid-canonical-property.md)
    
- **PR_SENDER_NAME** ([PidTagSenderName)](pidtagsendername-canonical-property.md)
    
- **PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **PR_DISPLAY_TO** ([PidTagDisplayTo)](pidtagdisplayto-canonical-property.md)
    
- **PR_SUBJECT** ([PidTagSubject)](pidtagsubject-canonical-property.md)
    
- **PR_MESSAGE_CLASS** ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)
    
- **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)
    
- **PR_MESSAGE_SIZE** ([PidTagMessageSize)](pidtagmessagesize-canonical-property.md)
    
- **PR_PRIORITY** ([PidTagPriority)](pidtagpriority-canonical-property.md)
    
- **PR_IMPORTANCE** ([PidTagImportance)](pidtagimportance-canonical-property.md)
    
- **PR_SENSITIVITY** ([PidTagSensitivity)](pidtagsensitivity-canonical-property.md)
    
- **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime)](pidtagmessagedeliverytime-canonical-property.md)
    
- **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime)](pidtagmessagedownloadtime-canonical-property.md)
    
- **PR_HASATTACH** ([PidTagHasAttachments)](pidtaghasattachments-canonical-property.md)
    
- **PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    
- **PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)
    
- **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Строки и столбцы таблицы двоичного содержимого можно усечены. Обычно поставщики возвращают 255 символов. Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes. При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно из объекта, используя идентификатор записи, чтобы открыть его, а затем вызывать метод **IMAPIProp::GetProps.** 
  
В зависимости от реализации поставщика ограничения и операции сортировки могут применяться во всех строках или к усеченной версии этой строки.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|ContentsTableDialog.cpp  <br/> |CContentsTableDlg::CContentsTableDlg  <br/> |Класс **CContentsTableDlg** использует **GetContentsTable** для получения записей в таблице содержимого.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

