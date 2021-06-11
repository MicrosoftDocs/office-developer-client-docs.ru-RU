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
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411997"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор записи для разового адреса.
  
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

## <a name="parameters"></a>Parameters

 _lpszName_
  
> [in] Указатель на имя отображения получателя **свойства PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Параметр  _lpszName может_ быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя. Параметр  _lpszAdrType_ не может быть NULL. 
    
 _lpszAddress_
  
> [in] Указатель на адрес сообщения получателя. Параметр  _lpszAddress не_ может быть NULL. 
    
 _ulFlags_
  
> [in] Битмашка флагов, которая влияет на разовую получатель. Можно установить следующие флаги:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать отформатированный контент сообщения. Если MAPI_SEND_NO_RICH_INFO установлено, MAPI задает свойство  [PR_SEND_RICH_INFO (PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false. Если MAPI_SEND_NO_RICH_INFO не установлено, MAPI задает это свойство true, если адрес обмена сообщениями получателя, на который указывает  _lpszAddress,_ не интерпретируется как интернет-адрес. В этом случае MAPI задает **PR_SEND_RICH_INFO** false. 
    
MAPI_UNICODE 
  
> Имя отображения, тип адреса и адрес находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpcbEntryID_
  
> [вышел] Указатель на количество bytes в идентификаторе записи, указываемом _параметром lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор записи для разового получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор одноавтной записи был успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CreateOneOff** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг звонят **в CreateOneOff** для создания идентификатора входа для разового получателя (получателя, который не принадлежит ни одному из контейнеров от любого из загруженных поставщиков адресных книг). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После завершения использования идентификатора записи, возвращенного **CreateOneOff,** освободите память, выделенную для идентификатора записи, с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="notes-to-transport-providers"></a>Заметки поставщикам транспорта

Поддержка формата транспортной нейтральной инкапсуляции (TNEF) и использование значения свойства PR_SEND_RICH_INFO, чтобы определить, следует ли использовать TNEF при транспортировке сообщения.  Не поддержка TNEF или не отправка сообщения в этом формате при запросе может быть проблемой для клиентов или клиентов на основе форм, которые требуют настраиваемые свойства MAPI. Это потому, что TNEF обычно используется для отправки пользовательских свойств для настраиваемых классов сообщений. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

