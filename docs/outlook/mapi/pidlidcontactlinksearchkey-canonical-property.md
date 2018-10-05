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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387498"
---
# <a name="pidlidcontactlinksearchkey-canonical-property"></a>Каноническое свойство PidLidContactLinkSearchKey

**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список **SearchKeys** для контакта, связанного с объектом сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactLinkSearchKey  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008584  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Замечания

|**Длина в байтах**|**Описание**|**Примечания**|
|:-----|:-----|:-----|
|2  <br/> |ContactEntryCount  <br/> |Отсутствует  <br/> |
|переменная  <br/> |SearchKey данных  <br/> |Повторяет ContactEntryCount раз  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также

- [Свойства MAPI](mapi-properties.md) 
- [Каноническое свойства MAPI](mapi-canonical-properties.md)
- [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

