---
title: Каноническое свойство PidLidSharingInitiatorSmtp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorSmtp
api_type:
- COM
ms.assetid: 4fb7d91d-4c51-41c1-9cb6-7b837dd12f11
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb699b2312064f8ed330238962dd86992c046139
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391453"
---
# <a name="pidlidsharinginitiatorsmtp-canonical-property"></a>Каноническое свойство PidLidSharingInitiatorSmtp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает SMTP-адрес пользователя, инициировавшего сообщение о совместном доступе. Это свойство общего доступа сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingInitiatorSmtp  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008A08  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть задано значение свойства **PR_SMTP_ADDRESS** ([PidTagSmtpAddress](pidtagsmtpaddress-canonical-property.md)) из адресной книги, заданной свойством **dispidSharingInitiatorEid** ([PidLidSharingInitiatorEntryId](pidlidsharinginitiatorentryid-canonical-property.md)) и должен быть игнорируются.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Открывает общий доступ папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

