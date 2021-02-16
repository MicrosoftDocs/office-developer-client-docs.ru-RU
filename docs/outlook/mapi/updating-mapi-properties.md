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
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407524"
---
# <a name="updating-mapi-properties"></a>Обновление свойств MAPI

**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты и поставщики услуг могут обновлять значение свойства, вызывая:
  
- Метод [IMAPIProp::SetProps](imapiprop-setprops.md) объекта для обновления значения одного или более свойств объекта. 
    
- Функция [HrSetOneProp](hrsetoneprop.md) для одновременного обновления только одного свойства. Используйте **HrSetOneProp только** в том случае, если целевой объект является локальным; Эта функция может привести к снижению производительности при работе с удаленными объектами. 
    
В следующей процедуре показано, как использовать **SetProps** для обновления класса сообщения или PR_MESSAGE_CLASS_A ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)сообщения. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Обновление класса сообщения 
  
1. Выделите [структуру SPropValue](spropvalue.md) для класса сообщений и установите соответствующие члены. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. Вызовите метод **IMAPIProp::SetProps** сообщения, чтобы установить новый класс сообщения. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)

