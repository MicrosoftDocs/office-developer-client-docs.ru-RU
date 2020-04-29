---
title: Вызов MAPI из служб Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a606b8bf82ce4c06c8e55f6e4df94220bc67501d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318109"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="c4fa5-103">Вызов MAPI из служб Windows</span><span class="sxs-lookup"><span data-stu-id="c4fa5-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="c4fa5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4fa5-105">Чтобы включить клиентские приложения MAPI, которые создаются как службы Windows для работы с поставщиками услуг, совместимыми с MAPI, MAPI накладывает несколько ограничений и требований.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="c4fa5-106">Клиенты MAPI имеют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="c4fa5-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="c4fa5-107">Они не могут разрешить пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="c4fa5-108">Они могут отправлять сообщения только через тесно связанное хранилище сообщений и поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="c4fa5-109">Кроме того, клиенты MAPI могут отправлять и получать сообщения с помощью только сервера Microsoft Exchange Server или другого поставщика транспорта на основе сервера.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="c4fa5-110">Из-за проблем с идентификацией и безопасностью между клиентскими приложениями и диспетчером очереди MAPI большинство поставщиков транспорта не поддерживаются в службе.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="c4fa5-111">Все клиентские приложения MAPI независимо от того, реализуются ли они как службы Windows, должны вызвать функцию [мапиинитиализе](mapiinitialize.md) для инициализации библиотек MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="c4fa5-112">Вызов функции [олеинитиализе](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) также необходимо для использования библиотек OLE.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="c4fa5-113">Как [мапиинитиализе](mapiinitialize.md) , так и [олеинитиализе](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) выполняют вызовы функции [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) для инициализации библиотек COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="c4fa5-114">Клиенты, которые являются службами, должны задать специальный флаг, MAPI_NT_SERVICE, в элементе **ulFlags** структуры [MAPIINIT_0](mapiinit_0.md) , который передается в [мапиинитиализе](mapiinitialize.md) , и в параметре _ulFlags_ , который передается в функцию [мапилогонекс](mapilogonex.md) для информирования MAPI о их особой реализации.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="c4fa5-115">Клиенты MAPI, написанные как службы Windows и записанные с помощью клиентского интерфейса MAPI, имеют дополнительные требования.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="c4fa5-116">Необходимо установить флаг MAPI_NO_MAIL в вызове [мапилогонекс](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="c4fa5-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="c4fa5-117">Другим типам клиентов не требуется устанавливать флаг для входа в систему, так как он автоматически задается MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="c4fa5-118">Для обработки сообщений в потоке инициализации клиент MAPI, реализованный как служба, выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="c4fa5-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="c4fa5-119">Вызывает функцию [мсгваитформултиплеобжектс](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) , когда блокируется главный поток.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="c4fa5-120">Вызывает последовательность функций [транслатемессаже](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), а также [диспатчмессаже](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) для обработки [сообщения, когда](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx) [мсгваитформултиплеобжектс](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) возвращает сумму значения параметра _нкаунт_ и значение **WAIT_OBJECT_0**, что указывает на то, что сообщение находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="c4fa5-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c4fa5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c4fa5-121">See also</span></span>



[<span data-ttu-id="c4fa5-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="c4fa5-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="c4fa5-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="c4fa5-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="c4fa5-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="c4fa5-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="c4fa5-125">Проблемы с операционной средой</span><span class="sxs-lookup"><span data-stu-id="c4fa5-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

