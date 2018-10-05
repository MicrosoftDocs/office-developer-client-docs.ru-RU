---
title: Запуск сервера форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: dec8706ba00356660ec82c25e0213ef3e638691d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387729"
---
# <a name="launching-a-form-server"></a>Запуск сервера форм

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Последовательность взаимодействия, которая происходит при загрузке формы из постоянного хранилища (то есть, из библиотеки форм) для отображения сообщения выглядит следующим образом:
  
1. Клиент обмена мгновенными сообщениями получает класс сообщения сообщения, отметки сообщений и состояние сообщения. Этот шаг является необязательным; Если эти элемента данных не указан на шаге 2, диспетчер форм будут их восстановить.
    
2. Клиент обмена мгновенными сообщениями вызывает [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) с сообщением целевой. 
    
3. Диспетчер форм загружает сервера форм из библиотеки соответствующих свойств. Если сервер формы в качестве целевого сообщения не установлен, диспетчер форм устанавливает формы исполняемые файлы, а также.
    
4. Диспетчер форм вызывает [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для объекта формы для получения объекта формы [IMAPIForm: IUnknown](imapiformiunknown.md) и [IPersistMessage: IUnknown](ipersistmessageiunknown.md) интерфейсов. 
    
5. Диспетчер форм вызывает [IPersistMessage::Load](ipersistmessage-load.md) с сообщением интерфейсы сайта и сообщения из объекта средства просмотра. 
    
6. Объект формы обратный вызов метода [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) клиента обмена сообщениями. 
    
7. Диспетчер формы вызывает метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) объекта формы с помощью интерфейса контекст представления из клиента обмена сообщениями. 
    
8. Объект формы обратный вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) клиента обмена сообщениями. 
    
9. Объект формы обратный вызов метода [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) клиента обмена сообщениями. 
    
10. Обмена сообщениями клиент вызывает метод [IMAPIForm::Advise](imapiform-advise.md) объекта формы с представлением интерфейсы контекста из средства просмотра и объектов сайта сообщения. 
    
11. Обмена сообщениями клиент вызывает метод [IMAPIForm::DoVerb](imapiform-doverb.md) объекта формы. 
    
12. Объект формы при необходимости создает его пользовательский интерфейс и взаимодействие с пользователем.
    
## <a name="see-also"></a>См. также



[Взаимодействие серверов форм](form-server-interactions.md)

