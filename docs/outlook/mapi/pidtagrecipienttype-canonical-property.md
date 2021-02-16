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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип получателя сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_TYPE  <br/> |
|Идентификатор:  <br/> |0x0C15  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Тип получателя, содержащийся в этом свойстве, состоит из одного обязательного значения и одного необязательного флага.
  
Это свойство должно содержать одно из следующих значений:
  
MAPI_TO 
  
> Получатель является основным (to) получателем. Клиенты необходимы для обработки основных получателей. ��� ��������� ���� �������� ���������������.
    
MAPI_CC 
  
> Получателем является получатель копии ( CC), получатель, который получает сообщение в дополнение к основным получателям.
    
MAPI_BCC 
  
> Получатель является получателем незрячих копий (BCC). Получатели основных копий и получателей копии не знают о существовании получателей копии. 
    
MAPI_P1 
  
> Получатель не получил сообщение при предыдущей попытке. Это повторное сообщение о более ранней передаче.
    
Кроме того, можно установить следующий флаг:
  
MAPI_SUBMITTED 
  
> Получатель уже получил сообщение, и ему не нужно его снова получать. Это повторное сообщение о более ранней передаче. Этот флаг устанавливается вместе со значениями **MAPI_TO,** **MAPI_CC** и **MAPI_BCC.** 
    
Значения MAPI_P1 и флаг **MAPI_SUBMITTED** используются при повторной перенастройки сообщения из-за ненастроенной связи с одним или более получателями. Для этой повторной передачи клиент MAPI_SUBMITTED для каждого **получателя,** который больше не нуждается в сообщении, но должен отображаться в списке получателей. Для каждого получателя, который не получил сообщение ранее, клиент сохраняет исходного получателя со значением **PR_RECIPIENT_TYPE** без изменений, но дополнительно передает копию получателя с MAPI_P1 в качестве исходного значения. Эта копия, которая отбрасывается до фактической доставки, заставляет получателя в конверт P1 и гарантирует физическую ретрансцию этому получателю. Свойству **PR_RESPONSIBILITY** [(PidTagResponsibility)](pidtagresponsibility-canonical-property.md)для MAPI_P1 задается false.
  
При отображении клиентом формы повторной MAPI_P1 отображаются только получатели. Если пользователь не вводит дополнительных получателей, при доставке сообщения список получателей отображается точно так же, как при первой доставке сообщения. 
  
Свойства **PR_DISPLAY_TO** ([PidTagDisplayTo),](pidtagdisplayto-canonical-property.md) **PR_DISPLAY_CC** ([PidTagDisplayCc)](pidtagdisplaycc-canonical-property.md)и **PR_DISPLAY_BCC** ([PidTagDisplayBcc)](pidtagdisplaybcc-canonical-property.md)связаны с типом получателя. Когда клиент вызывает **IMAPIProp::SaveChanges** сообщения и в списке получателей есть по крайней мере один получатель, поставщик службы хранения сообщений задает эти свойства следующим образом: 
  
|**Свойство**|**Описание**|
|:-----|:-----|
|PR_DISPLAY_TO  <br/> |Установите true, если один или несколько  получателей MAPI_TO получателей.  <br/> |
|PR_DISPLAY_CC  <br/> |Установите true, если один или несколько  получателей являются MAPI_CC получателями.  <br/> |
| PR_DISPLAY_BCC  <br/> |Установите true, если один или несколько  получателей MAPI_BCC получателей.  <br/> |
   
В X.400 конверт P1 или конверт доставки — это сведения, необходимые для доставки сообщения, включая свойства адреса получателя и любые флажки вариантов, управляющие доставкой и ответами. Конверт P2 или отображения — это сведения, которые обычно отображаются для каждого получателя, кроме самого текста сообщения. Обычно он включает тему, важность, приоритет, конфиденциальность и время отправки, а также имена основных и скопированные получателей. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов сообщений электронной почты.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовок

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
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

