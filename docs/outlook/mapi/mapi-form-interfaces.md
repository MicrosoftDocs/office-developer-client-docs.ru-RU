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
ms.openlocfilehash: 8452a6e49059dd0912f1efffef7e749afd6cdf6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809735"
---
# <a name="mapi-form-interfaces"></a>Интерфейсы форм MAPI

  
  
**Относится к**: Outlook 
  
MAPI определяет следующие интерфейсы, связанные с форм.
  
|**Имя интерфейса**|**Описание**|
|:-----|:-----|
|[IMAPIForm](imapiformiunknown.md) <br/> |Управляет объектам формы и обработка команд объекта формы.  <br/> |
|[IMAPIFormAdviseSink](imapiformadvisesinkiunknown.md) <br/> |Определяет может обрабатывать следующего сообщения и изменяет состояние следующий или предыдущий объект формы, объекта формы.  <br/> |
|[IMAPIFormContainer](imapiformcontaineriunknown.md) <br/> |Поддерживает установку, deinstallation и разрешение серверов формы с контейнером конкретной формы.  <br/> |
|[IMAPIFormFactory](imapiformfactoryiunknown.md) <br/> |Поддерживает использование серверов настраиваемые формы во время выполнения.  <br/> |
|[IMAPIFormInfo](imapiforminfoimapiprop.md) <br/> |Позволяет клиентским приложениям для работы со свойствами, которые специфичны для класса сообщения.  <br/> |
|[IMAPIFormMgr](imapiformmgriunknown.md) <br/> |Позволяет клиентским приложениям для получения сведений о форме серверы, активирует серверы формы и устанавливает серверы формы в системе обмена сообщениями.  <br/> |
|[IMAPIMessageSite](imapimessagesiteiunknown.md) <br/> |Используется для работы с сообщений, связанных с объектами формы.  <br/> |
|[IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) <br/> |Уведомляет клиентские приложения, которые в объекте формы возникновении события.  <br/> |
|[IMAPIViewContext](imapiviewcontextiunknown.md) <br/> |Использовать реагировать на Далее, назад и удаление команд в объекте формы.  <br/> |
|[IPersistMessage](ipersistmessageiunknown.md) <br/> |Служит для сохранения, инициализации и загрузки объектов формы между хранение сообщений.  <br/> |
   
Дополнительные сведения о методах интерфейсы формы MAPI документации для этих интерфейсов. Необходимо реализовать все интерфейсы формы MAPI для создания настраиваемых форм. Форма самого требует только реализовать **IPersistMessage**, **IMAPIForm**и **IMAPIFormAdviseSink** интерфейсы. Кроме того рекомендуется также реализовать **IMAPIFormFactory** и **IMAPIFormInfo**. **IMAPIFormFactory** полезен для соответствия требованиям OLE и **IMAPIFormInfo** позволяет хорошо написанных клиентских приложений лучше использовать формы. 
  
> [!NOTE]
> Строго сферой **IMAPIFormAdviseSink** — это необязательный интерфейс. Тем не менее настоятельно рекомендуется реализовать в форме серверы. Этот интерфейс важно эффективное взаимодействие между обмена сообщениями клиентов и серверов форм, особенно если несколько сообщений сервера форм класс сообщения обрабатывают. 
  
## <a name="see-also"></a>См. также



[Формы MAPI](mapi-forms.md)

