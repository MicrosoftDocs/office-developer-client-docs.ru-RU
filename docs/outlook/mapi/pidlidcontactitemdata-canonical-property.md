---
title: Каноническое свойство PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810236"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Каноническое свойство PidLidContactItemData

  
  
**Относится к**: Outlook 
  
Используется для отображения контактных данных.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidContactItemData  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008007  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Если этот параметр указан, свойство должно иметь шесть записи, соответствующие каждой к полю видимой в пользовательском интерфейсе приложения.
  
|**На основе одного индекса в многозначное свойство**|**Значение должно быть одно из следующих**|**Описание**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |Приложения должны отображать домашний адрес контакта.  <br/> |
|1  <br/> |0x00000002 или 0x00000000  <br/> |Приложения должны отображать работы контакта.  <br/> |
|1  <br/> |0x00000003  <br/> |Приложения должны отображать контакт в другой адрес.  <br/> |
|2  <br/> |0x00008080  <br/> |Приложения должны отображать Email1.  <br/> |
|2  <br/> |0x00008090  <br/> |Приложения должны отображать Почта2:.  <br/> |
|2  <br/> |0x000080A0  <br/> |Приложения должны отображать Почта3:.  <br/> |
|3,4,5,6  <br/> |PropertyID свойства телефона или любой из номеров факсов, который указан в [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |Приложения должны отображать соответствующего свойства.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

