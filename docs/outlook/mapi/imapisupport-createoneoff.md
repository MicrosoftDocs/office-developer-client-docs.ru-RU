---
title: имаписуппорткреатеонеофф
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
  
Создает идентификатор записи для одного адреса.
  
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

 _лпсзнаме_
  
> возврата Указатель на отображаемое имя получателя в свойстве **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Параметр _лпсзнаме_ может иметь значение null. 
    
 _лпсзадртипе_
  
> возврата Указатель на тип адреса (например, FAX, SMTP или X500) получателя. Параметр _лпсзадртипе_ не может иметь значение null. 
    
 _лпсзаддресс_
  
> возврата Указатель на адрес обмена сообщениями получателя. Параметр _лпсзаддресс_ не может иметь значение null. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, влияющих на одного получателя. Можно задать следующие флаги:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать форматированное содержимое сообщения. Если параметр MAPI_SEND_NO_RICH_INFO установлен, MAPI задает для свойства **PR_SEND_RICH_INFO** получателя ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) значение false. Если MAPI_SEND_NO_RICH_INFO не задано, MAPI задает для этого свойства значение TRUE, если адрес обмена сообщениями получателя, на который указывает _лпсзаддресс_ , не считается Интернет-адресом. В этом случае MAPI устанавливает **PR_SEND_RICH_INFO** в значение false. 
    
MAPI_UNICODE 
  
> Отображаемое имя, тип адреса и адрес имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, эти строки представлены в формате ANSI.
    
 _лпкбентрид_
  
> вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ . 
    
 _лппентрид_
  
> вышли Указатель на указатель на идентификатор записи для одноразового получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно создан идентификатор одноразовой записи.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: креатеонеофф** реализован для всех объектов поддержки поставщика услуг. Поставщики услуг вызывают **креатеонеофф** для создания идентификатора записи для одноразового получателя (получателя, не относящегося к какому-либо из контейнеров из загруженных в текущий момент поставщиков адресной книги). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

По завершении использования идентификатора записи, возвращенного функцией **креатеонеофф**, освободите память, выделенную для идентификатора записи, с помощью функции [мапифрибуффер](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Примечания для поставщиков транспорта

Поддерживает формат TNEF и используйте значение свойства **PR_SEND_RICH_INFO** , чтобы определить, следует ли использовать TNEF при передаче сообщения. Не поддерживает формат TNEF или не отправляется сообщение в этом формате при его запросе может быть проблемой для клиентов на основе форм или клиентов, которым требуются настраиваемые свойства MAPI. Это связано с тем, что TNEF обычно используется для отправки настраиваемых свойств настраиваемых классов сообщений. 
  
## <a name="see-also"></a>См. также



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Каноническое свойство PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

