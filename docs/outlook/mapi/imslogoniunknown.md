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
# <a name="imslogon--iunknown"></a><span data-ttu-id="68b58-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68b58-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="68b58-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68b58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68b58-105">Доступ к ресурсам в объекте для входов в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b58-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="68b58-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="68b58-106">Header file:</span></span>  <br/> |<span data-ttu-id="68b58-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="68b58-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="68b58-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="68b58-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="68b58-109">Объекты для логотипа в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="68b58-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="68b58-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="68b58-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="68b58-111">Поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="68b58-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="68b58-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="68b58-112">Called by:</span></span>  <br/> |<span data-ttu-id="68b58-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="68b58-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="68b58-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="68b58-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="68b58-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="68b58-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="68b58-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="68b58-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="68b58-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="68b58-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="68b58-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="68b58-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="68b58-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="68b58-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="68b58-120">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b58-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="68b58-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="68b58-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="68b58-122">Выйдите из службы хранения сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b58-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="68b58-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="68b58-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="68b58-124">Открывает папку или объект сообщения и возвращает указатель на объект для обеспечения дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="68b58-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="68b58-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="68b58-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="68b58-126">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="68b58-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="68b58-127">Консультация</span><span class="sxs-lookup"><span data-stu-id="68b58-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="68b58-128">Регистрирует объект у поставщика хранения сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="68b58-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="68b58-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="68b58-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="68b58-130">Удаляет регистрацию объекта для уведомления об изменениях в хранилище сообщений, ранее установленных с помощью вызова метода **IMSLogon::Advise.**</span><span class="sxs-lookup"><span data-stu-id="68b58-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="68b58-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="68b58-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="68b58-132">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="68b58-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68b58-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="68b58-133">Remarks</span></span>

<span data-ttu-id="68b58-134">Объект для логотипа в хранилище сообщений является частью поставщика открытого хранения сообщений, который напрямую вызывает MAPI.</span><span class="sxs-lookup"><span data-stu-id="68b58-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="68b58-135">Существует соответствие "один к одному" между объектом для эмблемы для хранения сообщений, который вызывает MAPI, и объектом хранения сообщений, который вызывает клиентские приложения; вы можете подумать о том, что объекты для логона и хранения будут одним объектом, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="68b58-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="68b58-136">Эти два объекта создаются вместе и вместе освобождены.</span><span class="sxs-lookup"><span data-stu-id="68b58-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68b58-137">См. также</span><span class="sxs-lookup"><span data-stu-id="68b58-137">See also</span></span>



[<span data-ttu-id="68b58-138">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="68b58-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

