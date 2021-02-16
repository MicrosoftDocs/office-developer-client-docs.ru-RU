---
title: Каноническое свойство PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278794"
---
# <a name="pidtagstatus-canonical-property"></a>Каноническое свойство PidTagStatus

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит 32-битовую битовуюmask флагов, определяя состояние папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STATUS  <br/> |
|Идентификатор:  <br/> |0x360B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство для папок аналогично свойству **PR_MSG_STATUS** [(PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)для сообщений. Его флаги предоставляются только для клиентского приложения и не влияют на хранилище сообщений. Клиенты могут использовать или игнорировать эти параметры. Клиент также может определить собственные значения для определяемых клиентом битов этого свойства.
  
Для битовойmask можно установить один или несколько из следующих флагов:
  
FLDSTATUS_DELMARKED 
  
> Папка помечена для удаления. Клиентские приложения устанавливают этот флаг.
    
FLDSTATUS_HIDDEN 
  
> Папка скрыта.
    
FLDSTATUS_HIGHLIGHTED 
  
> Папка выделена, например, в обратном видео.
    
FLDSTATUS_TAGGED 
  
> Папка помечена тегом.
    
Поставщики store сообщений присваивают этому свойству папки одно или несколько из этих значений, и клиенты интерпретируют состояние соответствующим образом для своих приложений. Например, клиент может использовать состояние папки, чтобы визуально различать папки в таблице иерархии, отображая папки с одинаковым состоянием таким же образом. Выделенная папка может быть показана в обратном видео, помеченные папки и папки, помеченные для удаления, могут быть помечены осмысленным значком, а скрытые папки можно скрыть.
  
Биты от 16 до 31 ("0x10000" через "0x80000000") этого свойства доступны для использования клиентского приложения IPM. Все остальные биты зарезервированы для использования в MAPI; те, которые не определены в предыдущем списке, должны изначально иметь нулевое значение и не изменяться.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

