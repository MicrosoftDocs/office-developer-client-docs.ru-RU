---
title: Каноническое свойство PidTagServiceDeleteFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDeleteFiles
api_type:
- COM
ms.assetid: 9ec80a93-9e8f-46be-a1d4-7648aae47fec
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da01385f83d9af9ad02eeb2fed08e3bc22d4df84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336402"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Каноническое свойство PidTagServiceDeleteFiles

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит список имен файлов, которые необходимо удалить при удалении службы сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕРВИЦЕ_ДЕЛЕТЕ_ФИЛЕС, ПР_СЕРВИЦЕ_ДЕЛЕТЕ_ФИЛЕС_А, ПР_СЕРВИЦЕ_ДЕЛЕТЕ_ФИЛЕС_В  <br/> |
|Идентификатор:  <br/> |0x3D10  <br/> |
|Тип данных:  <br/> |PT_MV_STRING8, ПТ_МВ_УНИКОДЕ  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Имена файлов из списка, содержащегося в этих свойствах, удаляются с компьютера при использовании панели управления для удаления службы сообщений. Не включайте в список всех библиотек DLL, поддерживающих несколько служб сообщений, или непреднамеренно удаляются дополнительные службы сообщений.
  
MAPI работает только с именами файлов и другими строками, передаваемыми в нее, в наборе знаков ANSI. Приложения, использующие имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

