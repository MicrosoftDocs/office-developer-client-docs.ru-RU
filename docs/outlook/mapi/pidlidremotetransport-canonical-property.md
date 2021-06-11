---
title: Каноническое свойство PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439445"
---
# <a name="pidlidremotetransport-canonical-property"></a>Каноническое свойство PidLidRemoteTransport

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет, с какой учетной записью связан элемент загона, в первую очередь для реализации функции POP Leave on Server. 
  
|||
|:-----|:-----|
|Связанные свойства  <br/> |dispidRemoteXP  <br/> |
|Набор свойств:  <br/> |PSETID_Remote  <br/> |
|Long ID (LID):  <br/> |0x00008F03  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Удаленное сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство актуально только для сообщений, которые имеют класс сообщений IPM. Удаленный. Корпорация Outlook сохраняет сопоставление различных учетных записей, скачиваемых в данный магазин, в сообщении о связанных с папками сведениях (FAI), но может также хранить эти сведения в реестре.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]] 
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

