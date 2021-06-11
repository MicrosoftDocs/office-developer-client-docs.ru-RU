---
title: Отключение поставщика магазина сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339202"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="cc3cd-103">Отключение поставщика магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="cc3cd-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="cc3cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc3cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc3cd-105">Если поставщик является поставщиком магазина сообщений, его можно закрыть одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="cc3cd-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="cc3cd-106">Когда клиент или шпалер MAPI вызывает [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="cc3cd-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="cc3cd-107">Отключение поставщика магазина сообщений с **помощью StoreLogoff** приводит к упорядочению и контролю остановки.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="cc3cd-108">Когда клиент вызывает [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="cc3cd-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="cc3cd-109">Реализация **IMsgStore::StoreLogoff** должна начинаться с вызова [IMAPISupport::StoreLogoffTransports,](imapisupport-storelogofftransports.md) чтобы сообщить MAPI о его закрытии, указав, что все связанные поставщики транспорта должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="cc3cd-110">Когда **возвращается IMsgStore::StoreLogoff,** его вызыватель вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="cc3cd-111">Реализовать этот **метод выпуска,** назвав метод **IUnknown::Release** объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="cc3cd-112">MAPI выполняет следующие задачи в реализации **IUnknown::Release** для магазинов сообщений:</span><span class="sxs-lookup"><span data-stu-id="cc3cd-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="cc3cd-113">Удаляет все структуры [MAPIUID,](mapiuid.md) зарегистрированные поставщиком магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="cc3cd-114">Удаляет строку поставщика хранения сообщений из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="cc3cd-115">Вызывает [IMSLogon::Logoff,](imslogon-logoff.md) чтобы освободить все открытые объекты, подобекты и объекты состояния.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="cc3cd-116">Вызывает [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) чтобы освободить объект логотипа поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="cc3cd-117">Некоторые клиенты могут отключить вызов **в IMsgStore::StoreLogoff,** инициав остановку поставщика магазина сообщений с помощью вызова метода **IUnknown::Release** магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="cc3cd-118">При таких обстоятельствах отключение без вызова **в StoreLogoff** является менее упорядоченным и управляемым.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="cc3cd-119">Напишите метод выпуска  магазина сообщений для обработки этой возможности и отслеживайте, был ли звонок **в IMAPISupport::StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="cc3cd-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="cc3cd-120">**StoreLogoffTransports** должен быть вызван один раз в процессе остановки.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="cc3cd-121">Если в методе **выпуска** обнаружено, что **StoreLogoffTransports** еще не вызывался, вызывайте его с LOGOFF_ABORT флагом.</span><span class="sxs-lookup"><span data-stu-id="cc3cd-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc3cd-122">См. также</span><span class="sxs-lookup"><span data-stu-id="cc3cd-122">See also</span></span>



[<span data-ttu-id="cc3cd-123">Отключение поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="cc3cd-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

