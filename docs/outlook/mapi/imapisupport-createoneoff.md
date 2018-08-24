---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594945"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает запись идентификатор указывает адрес.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpszName_
  
> [in] Указатель на отображаемое имя получателя, свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Параметр _lpszName_ может быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя. Параметр _lpszAdrType_ не может быть NULL. 
    
 _lpszAddress_
  
> [in] Указатель на обмена сообщениями адрес получателя. Параметр _lpszAddress_ не может быть NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, влияющей на одноразовых получателя. Можно задать следующие флажки:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать сообщения Форматированный контент. Если значение MAPI_SEND_NO_RICH_INFO, MAPI свойству получателя **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) присваивается значение FALSE. Если MAPI_SEND_NO_RICH_INFO не задано, MAPI этому свойству значение TRUE, если адрес получателя обмена мгновенными сообщениями, на который указывает _lpszAddress_ интерпретируется быть адрес в Интернете. В этом случае MAPI задает **PR_SEND_RICH_INFO** значение FALSE. 
    
MAPI_UNICODE 
  
> Отображаемое имя, тип адреса и адрес находятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на число байт в идентификаторе запись указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для одноразовых получателя.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор единичных записей успешно создан.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::CreateOneOff** применяется для всех объектов поддержки поставщика службы. Поставщики услуг вызова **CreateOneOff** для создания записи идентификатора для одноразовых получателя (получателя, не принадлежащие ни контейнеры из любого из поставщиками в настоящее время загрузки адресной книги). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При завершении с помощью идентификатора записи, возвращаемых **CreateOneOff**освободите память, выделенная для идентификатор записи с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Примечания для поставщиками транспорта

Поддержку транспорта Neutral Encapsulation формата TNEF и использовать значение свойства **PR_SEND_RICH_INFO** для определения необходимости использовать TNEF при передачи сообщения. Не поддерживает формат TNEF или не отправлять сообщения в формате запросу может вызвать проблемы для клиентов на основе форм или клиентов, которым требуется настраиваемых свойств MAPI. Это, так как TNEF обычно используется для отправки настраиваемых свойств для пользовательских классов сообщений. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

