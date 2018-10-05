---
title: Каноническое свойство PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396178"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a>Каноническое свойство PidTagProfileServerFullVersion

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает полные сведения о Microsoft Exchange Server, к которому подключены учетных записей в профиле версии и построения.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_SERVER_FULL_VERSION  <br/> |
|Идентификатор:  <br/> |0x663B  <br/> |
|Тип свойства:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Настройки профилей MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Профиль можно указать один или несколько учетных записей, которые подключаются к серверу Exchange, но они должна быть соединена с одного сервера Exchange.
  
Версии Outlook, предшествующие Microsoft Office Outlook 2007 не поддерживают это свойство. Эти версии Outlook Проверьте наличие **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** в профиле. 
  
Как правило если active почтовый ящик подключен к серверу Exchange, Outlook 2007 сохраняется полный сведений о версии Exchange Server в свойстве **PR_PROFILE_SERVER_FULL_VERSION** в текущей конфигурации. Outlook хранит сведения в структуре **EXCHANGE_STORE_VERSION_NUM** , который содержит номера основной и дополнительный номер версии и номера основной и дополнительной сборок. К примеру для хранения идентификатор версии Exchange Server **8.0.685.24**основной номер версии — 8 и дополнительный номер версии — 0 и 685 — номер основной сборки и дополнительный номер — номер сборки 24.
  
Только один из **PR_PROFILE_SERVER_VERSION** или **PR_PROFILE_SERVER_FULL_VERSION** скорее всего, существуют в профиле, но не гарантируется, либо всегда существует в профиле. Outlook не записывает либо свойством только после успешного подключения к серверу Exchange. 
  
В объектной модели Outlook можно использовать свойство **ExchangeMailboxServerVersion** объекта **пространство имен** для поиска версии Exchange Server, на котором размещен почтовый ящик active. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств.
    
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

