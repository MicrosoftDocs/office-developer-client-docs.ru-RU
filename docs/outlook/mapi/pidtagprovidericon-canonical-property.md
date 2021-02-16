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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит строку Юникода, которая указывает настраиваемый значок или значки, отображаемые для поставщика MAPI в строке Microsoft Office Outlook состояния в интерактивном и автономном состояниях.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Идентификатор:  <br/> |0x3417  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства указывают файл ресурсов, содержащий настраиваемый значок, который представляет поставщика MAPI в сетевом состоянии, и, при желании, другой пользовательский значок в автономном состоянии. Outlook всегда запрашивает эти свойства в представлении Юникод. 
  
Например, следующее значение свойства предписывает Outlook загрузить значок 1001 из модуля mymod32.dll и использовать этот значок для сетевого состояния:  `mymod32.dll,#1001` . Так как для автономного состояния не существует специального значка поставщика, в данном случае стандартный значок автономного режима Outlook используется в панели состояния. 
  
Следующее значение свойства предписывает Outlook загрузить значок 1001 из модуля mymod32.dll и использовать этот значок для сетевого состояния, а также загрузить значок 1002 из этого же модуля для использования в автономном  `mymod32.dll,#1001,#1002` состоянии: Значок Outlook не используется в панели состояния. 
  
По умолчанию, если пользовательские значки не указаны, поставщик представлен значками Outlook по умолчанию для состояния в сети и автономного состояния. При желании поставщик может указать отображаемую именем рядом со значком в панели состояния. Дополнительные сведения **см. в PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName).](pidtagproviderdisplayname-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

