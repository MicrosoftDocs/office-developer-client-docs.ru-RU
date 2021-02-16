---
title: Искомые свойства формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412921"
---
# <a name="retrieving-form-properties"></a>Искомые свойства формы

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы отправить запрос, значимый для настраиваемого типа сообщений, приложению необходимо знать свойства, которые ожидаются в этом сообщении. Чтобы получить список свойств, которые использует настраиваемый класс сообщений, клиентские приложения запрашивают диспетчер форм MAPI. Диспетчер форм получает эти сведения из соответствующего файла конфигурации формы, чтобы клиентские приложения могли использовать эти сведения без накладных расходов на активацию самого сервера форм. Для этого клиентские приложения вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) следующим образом: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Обратите внимание, что третий аргумент **ResolveMessageClass** — это папка, которая содержит связанную таблицу содержимого, которую запрос будет искать на серверах форм. NULL указывает, что диспетчер форм должен искать все доступные контейнеры форм. Если запрос нужно выполнить для определенной папки, лучше включить соответствующий [указатель IMAPIFolder.](imapifolderimapicontainer.md) 
  
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

