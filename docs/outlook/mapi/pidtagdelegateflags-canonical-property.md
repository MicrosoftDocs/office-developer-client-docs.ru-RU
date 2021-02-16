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
  
Указывает, может ли делегат просматривать объекты частных сообщений делегатора.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Идентификатор:  <br/> |0x686B  <br/> |
|Тип данных:  <br/> |PT_MV_LONG  <br/> |
|Область:  <br/> |Передача сообщений, определенных классом  <br/> |
   
## <a name="remarks"></a>Примечания

Для каждой записи этого свойства должно быть установлено одно из следующих значений.
  
|**Flag**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Делегату не должно быть разрешено просматривать частные объекты сообщений.  <br/> |
|ShowPrivate  <br/> |1   <br/> |Делегату должно быть разрешено просматривать частные объекты сообщений.  <br/> |
   
Это свойство должно быть установлено в объекте делегирования информации. Значение ShowPrivate указывает, что делегатор хочет сделать объекты частных сообщений видимыми. Этот параметр применим для всех папок, для которых делегат имеет роль рецензента, автора или редактора.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.
    
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

