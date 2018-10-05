---
title: Запуск новой формы создания
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391775"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="9a26a-103">Запуск новой формы создания</span><span class="sxs-lookup"><span data-stu-id="9a26a-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="9a26a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a26a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a26a-105">Специалистов по внедрению сервера форм следует ожидать следующую последовательность вызовов к серверу формы и объекты формы при клиентского приложения откроется новое сообщение для составления:</span><span class="sxs-lookup"><span data-stu-id="9a26a-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="9a26a-106">Клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения класса сведений о класс сообщения сервера форм.</span><span class="sxs-lookup"><span data-stu-id="9a26a-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="9a26a-107">Клиентское приложение вызывает [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) для получения объекта формы.</span><span class="sxs-lookup"><span data-stu-id="9a26a-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="9a26a-108">Диспетчер формы MAPI загружает на сервере формы, если он еще не в памяти и получает интерфейс [IMAPIForm](imapiformiunknown.md) с сервера формы.</span><span class="sxs-lookup"><span data-stu-id="9a26a-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="9a26a-109">Клиентское приложение принимает итоговый интерфейс **IMAPIForm** и вызывает метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения объекта [IPersistMessage](ipersistmessageiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9a26a-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="9a26a-110">Клиентское приложение вызывает метод [IPersistMessage::InitNew](ipersistmessage-initnew.md) для связывания объекта формы с [IMessage](imessageimapiprop.md), контекст представления и уведомить объектов приемника.</span><span class="sxs-lookup"><span data-stu-id="9a26a-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="9a26a-111">Клиентское приложение вызывает метод [IMAPIForm::DoVerb](imapiform-doverb.md) для вызова open команды.</span><span class="sxs-lookup"><span data-stu-id="9a26a-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9a26a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="9a26a-112">See also</span></span>



[<span data-ttu-id="9a26a-113">Взаимодействие серверов форм</span><span class="sxs-lookup"><span data-stu-id="9a26a-113">Form Server Interactions</span></span>](form-server-interactions.md)

