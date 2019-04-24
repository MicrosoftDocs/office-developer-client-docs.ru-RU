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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит формат SMTP-адреса электронной почты владельца почтового ящика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕНДЕР_СМТП_АДДРЕСС, ПР_СЕНДЕР_СМТП_АДДРЕСС_А, ПР_СЕНДЕР_СМТП_АДДРЕСС_В  <br/> |
|Идентификатор:  <br/> |0x5D01  <br/> |
|Тип данных:  <br/> |ПТ_УНИКОДЕ, PT_STRING8  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство представляет собой пример свойств адреса для отправителя сообщения. Он должен быть задан поставщиком исходящей транспортировки, который никогда не должен распространять какие бы то ни было существующие значения.
  
Если поставщик транспорта не предоставил свойства адреса отправителя, то диспетчер очереди MAPI пытается заполнить их, вызвав метод [IMAPISession:: куеридентити](imapisession-queryidentity.md) для идентификатора записи. Если не указаны никакие идентификаторы записей, диспетчер очереди MAPI сохраняет значение "Unknown" во всех свойствах адреса отправителя типа ПТ_УНИКОДЕ или PT_STRING8. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСОПОСТ]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов POST.
    
[[MS — ОКСОТАСК]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Задает свойства и операции, которые являются допустимыми для объектов контакта и личного списка рассылки.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

