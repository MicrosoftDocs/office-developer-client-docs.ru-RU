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
ms.openlocfilehash: 87299ce4335492a744dd4ee965b4f8b85bcedc84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564894"
---
# <a name="launching-a-form-server"></a><span data-ttu-id="d0af5-103">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="d0af5-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="d0af5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0af5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0af5-105">Последовательность взаимодействия, которая происходит при загрузке формы из постоянного хранилища (то есть, из библиотеки форм) для отображения сообщения выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d0af5-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="d0af5-106">Клиент обмена мгновенными сообщениями получает класс сообщения сообщения, отметки сообщений и состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0af5-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="d0af5-107">Этот шаг является необязательным; Если эти элемента данных не указан на шаге 2, диспетчер форм будут их восстановить.</span><span class="sxs-lookup"><span data-stu-id="d0af5-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="d0af5-108">Клиент обмена мгновенными сообщениями вызывает [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) с сообщением целевой.</span><span class="sxs-lookup"><span data-stu-id="d0af5-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="d0af5-109">Диспетчер форм загружает сервера форм из библиотеки соответствующих свойств.</span><span class="sxs-lookup"><span data-stu-id="d0af5-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="d0af5-110">Если сервер формы в качестве целевого сообщения не установлен, диспетчер форм устанавливает формы исполняемые файлы, а также.</span><span class="sxs-lookup"><span data-stu-id="d0af5-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="d0af5-111">Диспетчер форм вызывает [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для объекта формы для получения объекта формы [IMAPIForm: IUnknown](imapiformiunknown.md) и [IPersistMessage: IUnknown](ipersistmessageiunknown.md) интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d0af5-111">The form manager calls [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="d0af5-112">Диспетчер форм вызывает [IPersistMessage::Load](ipersistmessage-load.md) с сообщением интерфейсы сайта и сообщения из объекта средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="d0af5-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="d0af5-113">Объект формы обратный вызов метода [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d0af5-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="d0af5-114">Диспетчер формы вызывает метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) объекта формы с помощью интерфейса контекст представления из клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d0af5-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="d0af5-115">Объект формы обратный вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d0af5-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="d0af5-116">Объект формы обратный вызов метода [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d0af5-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="d0af5-117">Обмена сообщениями клиент вызывает метод [IMAPIForm::Advise](imapiform-advise.md) объекта формы с представлением интерфейсы контекста из средства просмотра и объектов сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="d0af5-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="d0af5-118">Обмена сообщениями клиент вызывает метод [IMAPIForm::DoVerb](imapiform-doverb.md) объекта формы.</span><span class="sxs-lookup"><span data-stu-id="d0af5-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="d0af5-119">Объект формы при необходимости создает его пользовательский интерфейс и взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="d0af5-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0af5-120">См. также</span><span class="sxs-lookup"><span data-stu-id="d0af5-120">See also</span></span>



[<span data-ttu-id="d0af5-121">Взаимодействие серверов форм</span><span class="sxs-lookup"><span data-stu-id="d0af5-121">Form Server Interactions</span></span>](form-server-interactions.md)

