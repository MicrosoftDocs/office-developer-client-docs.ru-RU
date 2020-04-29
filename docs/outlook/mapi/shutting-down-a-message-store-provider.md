---
title: Завершение работы поставщика хранилища сообщений
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
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="6de0a-103">Завершение работы поставщика хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="6de0a-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="6de0a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6de0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6de0a-105">Если поставщик является поставщиком хранилища сообщений, его можно завершить одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="6de0a-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="6de0a-106">Если клиент или диспетчер очереди MAPI вызывает [IMsgStore:: сторелогофф](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="6de0a-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="6de0a-107">При завершении работы поставщика хранилища сообщений с **сторелогофф** происходит завершение работы в определенном порядке и управляемым образом.</span><span class="sxs-lookup"><span data-stu-id="6de0a-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="6de0a-108">Когда клиент вызывает [IMAPISession:: logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="6de0a-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="6de0a-109">Реализация **IMsgStore:: сторелогофф** должна начинаться с вызова [Имаписуппорт:: сторелогоффтранспортс](imapisupport-storelogofftransports.md) , чтобы уведомить MAPI о завершении работы, указывая, что все связанные транспортные поставщики должны выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="6de0a-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="6de0a-110">Когда **IMsgStore:: сторелогофф** возвращает значение, его вызывающий объект вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6de0a-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="6de0a-111">Реализуйте этот метод **освобождения** , вызвав метод **IUnknown:: Release** объекта support.</span><span class="sxs-lookup"><span data-stu-id="6de0a-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="6de0a-112">MAPI выполняет следующие задачи в своей реализации интерфейса **IUnknown:: Release** для хранилищ сообщений:</span><span class="sxs-lookup"><span data-stu-id="6de0a-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="6de0a-113">Удаляет все структуры [мапиуид](mapiuid.md) , зарегистрированные поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6de0a-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="6de0a-114">Удаляет строку поставщика хранилища сообщений из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="6de0a-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="6de0a-115">Calls [имслогон:: logoff](imslogon-logoff.md) для освобождения всех открытых объектов, подобъектов и объектов Status.</span><span class="sxs-lookup"><span data-stu-id="6de0a-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="6de0a-116">Вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) для освобождения объекта входа поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6de0a-116">Calls [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="6de0a-117">Некоторые клиенты могут опустить вызов **IMsgStore:: сторелогофф**, инициируя завершение работы поставщика хранилища сообщений с вызовом метода **IUnknown:: Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6de0a-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="6de0a-118">Завершение работы при таких обстоятельствах без вызова **сторелогофф** менее упорядочено и управляется.</span><span class="sxs-lookup"><span data-stu-id="6de0a-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="6de0a-119">Запишите метод **освобождения** хранилища сообщений, чтобы обработать эту возможность, и следит за тем, был ли вызван вызов **Имаписуппорт:: сторелогоффтранспортс** .</span><span class="sxs-lookup"><span data-stu-id="6de0a-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="6de0a-120">В процессе завершения работы **сторелогоффтранспортс** должен вызываться один раз.</span><span class="sxs-lookup"><span data-stu-id="6de0a-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="6de0a-121">Если вы обнаружите в методе **Release** , что **сторелогоффтранспортс** еще не вызывался, вызовите его с флагом LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="6de0a-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6de0a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="6de0a-122">See also</span></span>



[<span data-ttu-id="6de0a-123">Завершение работы поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="6de0a-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

