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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385580"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="a677e-103">Вызов MAPI из служб Windows</span><span class="sxs-lookup"><span data-stu-id="a677e-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="a677e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a677e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a677e-105">Чтобы включить клиентские приложения MAPI, которые записываются в виде служб Windows для работы с MAPI-совместимое поставщиков услуг, MAPI, задает некоторые ограничения и требования.</span><span class="sxs-lookup"><span data-stu-id="a677e-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="a677e-106">Клиенты MAPI имеют следующие ограничения:</span><span class="sxs-lookup"><span data-stu-id="a677e-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="a677e-107">Они не могут разрешить пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a677e-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="a677e-108">Они могут отправлять сообщения только с помощью хранилища тесно связанных сообщений и транспорта поставщика.</span><span class="sxs-lookup"><span data-stu-id="a677e-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="a677e-109">Кроме того клиентов MAPI можно отправлять и получать сообщения с помощью Exchange Server корпорации Майкрософт или другого поставщика транспорта на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a677e-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="a677e-110">Из-за проблем удостоверения и безопасности между клиентскими приложениями и диспетчер очереди MAPI большинство поставщиков транспорта не поддерживаются в службе.</span><span class="sxs-lookup"><span data-stu-id="a677e-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="a677e-111">Все клиентские приложения MAPI, ли они реализованы в качестве службы Windows, необходимо вызвать функцию [MAPIInitialize](mapiinitialize.md) для инициализации библиотеки MAPI.</span><span class="sxs-lookup"><span data-stu-id="a677e-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="a677e-112">Вызов функции [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) также возникает необходимость использования библиотек OLE.</span><span class="sxs-lookup"><span data-stu-id="a677e-112">A call to the [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="a677e-113">[MAPIInitialize](mapiinitialize.md) и [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) вызывать функции [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) при инициализации библиотек модели компонентных объектов (COM).</span><span class="sxs-lookup"><span data-stu-id="a677e-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](https://msdn.microsoft.com/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="a677e-114">Клиенты, которые являются службы необходимо установить специальные флаг MAPI_NT_SERVICE, в член **ulFlags** структуры [MAPIINIT_0](mapiinit_0.md) , который передается в [MAPIInitialize](mapiinitialize.md) и с помощью параметра _ulFlags_ , который передается в [MAPILogonEx](mapilogonex.md) функция для оповещения MAPI их специальных реализаций.</span><span class="sxs-lookup"><span data-stu-id="a677e-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="a677e-115">Клиентов MAPI, которые записываются как службы Windows и записи с помощью клиентского интерфейса MAPI имеют дополнительные требования.</span><span class="sxs-lookup"><span data-stu-id="a677e-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="a677e-116">Они должны установить флаг MAPI_NO_MAIL в вызове [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="a677e-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="a677e-117">Другие типы клиентов нет необходимости задан флаг для входа в систему, так как он автоматически устанавливается с MAPI.</span><span class="sxs-lookup"><span data-stu-id="a677e-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="a677e-118">Для обработки сообщений в поток инициализации, клиент MAPI, который реализован в виде службы выполняет следующее.</span><span class="sxs-lookup"><span data-stu-id="a677e-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="a677e-119">Функция [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) вызывается при основной поток блокируется.</span><span class="sxs-lookup"><span data-stu-id="a677e-119">Calls the [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="a677e-120">Вызывает [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [используемых](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx)и [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) последовательность функции Windows для обработки сообщений при [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) возвращает сумму значение параметра _nCount_ и значение **WAIT_OBJECT_0**, это означает, что сообщение находится в очереди.</span><span class="sxs-lookup"><span data-stu-id="a677e-120">Calls the [GetMessage](https://msdn.microsoft.com/library/ms644936%28VS.85%29.aspx), [TranslateMessage](https://msdn.microsoft.com/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](https://msdn.microsoft.com/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](https://msdn.microsoft.com/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a677e-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a677e-121">See also</span></span>



[<span data-ttu-id="a677e-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="a677e-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="a677e-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="a677e-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="a677e-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="a677e-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="a677e-125">Проблемы с операционной средой</span><span class="sxs-lookup"><span data-stu-id="a677e-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

