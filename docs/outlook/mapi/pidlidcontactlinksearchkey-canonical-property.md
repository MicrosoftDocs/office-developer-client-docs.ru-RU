---
title: Каноническое свойство PidLidContactLinkSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactLinkSearchKey
api_type:
- COM
ms.assetid: 82d21d38-a6c6-4e12-85b1-8158b2f5cce7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea815631f63b5585a3f2705cfbd2639b8c655e6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319777"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Каноническое свойство PidLidContactLinkSearchKey

**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список **searchKeys для** контакта, связанного с этим объектом сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactLinkSearchKey  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008584  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Примечания

|**Длина в bytes**|**Описание**|**Примечания**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Нет  <br/> |
|переменная  <br/> |Данные SearchKey  <br/> |Повторяет время contactEntryCount  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также

- [Свойства MAPI](mapi-properties.md) 
- [Канонические свойства MAPI](mapi-canonical-properties.md)
- [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

