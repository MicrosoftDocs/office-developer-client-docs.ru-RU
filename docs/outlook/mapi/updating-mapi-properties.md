---
title: Обновление свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812539"
---
# <a name="updating-mapi-properties"></a>Обновление свойств MAPI

**Относится к**: Outlook 
  
Клиенты и поставщиков услуг можно обновить значение свойства, вызывая:
  
- Метод [IMAPIProp::SetProps](imapiprop-setprops.md) объекта обновление значения одного или нескольких свойств объекта. 
    
- Функция [HrSetOneProp](hrsetoneprop.md) для обновления только одно свойство за раз. Используйте **HrSetOneProp** только в том случае, если целевой объект является локальным; Эта функция может привести к снижению производительности при использовании с удаленных объектов. 
    
В следующей процедуре показано, как использовать **SetProps** для обновления класса сообщений или свойство PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), сообщения. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Чтобы обновить класс сообщения сообщения 
  
1. Выделите структуру [SPropValue](spropvalue.md) для класса сообщения и задать его члены соответствующим образом. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Вызовите метод **IMAPIProp::SetProps** сообщения, чтобы задать новый класс сообщения. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)

