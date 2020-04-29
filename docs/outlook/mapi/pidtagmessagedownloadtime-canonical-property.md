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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407930"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Каноническое свойство PidTagMessageDownloadTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит предполагаемое время для загрузки сообщения с удаленного сервера в локальное хранилище сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Идентификатор:  <br/> |0x0E18  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство выражается в секундах и представляет собой наилучшую оценку времени, в течение которого он получит доступ к удаленному поставщику транспорта, чтобы скачать данное сообщение из текущего расположения в хранилище сообщений, локальное на клиенте, просматривая папку заголовков. Удаленный поставщик транспорта обычно вычисляет значение этого свойства, путем деления значения свойства **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) на скорость канала связи (в байтах в секунду). Если поставщик не может рассчитать время загрузки, например, если он не знает скорость связи, он должен указать значение **PT_ERROR** , например **MAPI_E_NO_SUPPORT** для этого столбца в таблице содержимое папки заголовков. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

