---
title: Каноническое свойство PidTagOriginatingMtaCertificate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414811"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>Каноническое свойство PidTagOriginatingMtaCertificate

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор агента передачи сообщений (MTA), зародив сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|Идентификатор:  <br/> |0x0E25  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство, если установлено, доступно для отправленных сообщений в папке Отправленные элементы.
  
Это свойство соответствует атрибуту отчета X.400 за сообщение.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

