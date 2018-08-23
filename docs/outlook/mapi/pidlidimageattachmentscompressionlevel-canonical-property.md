---
title: Каноническое свойство PidLidImageAttachmentsCompressionLevel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55b965374bb1d7e5859f0cac5cc2f61956ea5b55
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578922"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>Каноническое свойство PidLidImageAttachmentsCompressionLevel

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Определяет уровень сжатия для применения на attachments изображения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008593  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация во время выполнения  <br/> |
   
## <a name="remarks"></a>Замечания

Ниже приведены уровни допустимый сжатие.
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

