---
title: Каноническое свойство PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425640"
---
# <a name="pidtagprovidericon-canonical-property"></a>Каноническое свойство PidTagProviderIcon

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит строку Unicode, которая указывает настраиваемый значок или значки, отображаемые для поставщика MAPI в панели Microsoft Office Outlook состояния как в интернете, так и в автономном режиме.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Идентификатор:  <br/> |0x3417  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

В этих свойствах указывается файл ресурса, содержащий настраиваемый значок, который представляет поставщика MAPI в онлайновом состоянии, и необязательно другой настраиваемый значок в автономном состоянии. Outlook всегда запрашивает эти свойства в представлении Юникод. 
  
Например, следующее значение свойства Outlook загрузить значок ID 1001 из модуля mymod32.dll и использовать этот значок для состояния online: `mymod32.dll,#1001` . Так как для автономного состояния нет значка, определенного для поставщика, в этом случае в панели состояния используется стандартный значок Outlook автономного режима. 
  
Следующее значение свойства Outlook загрузить значок ID 1001 из модуля mymod32.dll и использовать этот значок для состояния online, а также загрузить значок ID 1002 из этого же модуля, который будет использоваться для автономного состояния: `mymod32.dll,#1001,#1002` . В Outlook не используется значок состояния. 
  
По умолчанию, если не указаны настраиваемые значки, поставщик представлен значками Outlook по умолчанию для состояния online и автономного состояния. Поставщик может дополнительно указать имя отображения, которое будет отображаться рядом с значком в панели состояния. Дополнительные сведения см. **в PR_PROVIDER_DISPLAY_NAME_W** [(PidTagProviderDisplayName).](pidtagproviderdisplayname-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

