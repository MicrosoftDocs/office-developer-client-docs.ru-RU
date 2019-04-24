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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360517"
---
# <a name="updating-mapi-properties"></a>Обновление свойств MAPI

**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты и поставщики услуг могут обновлять значение свойства с помощью вызова:
  
- Метод объекта [IMAPIProp:: SetProps](imapiprop-setprops.md) для обновления значения одного или нескольких свойств объекта. 
    
- Функция [хрсетонепроп](hrsetoneprop.md) для обновления только одного свойства за раз. Используйте **хрсетонепроп** только в том случае, если целевой объект является локальным; Эта функция может привести к ухудшению производительности при использовании с удаленными объектами. 
    
В следующей процедуре показано, как использовать **SetProps** для обновления класса Message или свойства Пр_мессаже_класс_а ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения. 
  
### <a name="to-update-the-message-class-of-a-message"></a>Обновление класса сообщения сообщения 
  
1. Выделить структуру [спропвалуе](spropvalue.md) для класса сообщений и присвоить ей соответствующие элементы. 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. ВыЗовите метод сообщения **IMAPIProp:: SetProps** , чтобы задать новый класс сообщения. 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a>См. также

- [Обзор свойств MAPI](mapi-property-overview.md)

