---
title: Каноническое свойство PidTagSentRepresentingName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: bfee6c5e-d4c6-442e-af71-23156569fed5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e2df13f4e9c5d1d636c4f71ea6805ac031899e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314933"
---
# <a name="pidtagsentrepresentingname-canonical-property"></a>Каноническое свойство PidTagSentRepresentingName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемое имя пользователя обмена сообщениями, представленного отправителем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ, ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ_А, ПР_СЕНТ_РЕПРЕСЕНТИНГ_НАМЕ_В  <br/> |
|Идентификатор:  <br/> |0x0042  <br/> |
|Тип данных:  <br/> |ПТ_УНИКОДЕ, PT_STRING8  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства являются примерами свойств адресов для пользователя обмена сообщениями, представленного отправителями. Когда клиентское приложение отправляет сообщение от имени другого клиента, он должен задать всем представленным свойствам отправителя значения для этого клиента. Пользователь обмена сообщениями, который отправляется от собственного имени, обычно оставляет свойства предоставленных отправителей неопределенными.
  
Поставщик исходящей транспортировки всегда должен оставить это свойство без изменений, если оно было задано отправляющим клиентом. Если это не так, поставщик транспорта должен задать для него значение **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)) в исходящей копии сообщения и оставить его незаданным для локальной копии.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/cc433482%28EXCHG.80%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСОРСС]](https://msdn.microsoft.com/library/cc463884%28EXCHG.80%29.aspx)
  
> Задает свойства и операции, представляющие элементы RSS.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСКМАИЛ]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразует стандартные правила электронной почты из Интернета в объекты сообщений.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
[[MS — ОКСОКФГ]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Задает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.
    
[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.
    
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



[Каноническое свойство PidTagDisplayName](pidtagdisplayname-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

