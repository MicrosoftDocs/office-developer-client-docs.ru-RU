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
ms.openlocfilehash: 1c7ae4ab6de20d69581a98323c14a2c15f436cad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572825"
---
# <a name="shutting-down-a-message-store-provider"></a><span data-ttu-id="7a0d1-103">Завершение работы поставщика хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="7a0d1-103">Shutting Down a Message Store Provider</span></span>

  
  
<span data-ttu-id="7a0d1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a0d1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a0d1-105">Если ваш поставщик поставщика хранилища сообщений, его можно завершить работу в одном из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="7a0d1-105">If your provider is a message store provider, it can be shut down in one of the following ways:</span></span>
  
- <span data-ttu-id="7a0d1-106">Если это клиент или диспетчер очереди MAPI вызывает [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span><span class="sxs-lookup"><span data-stu-id="7a0d1-106">When a client or the MAPI spooler calls [IMsgStore::StoreLogoff](imsgstore-storelogoff.md).</span></span> <span data-ttu-id="7a0d1-107">Завершение работы поставщика хранилища сообщений с **StoreLogoff** вызывает завершение работы в надлежащей и управляемым процессом.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-107">Shutting down a message store provider with **StoreLogoff** causes the shutdown to occur in an orderly and controlled manner.</span></span> 
    
- <span data-ttu-id="7a0d1-108">Когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="7a0d1-108">When a client calls [IMAPISession::Logoff](imapisession-logoff.md).</span></span> 
    
<span data-ttu-id="7a0d1-109">Реализация **IMsgStore::StoreLogoff** должен начинаться с вызова [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) для оповещения MAPI, что оно завершает работу, указывающее регистрацию поставщиков, связанных с ними транспорта.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-109">Your implementation of **IMsgStore::StoreLogoff** should begin by calling [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) to inform MAPI that it is being shut down, indicating that any related transport providers should be logged off.</span></span> <span data-ttu-id="7a0d1-110">При возврате **IMsgStore::StoreLogoff** , вызывающий вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-110">When **IMsgStore::StoreLogoff** returns, its caller invokes your message store's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method.</span></span> <span data-ttu-id="7a0d1-111">Реализуйте метод в этом **выпуске** , вызвав метод **функции IUnknown::Release** объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-111">Implement this **Release** method by calling the support object's **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="7a0d1-112">При реализации **функции IUnknown::Release** для хранилищ сообщений MAPI выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7a0d1-112">MAPI performs the following tasks in its implementation of **IUnknown::Release** for message stores:</span></span> 
  
1. <span data-ttu-id="7a0d1-113">Удаляет все структуры [MAPIUID](mapiuid.md) , зарегистрированные поставщиком хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-113">Removes all of the [MAPIUID](mapiuid.md) structures registered by the message store provider.</span></span> 
    
2. <span data-ttu-id="7a0d1-114">Удаляет поставщика хранилища сообщений строку из таблицы состояния.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-114">Removes the message store provider's row from the status table.</span></span>
    
3. <span data-ttu-id="7a0d1-115">Вызывает [IMSLogon::Logoff](imslogon-logoff.md) для освобождения всех открытых объектов, вложенных объектов и объектов состояние.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-115">Calls [IMSLogon::Logoff](imslogon-logoff.md) to release all open objects, subobjects, and status objects.</span></span> 
    
4. <span data-ttu-id="7a0d1-116">Вызывает [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) для освобождения объект поставщика хранилища сообщений входа в систему.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-116">Calls [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) to release the message store provider's logon object.</span></span> 
    
<span data-ttu-id="7a0d1-117">Некоторые клиенты могут пропустить вызов **IMsgStore::StoreLogoff**, инициализация завершения конкретного поставщика хранилища сообщений с помощью вызова метода **функции IUnknown::Release** хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-117">Some clients might omit the call to **IMsgStore::StoreLogoff**, initiating the shutdown of your message store provider with the call to the message store's **IUnknown::Release** method.</span></span> <span data-ttu-id="7a0d1-118">Завершение работы при следующих условиях без вызова **StoreLogoff** менее нормального и управляемой.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-118">A shutdown under these circumstances without the call to **StoreLogoff** is less orderly and controlled.</span></span> <span data-ttu-id="7a0d1-119">Метод **выпуске** хранилища сообщений для обработки этой возможности и отслеживание ли вызов **IMAPISupport::StoreLogoffTransports** произошла Write.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-119">Write your message store's **Release** method to handle this possibility and keep track of whether or not a call to **IMAPISupport::StoreLogoffTransports** has occurred.</span></span> <span data-ttu-id="7a0d1-120">**StoreLogoffTransports** необходимо вызывать один раз при завершении работы.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-120">**StoreLogoffTransports** must be called once during the shutdown process.</span></span> <span data-ttu-id="7a0d1-121">Если в методе **выпуске** определяет, что **StoreLogoffTransports** еще не был вызван, вызовите с флагом LOGOFF_ABORT.</span><span class="sxs-lookup"><span data-stu-id="7a0d1-121">If you detect in your **Release** method that **StoreLogoffTransports** has not yet been called, invoke it with the LOGOFF_ABORT flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a0d1-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7a0d1-122">See also</span></span>



[<span data-ttu-id="7a0d1-123">Завершение работы поставщика службы</span><span class="sxs-lookup"><span data-stu-id="7a0d1-123">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

