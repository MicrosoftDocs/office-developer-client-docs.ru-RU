---
title: Каноническое свойство PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 22d3e649641dbe688912ecece7fde73a555f4a88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361098"
---
# <a name="pidtagattachrendering-canonical-property"></a>Каноническое свойство PidTagAttachRendering

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит метафиль microsoft Windows с отрисовкой сведений для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Идентификатор:  <br/> |0x3709  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Целью этого свойства является предоставление значка или другого изображения, которое может отображаться в родительском сообщении в точке вложения. Такое представление обычно включает имя вложения, если таковые имеются, и характер вложения, например документ Microsoft Office Word. Клиентская заявка может использовать это представление на дисплее сообщения. 
  
Для присоединенного файла это свойство обычно отображает значок для файла. 
  
Для прикрепленного сообщения это свойство обычно не заданной. Клиентский приложение, нуждающийся в отрисовке прикрепленного **сообщения,** должно получить свойство PR_MESSAGE_CLASS [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md)вызвать [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для указателя на соответствующий информационный объект формы, открыть интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) на этом объекте и использовать **GetProps** для получения свойства **PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)или PR_MINI_ICON [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md)  
  
Для встроенного статического объекта OLE это свойство содержит метафиль microsoft Windows, который можно использовать для нарисовки представления вложений в окне. 
  
Для встроенного динамического объекта OLE клиент должен использовать данные OLE для создания данных отрисовки. 
  
Во всех случаях клиентские приложения должны знать, что это свойство обычно имеет размер в несколько сотен bytes и подлежит truncation в таблице вложений. Если клиент хочет отрисовки вложения из этого свойства, не открывая само вложение, он должен работать в правиле обрезки таблицы. Дополнительные сведения см. в [статье Работа с большими столбцами.](working-with-large-columns.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

