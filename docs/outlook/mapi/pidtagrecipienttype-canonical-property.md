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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385846"
---
# <a name="pidtagrecipienttype-canonical-property"></a>Каноническое свойство PidTagRecipientType

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип получателя для получателя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Идентификатор:  <br/> |0x0C15  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Тип получателя, содержащиеся в этом свойстве состоит из одного необходимые значения и один необязательный флаг.
  
Это свойство должно содержать только один из следующих значений:
  
MAPI_TO 
  
> Получатель является основным (получателю). Клиентам требуется обрабатывать получателей. ��� ��������� ���� �������� ���������������.
    
MAPI_CC 
  
> Получатель является получателей скрытой копии (CC), получателя, который получает сообщение в дополнение к получателей.
    
MAPI_BCC 
  
> Получатель является получателей скрытой копии (СК). Основная база данных и копии получатели не знают о наличии получателей скрытой копии. 
    
MAPI_P1 
  
> Получатель не получил сообщение на Предыдущая попытка успешно. Это отправить более ранних передачи.
    
Кроме того можно задать следующий флаг:
  
MAPI_SUBMITTED 
  
> Получатель уже получил сообщение и не требуется получать еще раз. Это отправить более ранних передачи. Этот флаг устанавливается вместе с **MAPI_TO**, **MAPI_CC**и **MAPI_BCC** значения. 
    
Значение MAPI_P1 и флаг **MAPI_SUBMITTED** используются повторно отправлено сообщение из-за недоставке к одному или нескольким указанным получателям. Для этой повторной передачи клиента задает **MAPI_SUBMITTED** для каждого получателя, который не обязательно сообщение еще раз, но должно отображаться в списке получателей. Для каждого получателя, который ранее не получил сообщение клиент сохраняет исходный получатель на **PR_RECIPIENT_TYPE** значение без изменений, но кроме того отправляет копию получателя с MAPI_P1 вместо исходное значение. Эта копия, удаляется перед доставкой фактический принудительно получателя в конверте P1 и гарантирует физических повторной передачи получателя. Свойство **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) задано значение FALSE для MAPI_P1 получателей.
  
При клиента отображается форма отправить, отображаются только MAPI_P1 получателей. Если пользователь вводит дополнительных получателей при доставке сообщения, список получателей отображается точно так же, как и когда сообщение было отправлено в первый раз. 
  
**PR_DISPLAY_TO** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md)), **PR_DISPLAY_CC** ([PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)) и **PR_DISPLAY_BCC** ([PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)) свойства связаны с тип получателя. Если клиент вызывает сообщение **IMAPIProp::SaveChanges** и имеется хотя бы одного получателя в список получателей, поставщик хранения сообщений задает эти свойства следующим образом: 
  
|**Свойство**|**Описание**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Задайте значение TRUE, если один или несколько получателей, **MAPI_TO** получателей.  <br/> |
|PR_DISPLAY_CC  <br/> |Задайте значение TRUE, если один или несколько получателей, **MAPI_CC** получателей.  <br/> |
| PR_DISPLAY_BCC  <br/> |Задайте значение TRUE, если один или несколько получателей, **MAPI_BCC** получателей.  <br/> |
   
В X.400 конверт P1 или доставки — это сведения, необходимые для доставки сообщений, включая свойства адрес получателя и любые флаги управления доставки и ответов. Конверт P2 или отображения, сведения, обычно отображается для каждого получателя, отличный от самого текста сообщения. Как правило, включает тему, важность, приоритет, уровень конфиденциальности сообщения и время отправки, а также основной и скопированной получателей. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщения электронной почты.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRecipientStatus](pidtagrecipientstatus-canonical-property.md)
  
[Каноническое свойство PidTagDisplayTo](pidtagdisplayto-canonical-property.md)
  
[Каноническое свойство PidTagDisplayBcc](pidtagdisplaybcc-canonical-property.md)
  
[Каноническое свойство PidTagDisplayCc](pidtagdisplaycc-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

