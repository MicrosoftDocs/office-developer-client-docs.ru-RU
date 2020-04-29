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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436827"
---
# <a name="pidtagservicedeletefiles-canonical-property"></a>Каноническое свойство PidTagServiceDeleteFiles

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит список имен файлов, которые необходимо удалить при удалении службы сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SERVICE_DELETE_FILES, PR_SERVICE_DELETE_FILES_A PR_SERVICE_DELETE_FILES_W  <br/> |
|Идентификатор:  <br/> |0x3D10  <br/> |
|Тип данных:  <br/> |PT_MV_STRING8 PT_MV_UNICODE  <br/> |
|Область:  <br/> |Профиль MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Имена файлов из списка, содержащегося в этих свойствах, удаляются с компьютера при использовании панели управления для удаления службы сообщений. Не включайте в список всех библиотек DLL, поддерживающих несколько служб сообщений, или непреднамеренно удаляются дополнительные службы сообщений.
  
MAPI работает только с именами файлов и другими строками, передаваемыми в нее, в наборе знаков ANSI. Приложения, использующие имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом MAPI.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

