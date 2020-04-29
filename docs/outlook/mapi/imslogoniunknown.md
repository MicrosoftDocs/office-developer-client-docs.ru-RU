---
title: Имслогон IUnknown
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
# <a name="imslogon--iunknown"></a><span data-ttu-id="590b8-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="590b8-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="590b8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="590b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="590b8-105">Получает доступ к ресурсам в объекте входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="590b8-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="590b8-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="590b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="590b8-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="590b8-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="590b8-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="590b8-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="590b8-109">Объекты входа в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="590b8-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="590b8-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="590b8-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="590b8-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="590b8-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="590b8-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="590b8-112">Called by:</span></span>  <br/> |<span data-ttu-id="590b8-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="590b8-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="590b8-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="590b8-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="590b8-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="590b8-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="590b8-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="590b8-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="590b8-117">лпмслогон</span><span class="sxs-lookup"><span data-stu-id="590b8-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="590b8-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="590b8-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="590b8-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="590b8-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="590b8-120">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="590b8-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="590b8-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="590b8-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="590b8-122">Выполняет выход из системы поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="590b8-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="590b8-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="590b8-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="590b8-124">Открывает папку или объект Message и возвращает указатель на объект, предоставляющий дополнительный доступ.</span><span class="sxs-lookup"><span data-stu-id="590b8-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="590b8-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="590b8-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="590b8-126">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="590b8-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="590b8-127">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="590b8-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="590b8-128">Регистрирует объект с поставщиком хранилища сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="590b8-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="590b8-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="590b8-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="590b8-130">Удаляет регистрацию объекта для уведомления об изменениях хранилища сообщений, ранее установленных с помощью вызова метода **имслогон:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="590b8-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="590b8-131">опенстатусентри</span><span class="sxs-lookup"><span data-stu-id="590b8-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="590b8-132">Открывает объект Status.</span><span class="sxs-lookup"><span data-stu-id="590b8-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="590b8-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="590b8-133">Remarks</span></span>

<span data-ttu-id="590b8-134">Объект входа в хранилище сообщений является частью открытого поставщика хранилища сообщений, который напрямую вызывает MAPI.</span><span class="sxs-lookup"><span data-stu-id="590b8-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="590b8-135">Существует однозначное соответствие между объектом входа в хранилище сообщений, который вызывает MAPI, и объектом хранилища сообщений, которые вызывают клиентские приложения; Вы можете представить объекты входа и хранилища как один объект, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="590b8-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="590b8-136">Два объекта создаются вместе и освобождаются вместе.</span><span class="sxs-lookup"><span data-stu-id="590b8-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="590b8-137">См. также</span><span class="sxs-lookup"><span data-stu-id="590b8-137">See also</span></span>



[<span data-ttu-id="590b8-138">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="590b8-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

