---
title: Завершение сеанса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287155"
---
# <a name="ending-a-mapi-session"></a><span data-ttu-id="47ebc-103">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="47ebc-103">Ending a MAPI Session</span></span>

  
  
<span data-ttu-id="47ebc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47ebc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47ebc-105">Клиенты могут закончить свои сеансы в ответ на запрос пользователя сразу же или после обработки всех исходящие сообщения, а также при критических ошибках.</span><span class="sxs-lookup"><span data-stu-id="47ebc-105">Clients can end their sessions in response to a user's request, either immediately or after all outbound messages have been processed, and when a critical error occurs.</span></span> <span data-ttu-id="47ebc-106">Некоторые клиенты должны оставаться в системе, чтобы ожидающие исходящие сообщения могли связаться с поставщиком транспорта и системой обмена сообщениями назначения.</span><span class="sxs-lookup"><span data-stu-id="47ebc-106">Some clients need to stay logged on so that pending outbound messages can reach the transport provider and the destination messaging system.</span></span> <span data-ttu-id="47ebc-107">Если такой клиент отправляет сообщение и сразу же выходит из нее, то сообщение может оставаться в исходякой очереди до тех пор, пока пользователь не снова войдите в систему и не войдите в систему достаточно долго, чтобы сообщение было передано.</span><span class="sxs-lookup"><span data-stu-id="47ebc-107">If such a client sends a message and immediately logs off, the message may remain in the outgoing queue until a user logs back on and stays logged on long enough for the message to be transmitted.</span></span>
  
 <span data-ttu-id="47ebc-108">**Когда необходимо завершить сеанс подсистемой MAPI**</span><span class="sxs-lookup"><span data-stu-id="47ebc-108">**When you need to terminate your session with the MAPI subsystem**</span></span>
  
1. <span data-ttu-id="47ebc-109">Отмените регистрации для всех уведомлений, вызывая метод **Unadvise** каждого зарегистрированного объекта.</span><span class="sxs-lookup"><span data-stu-id="47ebc-109">Cancel the registrations for all notifications by calling the **Unadvise** method of every registered object.</span></span> 
    
