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
ms.openlocfilehash: 8600cc7071fbe5c08d5df074f9bf59f4320b7f18
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357584"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>Каноническое свойство PidLidImageAttachmentsCompressionLevel

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет уровень сжатия, применяемый к вложениям с изображениями.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидимгаттчмтскомпресслевел  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008593  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Настройка времени выполнения  <br/> |
   
## <a name="remarks"></a>Примечания

Ниже приведены допустимые уровни сжатия:
  
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

[[MS — ОКСПРОПС]] 
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

