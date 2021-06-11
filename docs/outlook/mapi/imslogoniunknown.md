---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428881"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="a45aa-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a45aa-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="a45aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a45aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a45aa-105">Доступ к ресурсам в объекте logon магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="a45aa-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a45aa-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a45aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="a45aa-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="a45aa-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="a45aa-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="a45aa-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a45aa-109">Объекты логона магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="a45aa-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="a45aa-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a45aa-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a45aa-111">Поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="a45aa-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="a45aa-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a45aa-112">Called by:</span></span>  <br/> |<span data-ttu-id="a45aa-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="a45aa-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="a45aa-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="a45aa-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a45aa-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="a45aa-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="a45aa-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="a45aa-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a45aa-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="a45aa-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a45aa-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="a45aa-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a45aa-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a45aa-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="a45aa-120">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="a45aa-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="a45aa-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="a45aa-122">Журналы поставщика магазина сообщений.</span><span class="sxs-lookup"><span data-stu-id="a45aa-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="a45aa-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="a45aa-124">Открывает папку или объект сообщения и возвращает указатель на объект, чтобы обеспечить дополнительный доступ.</span><span class="sxs-lookup"><span data-stu-id="a45aa-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="a45aa-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="a45aa-126">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="a45aa-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-127">Консультирование</span><span class="sxs-lookup"><span data-stu-id="a45aa-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="a45aa-128">Регистрирует объект с поставщиком магазина сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="a45aa-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="a45aa-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="a45aa-130">Удаляет регистрацию объекта для уведомления об изменениях в хранилище сообщений, ранее установленных с помощью вызова метода **IMSLogon::Advise.**</span><span class="sxs-lookup"><span data-stu-id="a45aa-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="a45aa-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="a45aa-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="a45aa-132">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="a45aa-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a45aa-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="a45aa-133">Remarks</span></span>

<span data-ttu-id="a45aa-134">Объект logon магазина сообщений является частью поставщика магазина открытых сообщений, который вызывает MAPI напрямую.</span><span class="sxs-lookup"><span data-stu-id="a45aa-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="a45aa-135">Между объектом логотипа магазина сообщений, вызываемого MAPI, и объектом магазина сообщений, вызываемого клиентских приложений, существует один к одному. вы можете думать о логотипе и хранить объекты как один объект, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a45aa-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="a45aa-136">Эти два объекта создаются вместе и освобождены вместе.</span><span class="sxs-lookup"><span data-stu-id="a45aa-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a45aa-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a45aa-137">See also</span></span>



[<span data-ttu-id="a45aa-138">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="a45aa-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

