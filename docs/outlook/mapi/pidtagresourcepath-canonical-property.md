---
title: Каноническое свойство PidTagResourcePath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429861"
---
# <a name="pidtagresourcepath-canonical-property"></a>Каноническое свойство PidTagResourcePath

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит путь к серверу поставщика услуг.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕСАУРЦЕ_ПАС, ПР_РЕСАУРЦЕ_ПАС_А, ПР_РЕСАУРЦЕ_ПАС_В  <br/> |
|Идентификатор:  <br/> |0x3E07  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Путь, содержащийся в этих свойствах, представляет предполагаемый путь, по которому пользователь может найти ресурсы. Определение этих свойств относится к конкретному поставщику. Например, приложение для планирования использует эти свойства, чтобы указать предполагаемое расположение для файлов приложений планирования.
  
Профиль пользователя обмена сообщениями предоставляет эти свойства для удобства, чтобы клиентское приложение не предложит пользователю обмена сообщениями сетевой путь или букву сетевого диска.
  
MAPI работает только с именами файлов в наборе символов ANSI (американский национальный институт стандартизации). Приложения, использующие имена файлов в наборе символов OEM, должны преобразовать их в ANSI перед вызовом функции MAPI.
  
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

