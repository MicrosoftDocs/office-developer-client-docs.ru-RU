---
title: Каноническое свойство PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439844"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Каноническое свойство PidTagRemoteProgress

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Это свойство содержит номер, который указывает состояние удаленной передачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Идентификатор:  <br/> |0x3E0B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Если передача не продолжается, это свойство должно быть установлено в 1. Если передача находится в стадии выполнения, она должна быть установлена в значении от 0 до 100, указывающее процент завершения передачи.
  
Текст, связанный с числовым кодом состояния, отображается в **свойстве PR_REMOTE_PROGRESS_TEXT** [(PidTagRemoteProgressText).](pidtagremoteprogresstext-canonical-property.md)
  
Для этого свойства можно установить следующие флаги:
  
MSGSTATUS_REMOTE_DELETE
  
> Передача сообщений удаляется.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Передача сообщений продолжается.
    
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

