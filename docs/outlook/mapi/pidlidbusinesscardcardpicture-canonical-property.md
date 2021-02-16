---
title: Каноническое свойство PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fd1ad923acca5a75d06e6b15ae7ae7411edefb92
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342009"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Каноническое свойство PidLidBusinessCardCardPicture

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит изображение визитной карточки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidBCCardPicture  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008041  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Примечания

Значением этого свойства должен быть переносной сетевой графики (PNG) или jpEG-поток. Это свойство следует использовать в сочетании со свойством **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition)](pidlidbusinesscarddisplaydefinition-canonical-property.md)следующим образом: **dispidBCCardPicture** не должен присутствовать в контакте, если **dispidBCDisplayDefinition** не существует. Это свойство также не должно присутствовать, если данные **в dispidBCCardPicture** не требуют изображения карточки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения наборов свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

