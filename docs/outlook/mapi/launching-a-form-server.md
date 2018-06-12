---
title: Запуск сервера форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a439e75a-92b3-4830-9dfc-e723d046be7b
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: c70fd9eb771268db4030cefdf2f27b75ae5963b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809650"
---
# <a name="launching-a-form-server"></a>Запуск сервера форм

  
  
**Применимо к**: Outlook 
  
Последовательность взаимодействия, которая происходит при загрузке формы из постоянного хранилища (то есть, из библиотеки форм) для отображения сообщения выглядит следующим образом:
  
1. Клиент обмена мгновенными сообщениями получает класс сообщения сообщения, отметки сообщений и состояние сообщения. Этот шаг является необязательным; Если эти элемента данных не указан на шаге 2, диспетчер форм будут их восстановить.
    
2. Клиент обмена мгновенными сообщениями вызывает [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) с сообщением целевой. 
    
3. Диспетчер форм загружает сервера форм из библиотеки соответствующих свойств. Если сервер формы в качестве целевого сообщения не установлен, диспетчер форм устанавливает формы исполняемые файлы, а также.
    
4. Диспетчер форм вызывает [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для объекта формы для получения объекта формы [IMAPIForm: IUnknown](imapiformiunknown.md) и [IPersistMessage: IUnknown](ipersistmessageiunknown.md) интерфейсов. 
    
5. Диспетчер форм вызывает [IPersistMessage::Load](ipersistmessage-load.md) с сообщением интерфейсы сайта и сообщения из объекта средства просмотра. 
    
6. Объект формы обратный вызов метода [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) клиента обмена сообщениями. 
    
7. Диспетчер формы вызывает метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) объекта формы с помощью интерфейса контекст представления из клиента обмена сообщениями. 
    
8. Объект формы обратный вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) клиента обмена сообщениями. 
    
9. Объект формы обратный вызов метода [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) клиента обмена сообщениями. 
    
10. Обмена сообщениями клиент вызывает метод [IMAPIForm::Advise](imapiform-advise.md) объекта формы с представлением интерфейсы контекста из средства просмотра и объектов сайта сообщения. 
    
11. Обмена сообщениями клиент вызывает метод [IMAPIForm::DoVerb](imapiform-doverb.md) объекта формы. 
    
12. Объект формы при необходимости создает его пользовательский интерфейс и взаимодействие с пользователем.
    
## <a name="see-also"></a>См. также



[Взаимодействие сервера формы](form-server-interactions.md)

