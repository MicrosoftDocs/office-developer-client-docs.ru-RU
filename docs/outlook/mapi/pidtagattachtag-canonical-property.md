---
title: Каноническое свойство PidTagAttachTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTag
api_type:
- HeaderDef
ms.assetid: 3d223809-b697-47c6-bc3c-2206aff7ad33
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: af5d05ee6d3592694952002c16e16188c3e458a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565622"
---
# <a name="pidtagattachtag-canonical-property"></a>Каноническое свойство PidTagAttachTag

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор объекта ASN.1 определение приложения, предоставленные вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_TAG  <br/> |
|Идентификатор:  <br/> |0x370A  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет приложения, изначально создавшего вложение.
  
 **Примечание** Не следует путать свойства **PR_ATTACH_TAG** и **PR_ATTACH_ENCODING** ([PidTagAttachEncoding](pidtagattachencoding-canonical-property.md)). Они не пару и связанные с. **PR_ATTACH_ENCODING** определяет алгоритм, используемый для преобразования данных в вложения. «Объект» имеет значение намного более общие в идентификатор объекта терминов и об использовании X.400, чем в объектно ориентированного программирования. 
  
Идентификаторы объектов синтаксис и образец идентификатор объекта определены в MAPIOID. Файл заголовка. Значения для **PR_ATTACH_TAG** не только, определенных в MAPIOID. З. 
  
Полные сведения о идентификаторы объектов обратитесь к документации по ASN.1, X.208 и X.209. Идентификатор объекта находится в элементе ссылка приложения среды часть перенос текста файла (FTBP). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

