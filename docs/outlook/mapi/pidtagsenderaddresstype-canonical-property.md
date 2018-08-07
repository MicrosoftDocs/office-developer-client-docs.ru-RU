---
title: Каноническое свойство PidTagSenderAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderAddressType
api_type:
- COM
ms.assetid: ad7f49ac-6fe8-4037-90f3-8dabd5648bed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5ff45bb8ae8fa011a8a46e7438dc73bab5649750
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811881"
---
# <a name="pidtagsenderaddresstype-canonical-property"></a>Каноническое свойство PidTagSenderAddressType

  
  
**Относится к**: Outlook 
  
Содержит тип адреса электронной почты отправителя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENDER_ADDRTYPE, PR_SENDER_ADDRTYPE_A, PR_SENDER_ADDRTYPE_W  <br/> |
|Идентификатор:  <br/> |0x0C1E  <br/> |
|Тип данных:  <br/> |PT_UNICODE PT_STRING8  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойства адреса отправителя сообщения. Он должен иметь значение исходящей поставщика транспорта, никогда не следует передать все ранее существующие значения.
  
Если отсутствует транспорт не предоставил любые свойства адрес отправителя, диспетчер очереди MAPI пытается заполните их путем вызова метода [IMAPISession::QueryIdentity](imapisession-queryidentity.md) на идентификатор записи. Если этот параметр указан без идентификаторы записей диспетчер очереди MAPI сохраняет «Неизвестно» в все свойства адреса отправителя типа PT_TSTRING. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Указывает, что свойства и операции, допустимые для учета объекты.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов списка рассылки и контактов.
    
[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

