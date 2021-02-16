---
title: Каноническое свойство PidTagSenderSmtpAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 321cde5a-05db-498b-a9b8-cb54c8a14e34
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c39fce40fb508370e62cb8b38123fa6ccc0e7d7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342632"
---
# <a name="pidtagsendersmtpaddress-canonical-property"></a>Каноническое свойство PidTagSenderSmtpAddress

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит формат SMTP-адреса электронной почты владельца отправляемого почтового ящика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENDER_SMTP_ADDRESS, PR_SENDER_SMTP_ADDRESS_A, PR_SENDER_SMTP_ADDRESS_W  <br/> |
|Идентификатор:  <br/> |0x5D01  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является примером свойств адреса для отправитель сообщения. Его должен установить исходяющий поставщик транспорта, который никогда не должен распространять ранее существующие значения.
  
Если ни один поставщик транспорта не предоставил никаких свойств адреса отправитель, пульдер MAPI пытается заполнить их, вызывая метод [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора записи. Если идентификаторы записей не указаны, то пульщик MAPI сохраняет "Unknown" во всех свойствах адреса отправитель типа PT_UNICODE или PT_STRING8. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Microsoft Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов post.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

