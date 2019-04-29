---
title: Каноническое свойство PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422777"
---
# <a name="pidtagprovideruid-canonical-property"></a>Каноническое свойство PidTagProviderUid

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит структуру **мапиуид** поставщика услуг, который обрабатывает сообщение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРОВИДЕР_УИД  <br/> |
|Идентификатор:  <br/> |0x300C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общие протоколы MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство вычисляется всеми поставщиками служб. Он содержит структуру [мапиуид](mapiuid.md) , связанную с, и обычно жестко запрограммированную поставщиком. Он обычно используется клиентским приложением, которое заинтересовано только в контейнерах адресной книги, предоставленных определенным поставщиком. 
  
Это свойство отображается только в качестве записи столбца в таблице поставщика.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

