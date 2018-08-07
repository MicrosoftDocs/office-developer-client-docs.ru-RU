---
title: Каноническое свойство PidTagRecipientCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811663"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Каноническое свойство PidTagRecipientCertificate

  
  
**Относится к**: Outlook 
  
Содержит сертификат ASN.1 получателя сообщения для использования в отчете.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Идентификатор:  <br/> |0x0C13  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует копию получателя свойство **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) для использования в отчете. Используется для подтверждения инициатором, в том, что получатель фактически получено сообщение, которое не обязательно отчетов о доставке.
  
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

