---
title: Каноническое свойство PidTagUrlComponentName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUrlComponentName
api_type:
- COM
ms.assetid: a21906f9-5408-41ba-a89b-273ab60eeef3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 26a9d432d98c546aefa8f511ba2c4c9bb26cfd80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320428"
---
# <a name="pidtagurlcomponentname-canonical-property"></a>Каноническое свойство PidTagUrlComponentName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Имя компонента URL-адреса для сообщения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_URL_COMP_NAME, PR_URL_COMP_NAME_A, PR_URL_COMP_NAME_W  <br/> |
|Идентификатор:  <br/> |0x10F3  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства должны быть уникальными в папке. Если не установлено, когда сообщение создано, хранилище сообщений должно устанавливать эти свойства на основе различных свойств сообщения в зависимости от класса сообщения. Например, **IPM. Примечание** и **IPM. Для** сообщений о встречах этот набор свойств должен быть заданной на основе свойства **PR_SUBJECT** [(PidTagSubject)](pidtagsubject-canonical-property.md)и **IPM. Для** контактных сообщений этот набор свойств должен быть заданной на основе свойства **dispidFileUnder** ([PidLidFileUnder).](pidlidfileunder-canonical-property.md) Для большинства других классов сообщений это свойство должно быть основано на свойстве **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
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

