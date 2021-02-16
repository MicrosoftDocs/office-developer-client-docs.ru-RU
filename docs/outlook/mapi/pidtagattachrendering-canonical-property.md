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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит метафикс Microsoft Windows с информацией об отображении вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Идентификатор:  <br/> |0x3709  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предназначено для предоставления значка или другого изображения, которое может отображаться в родительском сообщении в точке вложения. Такое представление обычно включает имя вложения ,если таковой имеется, и характер вложения, например Microsoft Office Word. Клиентские приложения могут использовать это представление для отображения сообщения. 
  
Для вложенного файла это свойство обычно является значком для файла. 
  
Для вложенного сообщения это свойство обычно не за установлено. Клиентский приложение, которое должно отрисовывать вложенное сообщение, должно получить свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md)вызвать [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для указателя на соответствующий объект сведений формы, открыть интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) для этого объекта и использовать **GetProps** для получения свойства **PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)или **PR_MINI_ICON** ([PidTagMiniIcon).](pidtagminiicon-canonical-property.md) 
  
Для внедренного статического объекта OLE это свойство содержит метафикс Microsoft Windows, который можно использовать для отрисовки представления вложения в окне. 
  
Для внедренного динамического объекта OLE клиент должен использовать данные OLE для создания сведений об отрисовке. 
  
Во всех случаях клиентские приложения должны знать, что это свойство обычно имеет размер в несколько сотен bytes и подвергается урезке в таблице вложений. Если клиент хочет отрисовать вложение из этого свойства, не открывая само вложение, оно должно работать в правиле уселения таблицы. Дополнительные сведения см. [в статье "Работа с большими столбцами".](working-with-large-columns.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

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

