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
ms.openlocfilehash: 334ecaacec88c3730f4cc2f4c80eb35d5a553c4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812155"
---
# <a name="retrieving-form-properties"></a>Получение свойств формы

  
  
**Относится к**: Outlook 
  
Для отправки запроса, который может применяться к типу настраиваемого сообщения, приложение должно знать свойства, которые должны быть на это сообщение. Чтобы получить список свойств, которые использует пользовательский класс сообщения, клиентское приложение запрашивает диспетчера формы MAPI. Диспетчер форм возвращает эту информацию из файла конфигурации соответствующую форму, чтобы клиентские приложения могут использовать эти сведения без затрат активации самого сервера формы. Для этого клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Обратите внимание, что третий аргумент **ResolveMessageClass** к папке, содержащей таблицу связанного содержимого, запрос выполняет поиск серверов формы. Значение NULL означает, что диспетчер форм должна выполнять все доступные формы контейнеров. Если запрос будет выполняться для определенной папки, рекомендуется включить соответствующую указатель [IMAPIFolder](imapifolderimapicontainer.md) вместо этого. 
  
## <a name="see-also"></a>См. также



[Взаимодействие серверов форм](form-server-interactions.md)