2. <span data-ttu-id="47ebc-110">Освободите все открытые объекты, вызывая их методы [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47ebc-110">Release all open objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) methods.</span></span> <span data-ttu-id="47ebc-111">Типы открытых объектов могут включать приемники консультаций, таблицу состояния, папку "Outbox", одно или несколько хранилищ сообщений и адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="47ebc-111">The types of open objects can include advise sinks, the status table, the Outbox folder, one or more message stores, and the address book.</span></span> 
    
3. <span data-ttu-id="47ebc-112">Вызовите [MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить память для всех кэшных идентификаторов записей, таких как **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId).](pidtagipmsubtreeentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="47ebc-112">Call [MAPIFreeBuffer](mapifreebuffer.md) to free the memory for any cached entry identifiers, such as **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
4. <span data-ttu-id="47ebc-113">Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session.</span><span class="sxs-lookup"><span data-stu-id="47ebc-113">Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session.</span></span> <span data-ttu-id="47ebc-114">**При этом** всем другим клиентам, использующим текущий общий сеанс, сообщается, что они должны выйти из системы, отправив уведомление об ошибке.</span><span class="sxs-lookup"><span data-stu-id="47ebc-114">**Logoff** notifies all other clients that are using the current shared session that they should log off by sending an error notification.</span></span> 
    
5. <span data-ttu-id="47ebc-115">Освободите указатель сеанса, вызывая метод **IUnknown::Release** сеанса.</span><span class="sxs-lookup"><span data-stu-id="47ebc-115">Release the session pointer by calling the session's **IUnknown::Release** method.</span></span> 
    
6. <span data-ttu-id="47ebc-116">Если вы вызывали [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) во время запуска сеанса для инициализации библиотек OLE, теперь не инициализируют их, вызывая [OleUninitialize.](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="47ebc-116">If you called [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) during session startup to initialize the OLE libraries, uninitialize them now by calling [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx).</span></span> <span data-ttu-id="47ebc-117">Только клиенты, которые **вызывали OleInitialize,** должны **вызывать OleUninitialize.**</span><span class="sxs-lookup"><span data-stu-id="47ebc-117">Only clients that have called **OleInitialize** must call **OleUninitialize**.</span></span> 
    
7. <span data-ttu-id="47ebc-118">Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md).</span><span class="sxs-lookup"><span data-stu-id="47ebc-118">Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="47ebc-119">Если в какой-то момент вы вызывали **OleInitialize,** убедитесь, что перед вызовом **MAPIUninitialize** происходит вызов **OleUninitialize.**</span><span class="sxs-lookup"><span data-stu-id="47ebc-119">If you called **OleInitialize** at some point, make sure that a call to **OleUninitialize** occurs before this call to **MAPIUninitialize**.</span></span> <span data-ttu-id="47ebc-120">Временные рамки очень важны.</span><span class="sxs-lookup"><span data-stu-id="47ebc-120">The timing is crucial.</span></span> <span data-ttu-id="47ebc-121">Если вызов **OleUninitialize** следует за вызовом **MAPIUninitialize,** клиент может завершиться не по-разому.</span><span class="sxs-lookup"><span data-stu-id="47ebc-121">If the call to **OleUninitialize** follows the call to **MAPIUninitialize**, your client might terminate ungracefully.</span></span> 
    
8. <span data-ttu-id="47ebc-122">Если вы [вызывали ScInitMapiUtil](scinitmapiutil.md) во время запуска сеанса, чтобы инициализировать библиотеку utility MAPI, теперь не инициализировать ее, вызывая [DeinitMapiUtil](deinitmapiutil.md).</span><span class="sxs-lookup"><span data-stu-id="47ebc-122">If you called [ScInitMapiUtil](scinitmapiutil.md) during session startup to initialize the MAPI utility library, uninitialize it now by calling [DeinitMapiUtil](deinitmapiutil.md).</span></span> <span data-ttu-id="47ebc-123">Только клиенты, которые вызвали **ScInitMapiUtil,** должны вызывать **DeinitMapiUtil.**</span><span class="sxs-lookup"><span data-stu-id="47ebc-123">Only clients that have called **ScInitMapiUtil** must call **DeinitMapiUtil**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="47ebc-124">Все открытые объекты должны быть отпущены перед вызовом **IMAPISession::Logoff.**</span><span class="sxs-lookup"><span data-stu-id="47ebc-124">All open objects must be released before the call to **IMAPISession::Logoff**.</span></span> <span data-ttu-id="47ebc-125">Объекты, которые остаются открытыми после **того,** как выйдите из нее, становятся недопустимыми; они не могут принимать вызовы и могут никогда не быть освобождены.</span><span class="sxs-lookup"><span data-stu-id="47ebc-125">Objects that remain open after **Logoff** is called become invalid; they cannot accept any calls and might never be freed.</span></span> <span data-ttu-id="47ebc-126">При вызове одного из этих объектов ожидается сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="47ebc-126">If a call is made to one of these objects, expect the call to fail.</span></span> 
  
 <span data-ttu-id="47ebc-127">MAPI не имеет механизма удаления DLL в процессе завершения сеанса.</span><span class="sxs-lookup"><span data-stu-id="47ebc-127">MAPI has no mechanism for deleting DLLs during the session shutdown process.</span></span> <span data-ttu-id="47ebc-128">DLL поставщика услуг можно удалить только в том случае, если клиент конфигурации, например панель управления, вызывает функцию точки входа службы сообщений с MSG_SERVICE_INSTALL события.</span><span class="sxs-lookup"><span data-stu-id="47ebc-128">A service provider's DLL can only be deleted when a configuration client such as the Control Panel calls its message service entry point function with the MSG_SERVICE_INSTALL event.</span></span> 
  

