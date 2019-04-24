---
title: Каноническое свойство PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270016"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Каноническое свойство PidTagDefaultViewEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор элемента представления по умолчанию для папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ДЕФАУЛТ_ВИЕВ_ЕНТРИД  <br/> |
|Идентификатор:  <br/> |0x3616  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство представляет собой идентификатор элемента представления папки, который должен быть установлен в качестве исходного представления. Свойство не требуется задавать, если в качестве начального представления используется "обычное представление".
  
Клиентское приложение может получить это свойство во время открытия папки и добиться значительного выигрыша в производительности. Это свойство можно использовать в качестве ярлыка для получения представления по умолчанию вместо того, чтобы открывать связанную таблицу содержимого и отправить ограничение.
  
Реализация поставщика услуг метода [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md) может копировать это свойство при копировании папок. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКФОЛД]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

