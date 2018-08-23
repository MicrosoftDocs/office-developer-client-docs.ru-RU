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
ms.openlocfilehash: 172abe64073b11d98bfb5f76999237218ef8944a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581351"
---
# <a name="updating-mapi-properties"></a>Обновление свойств MAPI

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

