---
title: Интерфейсы форм MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 611213c9-e758-4366-b193-fc62181d3d1f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f207f9550c61ad69fd1fc560cdb2084b7bb56c6f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412347"
---
# <a name="mapi-form-interfaces"></a>Интерфейсы форм MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI определяет следующие интерфейсы, относящиеся к формам.
  
|**Имя интерфейса**|**Описание**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Манипулирует объектами формы и обрабатывает команды объектов формы.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Определяет, может ли объект формы обрабатывать следующее сообщение и изменяет следующее или предыдущее состояние объекта формы.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Поддерживает установку, деинсталляцию и разрешение серверов форм в определенном контейнере форм.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Поддерживает использование настраиваемых серверов форм во время работы.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Позволяет клиентские приложения работать с свойствами, определенными для класса сообщений.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Позволяет клиентские приложения получать сведения о серверах форм, активировать серверы форм и устанавливать серверы форм в системе обмена сообщениями.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Используется для обработки сообщений, связанных с объектами форм.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Сообщает клиентские приложения о том, что событие произошло в объекте формы.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Используется для ответа на команды Next, Previous и Delete в объекте формы.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Используется для сохранения, инициализации и загрузки объектов формы в хранилище сообщений и из него.  <br/> |
   
Дополнительные сведения о методах интерфейсов форм MAPI см. в документации по этим интерфейсам. Чтобы создать настраиваемую форму, не нужно внедрять все интерфейсы форм MAPI. Сама форма требует только реализации интерфейсов **IPersistMessage,** **IMAPIForm** и **IMAPIFormAdviseSink.** Кроме того, это также хорошая идея для реализации **IMAPIFormFactory** и **IMAPIFormInfo**. **IMAPIFormFactory** полезен для соответствия требованиям OLE, а **IMAPIFormInfo** позволяет хорошо написанным клиентным приложениям лучше использовать ваши формы. 
  
> [!NOTE]
> Строго говоря, **IMAPIFormAdviseSink** является необязательным интерфейсом. Однако настоятельно рекомендуется реализовать его на серверах форм. Этот интерфейс имеет решающее значение для эффективного взаимодействия между клиентами обмена сообщениями и серверами форм, особенно когда рассматривается несколько сообщений класса сообщений сервера формы. 
  
## <a name="see-also"></a>См. также



[Формы MAPI](mapi-forms.md)

