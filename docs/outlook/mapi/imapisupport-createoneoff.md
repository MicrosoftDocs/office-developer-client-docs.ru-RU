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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор записи для разовый адрес.
  
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
  
> [in] Указатель на отображаемого имени получателя, **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Параметр  _lpszName может_ иметь NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя. Параметр  _lpszAdrType не_ может иметь NULL. 
    
 _lpszAddress_
  
> [in] Указатель на адрес сообщения получателя. Параметр  _lpszAddress не_ может иметь NULL. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, влияемая на одного получателя. Можно установить следующие флаги:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать отформатированный контент сообщения. Если MAPI_SEND_NO_RICH_INFO задан, MAPI устанавливает для свойства **PR_SEND_RICH_INFO** получателя [(PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false. Если MAPI_SEND_NO_RICH_INFO не заданная, MAPI устанавливает для этого свойства true, если адрес получателя сообщений, на который указывает  _lpszAddress,_ не интерпретируется как адрес Интернета. В этом случае MAPI **PR_SEND_RICH_INFO** false. 
    
MAPI_UNICODE 
  
> Отображаемого имени, типа адреса и адреса в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на количество в идентификаторе записи, на которые указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для одного получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор однорахой записи успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::CreateOneOff** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг звонят **в CreateOneOff,** чтобы создать идентификатор записи для одного получателя (получателя, который не принадлежит ни одному из контейнеров ни от одного из текущих загруженных поставщиков адресной книги). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

После завершения использования идентификатора записи, возвращаемого **CreateOneOff,** освободите память, выделенную для идентификатора записи, с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="notes-to-transport-providers"></a>Примечания для поставщиков транспорта

Поддержка формата TNEF и использование значения свойства **PR_SEND_RICH_INFO,** чтобы определить, следует ли использовать формат TNEF при транспортировке сообщения. Не поддерживает формат TNEF или не отправляет сообщение в этом формате при запросе, может быть проблемой для клиентов на основе форм, которые требуют настраиваемые свойства MAPI. Это необходимо, поскольку TNEF обычно используется для отправки настраиваемой свойства для настраиваемой классы сообщений. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

