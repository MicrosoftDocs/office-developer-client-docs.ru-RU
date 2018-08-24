---
title: Каноническое свойство PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3f23a332ee6778f71ce0809dfae8c0b6a92246a8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595148"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a>Каноническое свойство PidTagRecipientNumberForAdvice

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит получателя сообщения телефонного номера для звонка информацией о физической доставки сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W  <br/> |
|Идентификатор:  <br/> |0x0C14  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства предназначены для использования в сочетании с доставки физических назначения, а не электронный почтовый ящик, когда человеческого получателя не должен быть указан в доставке. Например, номер телефона на лист обложка факса.
  
## <a name="related-resources"></a>Связанные ресурсы

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

