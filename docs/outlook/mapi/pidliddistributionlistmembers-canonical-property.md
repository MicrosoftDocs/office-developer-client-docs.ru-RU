---
title: Каноническое свойство PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335072"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Каноническое свойство PidLidDistributionListMembers

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает список идентификаторами EntryID объектов, соответствующих членам личного списка рассылки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |диспиддлмемберс  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008055  <br/> |
|Тип данных:  <br/> |PT_MV_BINARY  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Участники личного списка рассылки могут быть другими личными списками рассылки, электронными адресами, входящими в контакт, глобальными списками адресов пользователей или списками рассылки или одноразовыми адресами электронной почты. Формат каждого EntryId должен быть либо одноразовым EntryIdом, указанным в разделе [[MS – окскдата],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) либо упакованным entryidм. 
  
При задании этого свойства клиент или сервер должны обеспечивать его общий размер менее 15 000 байт.
  
Это свойство указывает список одноразовых идентификаторами EntryID, соответствующих членам личного списка рассылки. Эти одноразовые идентификаторами EntryID инкапсулируют отображаемые имена и адреса электронной почты для участников личного списка рассылки.
  
Если клиент или сервер задает это свойство, его необходимо синхронизировать с этим свойством **диспиддлмемберс** для каждой записи в свойстве **диспиддлонеоффмемберс** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), в том же месте в **диспиддлонеоффмемберс**.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

