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
ms.openlocfilehash: 160ddc53edf3d9681adf6f9d536a488c0c345a07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811042"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Каноническое свойство PidTagDelegateFlags

  
  
**Относится к**: Outlook 
  
Указывает ли делегата можно просматривать объекты представитель личное сообщение.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Идентификатор:  <br/> |0x686B  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Сообщение, определенное класс передаваемого  <br/> |
   
## <a name="remarks"></a>Замечания

Каждая запись этого свойства необходимо установить одно из следующих значений.
  
|**Flag**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Делегат не должны просматривать объекты личное сообщение.  <br/> |
|ShowPrivate  <br/> |1  <br/> |Делегат должны просматривать объекты личное сообщение.  <br/> |
   
Это свойство необходимо установить в объекте сведения делегата. Значение «ShowPrivate» указывает, что представитель сделайте видимым объекты личное сообщение. Этот параметр применяется ко всем папкам, для которых делегат имеет роль проверяющего, автор или редактора.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

