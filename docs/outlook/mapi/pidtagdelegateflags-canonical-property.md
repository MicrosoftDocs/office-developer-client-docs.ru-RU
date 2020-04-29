---
title: Каноническое свойство PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359901"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Каноническое свойство PidTagDelegateFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, может ли представитель просматривать частные объекты сообщений этого представителя.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Идентификатор:  <br/> |0x686B  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Определяемый классом Message передающей  <br/> |
   
## <a name="remarks"></a>Примечания

Каждой записи этого свойства должно быть присвоено одно из следующих значений.
  
|**Флаг**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|хидепривате  <br/> |нуль  <br/> |Представителю не следует разрешено просматривать объекты частных сообщений.  <br/> |
|шовпривате  <br/> |1,1  <br/> |Представителю следует разрешить просмотр частных объектов сообщений.  <br/> |
   
Это свойство должно быть задано в объекте сведений о делегате. Значение "Шовпривате" указывает на то, что делегирование хочет отобразить частные объекты сообщений. Этот параметр применяется ко всем папкам, для которых представитель имеет роль рецензента, автора или редактора.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.
    
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

