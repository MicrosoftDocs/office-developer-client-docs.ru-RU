---
title: Каноническое свойство PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316515"
---
# <a name="pidtagaccess-canonical-property"></a>Каноническое свойство PidTagAccess

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающих операции, доступные клиенту для объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АКЦЕСС  <br/> |
|Идентификатор:  <br/> |0x0FF4  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Свойства управления доступом  <br/> |
   
## <a name="remarks"></a>Замечания

Для клиента это свойство доступно только для чтения. Он должен быть побитовым **или** содержать от нуля или более значений из таблицы ниже. 
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|МАПИ_АКЦЕСС_МОДИФИ  <br/> |0x00000001  <br/> |Запись  <br/> |
|МАПИ_АКЦЕСС_РЕАД  <br/> |0x00000002  <br/> |Чтение  <br/> |
|МАПИ_АКЦЕСС_ДЕЛЕТЕ  <br/> |0x00000004  <br/> |Delete  <br/> |
|МАПИ_АКЦЕСС_КРЕАТЕ_ХИЕРАРЧИ  <br/> |0x00000008  <br/> |Создание вложенных папок в иерархии папок  <br/> |
|МАПИ_АКЦЕСС_КРЕАТЕ_КОНТЕНТС  <br/> |0x00000010  <br/> |Создание сообщений с содержимым  <br/> |
|МАПИ_АКЦЕСС_КРЕАТЕ_АССОЦИАТЕД  <br/> |0x00000020  <br/> |Создание связанных сообщений с содержимым  <br/> |
   
Флаги МАПИ_АКЦЕСС_ДЕЛЕТЕ, МАПИ_АКЦЕСС_МОДИФИ и МАПИ_АКЦЕСС_РЕАД находятся в папках и объектах сообщений, а также в столбцах **пр_акцесс** в таблицах контента и связанных таблицах содержимого. Флаги МАПИ_АКЦЕСС_КРЕАТЕ_АССОЦИАТЕД, МАПИ_АКЦЕСС_КРЕАТЕ_КОНТЕНТС и МАПИ_АКЦЕСС_КРЕАТЕ_ХИЕРАРЧИ доступны только для объектов Folder. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

