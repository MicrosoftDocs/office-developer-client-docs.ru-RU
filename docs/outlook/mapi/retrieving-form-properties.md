---
title: Получение свойств формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a6636b6298fcf565a297ed5df8a885c43c279c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583850"
---
# <a name="retrieving-form-properties"></a>Получение свойств формы

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Для отправки запроса, который может применяться к типу настраиваемого сообщения, приложение должно знать свойства, которые должны быть на это сообщение. Чтобы получить список свойств, которые использует пользовательский класс сообщения, клиентское приложение запрашивает диспетчера формы MAPI. Диспетчер форм возвращает эту информацию из файла конфигурации соответствующую форму, чтобы клиентские приложения могут использовать эти сведения без затрат активации самого сервера формы. Для этого клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Обратите внимание, что третий аргумент **ResolveMessageClass** к папке, содержащей таблицу связанного содержимого, запрос выполняет поиск серверов формы. Значение NULL означает, что диспетчер форм должна выполнять все доступные формы контейнеров. Если запрос будет выполняться для определенной папки, рекомендуется включить соответствующую указатель [IMAPIFolder](imapifolderimapicontainer.md) вместо этого. 
  
## <a name="see-also"></a>См. также



[Взаимодействие серверов форм](form-server-interactions.md)

