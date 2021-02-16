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
  
Содержит сертификат ASN.1 получателя сообщения для использования в отчете.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECIPIENT_CERTIFICATE  <br/> |
|Идентификатор:  <br/> |0x0C13  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Получатель MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является копией свойства PR_USER_CERTIFICATE **(** [PidTagUserCertificate)](pidtagusercertificate-canonical-property.md)для использования в отчете. Его можно использовать для того, чтобы доказать источнику, что получатель действительно получил сообщение, что в отчете о доставке не обязательно указывается.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

