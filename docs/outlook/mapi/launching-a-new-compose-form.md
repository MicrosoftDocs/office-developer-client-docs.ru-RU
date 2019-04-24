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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270058"
---
# <a name="launching-a-new-compose-form"></a><span data-ttu-id="ddab0-103">Запуск новой формы создания</span><span class="sxs-lookup"><span data-stu-id="ddab0-103">Launching a New Compose Form</span></span>

  
  
<span data-ttu-id="ddab0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ddab0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ddab0-105">При открытии приложением для создания нового сообщения с помощью средств реализации сервера форм необходимо ожидать приведенной ниже последовательности вызовов этих методов к серверу форм и объектам формы.</span><span class="sxs-lookup"><span data-stu-id="ddab0-105">Form server implementers should expect the following sequence of method calls to their form server and form objects when a client application opens a new message for composing:</span></span>
  
1. <span data-ttu-id="ddab0-106">Клиентское приложение вызывает метод [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для получения сведений о классе, посвященных классу сообщений сервера форм.</span><span class="sxs-lookup"><span data-stu-id="ddab0-106">The client application calls the [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) method to get class information about the form server's message class.</span></span> 
    
2. <span data-ttu-id="ddab0-107">Клиентское приложение вызывает метод [имапиформмгр:: креатеформ](imapiformmgr-createform.md) , чтобы получить новый объект Form.</span><span class="sxs-lookup"><span data-stu-id="ddab0-107">The client application calls [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) to get a new form object.</span></span> 
    
3. <span data-ttu-id="ddab0-108">Диспетчер форм MAPI загружает сервер форм, если он еще не находится в памяти, и получает интерфейс [имапиформ](imapiformiunknown.md) от сервера форм.</span><span class="sxs-lookup"><span data-stu-id="ddab0-108">The MAPI form manager loads the form server, if it is not already in memory, and gets an [IMAPIForm](imapiformiunknown.md) interface from the form server.</span></span> 
    
4. <span data-ttu-id="ddab0-109">Клиентское приложение получает полученный в результате интерфейс **имапиформ** и вызывает метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения интерфейса [иперсистмессаже](ipersistmessageiunknown.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="ddab0-109">The client application takes the resulting **IMAPIForm** interface and calls the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) method to get the object's [IPersistMessage](ipersistmessageiunknown.md) interface.</span></span> 
    
5. <span data-ttu-id="ddab0-110">Клиентское приложение вызывает метод [иперсистмессаже:: инитнев](ipersistmessage-initnew.md) , чтобы сопоставить объект формы с объектами [iMessage](imessageimapiprop.md), View контекста и приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ddab0-110">The client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) method to associate the form object with [IMessage](imessageimapiprop.md), view context, and advise sink objects.</span></span>
    
6. <span data-ttu-id="ddab0-111">Клиентское приложение вызывает метод [имапиформ::D оверб](imapiform-doverb.md) для вызова команды Open.</span><span class="sxs-lookup"><span data-stu-id="ddab0-111">The client application calls the [IMAPIForm::DoVerb](imapiform-doverb.md) method to invoke the open verb.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="ddab0-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ddab0-112">See also</span></span>



[<span data-ttu-id="ddab0-113">Взаимодействие с сервером форм</span><span class="sxs-lookup"><span data-stu-id="ddab0-113">Form Server Interactions</span></span>](form-server-interactions.md)

