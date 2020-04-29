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
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431668"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a>Каноническое свойство PidTagRecipientCertificate

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит сертификат получателя сообщения ASN. 1 получателя, который будет использоваться в отчете.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Идентификатор:  <br/> |0x0C13  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является копией свойства **PR_USER_CERTIFICATE** получателя ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) для использования в отчете. Его можно использовать, чтобы доказать инициатор, который фактически получал сообщение, что отчет о доставке не обязательно указывает.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

