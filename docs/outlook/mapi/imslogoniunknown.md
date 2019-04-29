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
# <a name="imslogon--iunknown"></a><span data-ttu-id="6ef3a-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ef3a-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="6ef3a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ef3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ef3a-105">Получает доступ к ресурсам в объекте входа в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ef3a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-106">Header file:</span></span>  <br/> |<span data-ttu-id="6ef3a-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="6ef3a-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="6ef3a-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="6ef3a-109">Объекты входа в хранилище сообщений</span><span class="sxs-lookup"><span data-stu-id="6ef3a-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="6ef3a-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="6ef3a-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="6ef3a-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="6ef3a-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-112">Called by:</span></span>  <br/> |<span data-ttu-id="6ef3a-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef3a-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="6ef3a-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6ef3a-115">Иид_имслогон</span><span class="sxs-lookup"><span data-stu-id="6ef3a-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="6ef3a-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="6ef3a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="6ef3a-117">ЛПМСЛОГОН</span><span class="sxs-lookup"><span data-stu-id="6ef3a-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6ef3a-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="6ef3a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6ef3a-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="6ef3a-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="6ef3a-120">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="6ef3a-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="6ef3a-122">Выполняет выход из системы поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="6ef3a-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="6ef3a-124">Открывает папку или объект Message и возвращает указатель на объект, предоставляющий дополнительный доступ.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="6ef3a-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="6ef3a-126">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-127">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="6ef3a-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="6ef3a-128">Регистрирует объект с поставщиком хранилища сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="6ef3a-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="6ef3a-130">Удаляет регистрацию объекта для уведомления об изменениях хранилища сообщений, ранее установленных с помощью вызова метода **имслогон:: Advise** .</span><span class="sxs-lookup"><span data-stu-id="6ef3a-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="6ef3a-131">Опенстатусентри</span><span class="sxs-lookup"><span data-stu-id="6ef3a-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="6ef3a-132">Открывает объект Status.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ef3a-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="6ef3a-133">Remarks</span></span>

<span data-ttu-id="6ef3a-134">Объект входа в хранилище сообщений является частью открытого поставщика хранилища сообщений, который напрямую вызывает MAPI.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="6ef3a-135">Существует однозначное соответствие между объектом входа в хранилище сообщений, который вызывает MAPI, и объектом хранилища сообщений, которые вызывают клиентские приложения; Вы можете представить объекты входа и хранилища как один объект, который предоставляет два интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="6ef3a-136">Два объекта создаются вместе и освобождаются вместе.</span><span class="sxs-lookup"><span data-stu-id="6ef3a-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6ef3a-137">См. также</span><span class="sxs-lookup"><span data-stu-id="6ef3a-137">See also</span></span>



[<span data-ttu-id="6ef3a-138">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="6ef3a-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

