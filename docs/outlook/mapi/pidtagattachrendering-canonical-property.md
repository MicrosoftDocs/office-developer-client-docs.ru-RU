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
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810870"
---
# <a name="pidtagattachrendering-canonical-property"></a>Каноническое свойство PidTagAttachRendering

  
  
**Относится к**: Outlook 
  
Содержит метафайлов Microsoft Windows с сведения о визуализации для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_RENDERING  <br/> |
|Идентификатор:  <br/> |0x3709  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство предназначено для предоставления значок или другие графические представление, которое может отображаться в сообщении родительского точке вложения. Такое представление обычно включает в себя, имя вложения, при их наличии и характер вложения, такие как документ Microsoft Office Word. Клиентское приложение может использовать это представление в окне сообщения. 
  
Для вложенного файла это свойство обычно показан переключатель, относящийся значка для файла. 
  
Вложенные сообщения это свойство обычно не задается. Клиентское приложение для отображения вложенное сообщение должны получить его свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), вызовите [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для указателя соответствующего объекта данные формы Откройте интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) для этого объекта и используйте **GetProps** , чтобы получить **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) или свойство **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Для статических внедренный объект OLE это свойство содержит метафайл Microsoft Windows, который можно использовать для рисования представление вложения в окне. 
  
Для динамического внедренный объект OLE клиент должен использовать данные OLE для создания отображения сведений. 
  
Во всех случаях клиентское приложение следует иметь в виду, что это свойство обычно является нескольких сотен байтов по размеру и может быть усечения в таблице вложений. Если необходимо отображать вложения из этого свойства без открытия самого вложение клиента, работы в рамках правила усечения таблицы. Для получения дополнительных сведений см [большой](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

