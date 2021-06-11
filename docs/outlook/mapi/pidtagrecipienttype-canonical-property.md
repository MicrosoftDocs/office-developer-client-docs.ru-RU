---
title: Каноническое свойство PidTagRecipientType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientType
api_type:
- COM
ms.assetid: 67e31027-6bc2-4a40-9b00-d61baef4ab0f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9d74fdb3acb6db94078d6090f0def050fb564cd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355260"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Каноническое свойство PidTagRecipientType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит тип получателя для получателя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Идентификатор:  <br/> |0x0C15  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Тип получателя, содержащийся в этом свойстве, состоит из одного необходимого значения и одного необязательного флага.
  
Это свойство должно содержать одно из следующих значений:
  
MAPI_TO 
  
> Получатель — основной получатель (To). Клиенты должны обрабатывать основных получателей. ��� ��������� ���� �������� ���������������.
    
MAPI_CC 
  
> Получатель — получатель углеродной копии (CC), получатель, который получает сообщение в дополнение к основным получателям.
    
MAPI_BCC 
  
> Получатель — получатель слепой копии углерода (BCC). Получатели первичной и углеродной копии не знают о существовании получателей BCC. 
    
MAPI_P1 
  
> Получатель не получил сообщение во время предыдущей попытки. Это повторное сообщение более ранней передачи.
    
Кроме того, можно установить следующий флаг:
  
MAPI_SUBMITTED 
  
> Получатель уже получил сообщение и не нуждается в его повторном получении. Это повторное сообщение более ранней передачи. Этот флаг устанавливается в сочетании с **значениями MAPI_TO,** **MAPI_CC** и **MAPI_BCC.** 
    
Значение MAPI_P1 и флаг **MAPI_SUBMITTED** используются при повторной перенастройки сообщения из-за неделивного использования для одного или более получателей. Для этой повторной передачи  клиент задает MAPI_SUBMITTED для каждого получателя, который снова не нуждается в сообщении, но должен отображаться в списке получателей. Для каждого получателя, который не получил сообщение ранее, клиент сохраняет исходного получателя с его **значением PR_RECIPIENT_TYPE** неизменным, но дополнительно представляет копию получателя с MAPI_P1 на место исходного значения. Эта копия, отбрасывается до фактической доставки, заставляет получателя в конверт P1 и гарантирует физическую ретрансмиссию этому получателю. Свойство **PR_RESPONSIBILITY** [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)задавалось false для MAPI_P1 получателей.
  
При отображении формы повторной MAPI_P1 клиент. Если пользователь не вводит дополнительных получателей, при доставке сообщения список получателей отображается точно так же, как и при первом отправлении сообщения. 
  
Свойства **PR_DISPLAY_TO** [(PidTagDisplayTo),](pidtagdisplayto-canonical-property.md) **PR_DISPLAY_CC** [(PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)и **PR_DISPLAY_BCC** [(PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)связаны с типом получателя. Если клиент вызывает **IMAPIProp::SaveChanges** сообщения и в списке получателей есть по крайней мере один получатель, поставщик магазина сообщений задает эти свойства следующим образом: 
  
|**Свойство**|**Описание**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Установите true, если один или несколько получателей являются **MAPI_TO** получателями.  <br/> |
|PR_DISPLAY_CC  <br/> |Установите true, если один или несколько получателей являются **MAPI_CC** получателями.  <br/> |
| PR_DISPLAY_BCC  <br/> |Установите true, если один или несколько получателей являются **MAPI_BCC** получателями.  <br/> |
   
В X.400 конверт P1 или доставка — это сведения, необходимые для доставки сообщения, включая свойства адреса получателя и любые флаги параметра, контролирующие доставку и ответы. Конверт P2 или дисплей — это сведения, обычно отображаемые каждому получателю, кроме самого текста сообщения. Как правило, он включает тему, значение, приоритет, чувствительность и время отправки, а также основные и скопированные имена получателей. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Каноническое свойство PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Каноническое свойство PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Каноническое свойство PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

