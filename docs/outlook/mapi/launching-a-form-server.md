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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270051"
---
# <a name="launching-a-form-server"></a>Запуск сервера форм

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Серия взаимодействий, которые возникают при загрузке формы из постоянного хранилища (то есть из библиотеки форм) для отображения сообщения:
  
1. Клиент обмена сообщениями получает класс сообщения, флаги сообщений и состояние сообщения. Этот шаг необязателен; Если эти фрагменты данных не будут предоставлены на шаге 2, руководитель форм будет извлекать их.
    
2. Клиент обмена сообщениями вызывает [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) с целевым сообщением. 
    
3. Диспетчер форм загружает сервер форм из соответствующей библиотеки форм. Если сервер формы для целевого сообщения не установлен, диспетчер форм устанавливает исполняемые файлы формы.
    
4. Руководитель формы вызывает [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) на объект формы, чтобы получить [IMAPIForm объекта формы: IUnknown](imapiformiunknown.md) и [IPersistMessage: интерфейсы IUnknown.](ipersistmessageiunknown.md) 
    
5. Руководитель формы вызывает [IPersistMessage:::Load](ipersistmessage-load.md) с веб-сайтом сообщений и интерфейсами сообщений из объекта просмотра. 
    
6. Объект формы возвращается к методу [IMAPIMessageSite::GetSiteStatus.](imapimessagesite-getsitestatus.md) 
    
7. Менеджер формы вызывает метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) объекта формы с интерфейсом контекста представления от клиента обмена сообщениями. 
    
8. Объект формы возвращается к методу [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) клиента обмена сообщениями. 
    
9. Объект формы возвращается к методу [IMAPIViewContext::GetViewStatus клиента](imapiviewcontext-getviewstatus.md) обмена сообщениями. 
    
10. Клиент обмена сообщениями вызывает метод [IMAPIForm:::Advise](imapiform-advise.md) объекта формы с интерфейсами контекста представления из объекта просмотра и объекта сайта сообщения. 
    
11. Клиент обмена сообщениями вызывает метод [IMAPIForm::D oVerb](imapiform-doverb.md) объекта формы. 
    
12. Объект формы создает пользовательский интерфейс при необходимости и взаимодействует с пользователем.
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

