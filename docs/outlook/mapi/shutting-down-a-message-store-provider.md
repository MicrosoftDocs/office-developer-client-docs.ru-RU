---
title: Завершение работы поставщика store сообщений
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
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="9f1d7-103">Завершение работы поставщика store сообщений</span><span class="sxs-lookup"><span data-stu-id="9f1d7-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="9f1d7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f1d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f1d7-105">Если ваш поставщик является поставщиком store сообщений, его можно отключить одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="9f1d7-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="9f1d7-106">Когда клиент или пулер MAPI вызывает [IMsgStore::StoreLogoff.](imsgstore-storelogoff.md)</span><span class="sxs-lookup"><span data-stu-id="9f1d7-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="9f1d7-107">Отключение поставщика хранения сообщений с **помощью StoreLogoff** приводит к упорядочению и контролю завершения работы.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="9f1d7-108">Когда клиент вызывает [IMAPISession::Logoff.](imapisession-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="9f1d7-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="9f1d7-109">Реализация **IMsgStore::StoreLogoff** должна начинаться с вызова [IMAPISupport::StoreLogoffTransports,](imapisupport-storelogofftransports.md) чтобы сообщить MAPI о том, что она закрывается, указывая, что все связанные поставщики транспорта должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="9f1d7-110">Когда **возвращается IMsgStore::StoreLogoff,** его вызыватель вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) вашего магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="9f1d7-111">Реализуя **этот метод Release,** вы вызываете метод **IUnknown::Release** объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="9f1d7-112">MAPI выполняет следующие задачи в реализации **IUnknown::Release** для хранилищ сообщений:</span><span class="sxs-lookup"><span data-stu-id="9f1d7-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="9f1d7-113">Удаляет все структуры [MAPIUID,](mapiuid.md) зарегистрированные поставщиком store сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="9f1d7-114">Удаляет строку поставщика хранения сообщений из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="9f1d7-115">Вызывает [IMSLogon::Logoff,](imslogon-logoff.md) чтобы освободить все открытые объекты, подобекты и объекты состояния.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="9f1d7-116">Вызывает [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) чтобы освободить объект для логотипа поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="9f1d7-117">Некоторые клиенты могут опустить вызов **IMsgStore::StoreLogoff,** инициав завершение работы поставщика вашего магазина сообщений с помощью вызова метода **IUnknown::Release** в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="9f1d7-118">При таких обстоятельствах завершение работы без вызова **StoreLogoff** является менее упорядоченным и контролируемым.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="9f1d7-119">Запишите метод release  вашего магазина сообщений, чтобы обработать эту возможность и отслеживать, произошел ли вызов **IMAPISupport::StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="9f1d7-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="9f1d7-120">Во время завершения работы необходимо один раз вызвано хранилище **StoreLogoffTransports.**</span><span class="sxs-lookup"><span data-stu-id="9f1d7-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="9f1d7-121">Если вы обнаружите в методе **Release,** что **StoreLogoffTransports** еще не был вызван, вы можете вызвать его с LOGOFF_ABORT флагом.</span><span class="sxs-lookup"><span data-stu-id="9f1d7-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9f1d7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9f1d7-122">See also</span></span>



[<span data-ttu-id="9f1d7-123">Завершение работы поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="9f1d7-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

