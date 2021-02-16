---
title: Каноническое свойство PidTagBody
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBody
api_type:
- HeaderDef
ms.assetid: 47c0d0fe-4d57-4b81-bdb5-336de85c194c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 243a59798980d8c0cfaf1a726d6408dbd66ebba8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326637"
---
# <a name="pidtagbody-canonical-property"></a>Каноническое свойство PidTagBody

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит текст сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_BODY, PR_BODY_A, PR_BODY_W  <br/> |
|Идентификатор:  <br/> |0x1000  <br/> |
|Тип данных:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства обычно используются только в межличном сообщении (IPM). 
  
В хранилищах сообщений, поддерживаюх формат RTF, игнорируются изменения, внесенные в пробелы в тексте сообщения. Когда **PR_BODY** сохраняется в первый раз, хранилище сообщений также создает и сохраняет свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)— версию текста сообщения в RTF. Если метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) впоследствии вызывается и **PR_BODY** был изменен, хранилище сообщений вызывает функцию [RTFSync,](rtfsync.md) чтобы обеспечить синхронизацию с версией RTF. Если изменено только пробел, свойства остаются без изменений. При этом сохраняются все нетривиальные форматы RTF при передаче сообщения через клиенты и системы обмена сообщениями, не сохраняющие RTF. 
  
Значение этого свойства должно быть выражено на странице кода операционной системы, в которую запущен MAPI. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

