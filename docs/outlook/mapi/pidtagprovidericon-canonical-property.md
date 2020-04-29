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
  
Содержит строку Юникода, указывающую настраиваемый значок или значки, которые будут отображаться для поставщика MAPI в строке состояния Microsoft Office Outlook как в оперативном, так и в автономном состояниях.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ICON PR_PROVIDER_ICON_W  <br/> |
|Идентификатор:  <br/> |0x3417  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

В этих свойствах указывается файл ресурсов, который содержит пользовательский значок, представляющий поставщика MAPI в интерактивном состоянии, и (при необходимости) другой настраиваемый значок в автономном состоянии. Outlook всегда запрашивает эти свойства в представлении Юникод. 
  
Например, следующее значение свойства указывает, что Outlook должен загрузить идентификатор Icon 1001 из модуля mymod32. dll и использовать этот значок в интерактивном режиме: `mymod32.dll,#1001`. Так как для автономного состояния отсутствует значок, зависящий от поставщика, в строке состояния используется стандартный значок Outlook offline. 
  
Следующее значение свойства указывает, что Outlook загружает идентификатор Icon 1001 из модуля mymod32. dll и использует этот значок для состояния Online, а также для загрузки кода Icon 1002 из этого же модуля для использования в автономном состоянии: `mymod32.dll,#1001,#1002`. В строке состояния не используется значок Outlook. 
  
По умолчанию, если настраиваемые значки не указаны, поставщик представляется значками Outlook по умолчанию для состояния Online и автономным состоянием. Поставщик может дополнительно указать отображаемое имя, которое будет отображаться рядом со значком в строке состояния. Дополнительные сведения см **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
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

