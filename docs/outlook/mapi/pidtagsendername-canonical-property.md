---
title: Каноническое свойство PidTagSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355071"
---
# <a name="pidtagsendername-canonical-property"></a>Каноническое свойство PidTagSenderName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемую именем отправитель сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W  <br/> |
|Идентификатор:  <br/> |0x0C1A  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Адрес  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств адресов отправщика сообщений. Он должен быть задат исходячим поставщиком транспорта, который никогда не должен распространять какие-либо ранее существующие значения.
  
Если ни один поставщик транспорта не предоставил никаких свойств адресов отправитель, пуллер MAPI пытается заполнить их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) для идентификатора входа. Если идентификаторы записей не предоставлены, пульпер MAPI сохраняет "Unknown" во всех свойствах адресов отправителей типа PT_TSTRING. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Описывает формат сообщений, используемых для отправки сведений, связанных с совместной папкой клиента.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые представляют элементы RSS.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для почтовых объектов.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для контактов и личных списков рассылки.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

