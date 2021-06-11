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
# <a name="launching-a-form-server"></a><span data-ttu-id="1f464-103">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="1f464-103">Launching a Form Server</span></span>

  
  
<span data-ttu-id="1f464-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f464-105">Серия взаимодействий, которые возникают при загрузке формы из постоянного хранилища (то есть из библиотеки форм) для отображения сообщения:</span><span class="sxs-lookup"><span data-stu-id="1f464-105">The series of interactions that occurs when a form is loaded from persistent storage (that is, from a form library) to display a message is as follows:</span></span>
  
1. <span data-ttu-id="1f464-106">Клиент обмена сообщениями получает класс сообщения, флаги сообщений и состояние сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f464-106">The messaging client gets the message's message class, message flags, and message status.</span></span> <span data-ttu-id="1f464-107">Этот шаг необязателен; Если эти фрагменты данных не будут предоставлены на шаге 2, руководитель форм будет извлекать их.</span><span class="sxs-lookup"><span data-stu-id="1f464-107">This step is optional; if these pieces of data are not provided in step 2, the form manager will retrieve them.</span></span>
    
2. <span data-ttu-id="1f464-108">Клиент обмена сообщениями вызывает [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) с целевым сообщением.</span><span class="sxs-lookup"><span data-stu-id="1f464-108">The messaging client calls [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) with the target message.</span></span> 
    
3. <span data-ttu-id="1f464-109">Диспетчер форм загружает сервер форм из соответствующей библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="1f464-109">The form manager loads the form server from the appropriate form library.</span></span> <span data-ttu-id="1f464-110">Если сервер формы для целевого сообщения не установлен, диспетчер форм устанавливает исполняемые файлы формы.</span><span class="sxs-lookup"><span data-stu-id="1f464-110">If the form server for the target message is not installed, the form manager installs the form's executable files, as well.</span></span>
    
4. <span data-ttu-id="1f464-111">Руководитель формы вызывает [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) на объект формы, чтобы получить [IMAPIForm объекта формы: IUnknown](imapiformiunknown.md) и [IPersistMessage: интерфейсы IUnknown.](ipersistmessageiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="1f464-111">The form manager calls [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) on the form object to obtain the form object's [IMAPIForm : IUnknown](imapiformiunknown.md) and [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interfaces.</span></span> 
    
5. <span data-ttu-id="1f464-112">Руководитель формы вызывает [IPersistMessage:::Load](ipersistmessage-load.md) с веб-сайтом сообщений и интерфейсами сообщений из объекта просмотра.</span><span class="sxs-lookup"><span data-stu-id="1f464-112">The form manager calls [IPersistMessage::Load](ipersistmessage-load.md) with the message site and message interfaces from the viewer object.</span></span> 
    
6. <span data-ttu-id="1f464-113">Объект формы возвращается к методу [IMAPIMessageSite::GetSiteStatus.](imapimessagesite-getsitestatus.md)</span><span class="sxs-lookup"><span data-stu-id="1f464-113">The form object calls back to the messaging client's [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md) method.</span></span> 
    
7. <span data-ttu-id="1f464-114">Менеджер формы вызывает метод [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) объекта формы с интерфейсом контекста представления от клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1f464-114">The form manager calls the form object's [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method with the view context interface from the messaging client.</span></span> 
    
8. <span data-ttu-id="1f464-115">Объект формы возвращается к методу [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) клиента обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1f464-115">The form object calls back to the messaging client's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method.</span></span> 
    
9. <span data-ttu-id="1f464-116">Объект формы возвращается к методу [IMAPIViewContext::GetViewStatus клиента](imapiviewcontext-getviewstatus.md) обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1f464-116">The form object calls back to the messaging client's [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method.</span></span> 
    
10. <span data-ttu-id="1f464-117">Клиент обмена сообщениями вызывает метод [IMAPIForm:::Advise](imapiform-advise.md) объекта формы с интерфейсами контекста представления из объекта просмотра и объекта сайта сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f464-117">The messaging client calls the form object's [IMAPIForm::Advise](imapiform-advise.md) method with the view context interfaces from the viewer object and the message site object.</span></span> 
    
11. <span data-ttu-id="1f464-118">Клиент обмена сообщениями вызывает метод [IMAPIForm::D oVerb](imapiform-doverb.md) объекта формы.</span><span class="sxs-lookup"><span data-stu-id="1f464-118">The messaging client calls the form object's [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> 
    
12. <span data-ttu-id="1f464-119">Объект формы создает пользовательский интерфейс при необходимости и взаимодействует с пользователем.</span><span class="sxs-lookup"><span data-stu-id="1f464-119">The form object creates its user interface, if necessary, and interacts with the user.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f464-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1f464-120">See also</span></span>



[<span data-ttu-id="1f464-121">Взаимодействие с сервером форм</span><span class="sxs-lookup"><span data-stu-id="1f464-121">Form Server Interactions</span></span>](form-server-interactions.md)

