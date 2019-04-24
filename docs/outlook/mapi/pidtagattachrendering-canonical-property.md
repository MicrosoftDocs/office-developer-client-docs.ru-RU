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
  
Содержит метафайл Microsoft Windows с отображением сведений о вложении. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АТТАЧ_РЕНДЕРИНГ  <br/> |
|Идентификатор:  <br/> |0x3709  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предназначено для предоставления значка или другого представления пикториал, которое может отображаться в родительском сообщении в точке вложения. Как правило, такое представление включает имя вложения, если оно есть, и характер вложения, например документ Microsoft Office Word. Клиентское приложение может использовать это представление в отображении сообщения. 
  
Для вложенного файла это свойство обычно портрайс значок для файла. 
  
Для вложенного сообщения это свойство обычно не задается. Клиентскому приложению, необходимому для отображения вложенного сообщения, необходимо получить его свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), вызовите [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для указателя на соответствующий объект сведений о форме. Откройте интерфейс [имапиформинфо](imapiforminfoimapiprop.md) для этого объекта и используйте свойства- **PROPS** для получения свойства **Пр_икон** ([PidTagIcon](pidtagicon-canonical-property.md)) или **пр_мини_икон** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Для внедренного статического объекта OLE это свойство содержит метафайл Microsoft Windows, который можно использовать для рисования представления вложений в окне. 
  
Для внедренного динамического объекта OLE клиент должен использовать данные OLE для создания данных отображения. 
  
Во всех случаях клиентское приложение должно знать о том, что это свойство обычно имеет размер не более ста байт и может быть усечено в таблице вложений. Если клиент хочет отобразить вложение из этого свойства, не открывая само вложение, оно должно работать в рамках правила усечения таблицы. Более подробную информацию можно узнать [в статье работа с большими столбцами](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

