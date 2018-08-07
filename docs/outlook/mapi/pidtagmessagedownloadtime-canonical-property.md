---
title: Каноническое свойство PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811357"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Каноническое свойство PidTagMessageDownloadTime

  
  
**Относится к**: Outlook 
  
Содержит предполагаемое время для загрузки сообщения с удаленного сервера в хранилище локального сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Идентификатор:  <br/> |0x0E18  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общие системы обмена сообщениями  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство выражается в секундах и представляет наилучшую оценку времени, потребуется поставщик удаленного транспорта для загрузки данного сообщения из текущего места для хранения сообщений локальной папке заголовка клиенту. Поставщик удаленного транспорта обычно рассчитываются значение для этого свойства значение свойства **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)), скорость канала связи в байтах в секунду. Если поставщик не удается вычислить время загрузки, например, если не известно, скорость соединения, его следует предоставлять **PT_ERROR** значение например **MAPI_E_NO_SUPPORT** для этого столбца в таблице содержимое папки заголовок. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

