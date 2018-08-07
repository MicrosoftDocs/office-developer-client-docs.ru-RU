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
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811592"
---
# <a name="pidtagprovidericon-canonical-property"></a>Каноническое свойство PidTagProviderIcon

  
  
**Относится к**: Outlook 
  
Содержит строку Юникода, задает пользовательский значок или значки, отображаемые для поставщика MAPI в строке состояния Microsoft Office Outlook в США и в автономном режиме.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROVIDER_ICON PR_PROVIDER_ICON_W  <br/> |
|Идентификатор:  <br/> |0x3417  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Хранение сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства укажите файл ресурсов, содержащий пользовательский значок, представляющий поставщика MAPI в оперативном состоянии, и при необходимости другой пользовательский значок в автономный режим. Outlook всегда запрашивает этих свойств в Юникод. 
  
К примеру, следующее значение свойства указывает Outlook, чтобы загрузить значок ID 1001 из mymod32.dll модуль и использовать этот значок для состояние online: `mymod32.dll,#1001`. Так как значок не зависящие от поставщика для автономный режим, в этом случае в строке состояния используется стандартный значок автономной Outlook. 
  
Следующее значение свойства указывает Outlook можно загрузить значок ID 1001 из mymod32.dll модуль и используйте этот значок для состояние online, а также загрузить значок ID 1002 из этой же модуль для использования в автономный режим: `mymod32.dll,#1001,#1002`. Значок Outlook не используется в строке состояния. 
  
По умолчанию если нет настраиваемых значков не заданы, поставщик представлены значки Outlook по умолчанию состояние online и автономный режим. Поставщик при необходимости можно указать отображаемое имя, которое будет отображаться рядом со значком в строке состояния. Для получения дополнительных сведений см **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
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

