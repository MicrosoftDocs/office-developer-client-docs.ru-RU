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
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563942"
---
# <a name="imslogon--iunknown"></a><span data-ttu-id="57edb-103">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="57edb-103">IMSLogon : IUnknown</span></span>

  
  
<span data-ttu-id="57edb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57edb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57edb-105">Доступ к ресурсам в сообщение хранилища вход в систему.</span><span class="sxs-lookup"><span data-stu-id="57edb-105">Accesses resources in a message store logon object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="57edb-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="57edb-106">Header file:</span></span>  <br/> |<span data-ttu-id="57edb-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="57edb-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="57edb-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="57edb-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="57edb-109">Объекты входа хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="57edb-109">Message store logon objects</span></span>  <br/> |
|<span data-ttu-id="57edb-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="57edb-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="57edb-111">Поставщики хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="57edb-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="57edb-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="57edb-112">Called by:</span></span>  <br/> |<span data-ttu-id="57edb-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="57edb-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="57edb-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="57edb-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="57edb-115">IID_IMSLogon</span><span class="sxs-lookup"><span data-stu-id="57edb-115">IID_IMSLogon</span></span>  <br/> |
|<span data-ttu-id="57edb-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="57edb-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="57edb-117">LPMSLOGON</span><span class="sxs-lookup"><span data-stu-id="57edb-117">LPMSLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="57edb-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="57edb-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="57edb-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="57edb-119">GetLastError</span></span>](imslogon-getlasterror.md) <br/> |<span data-ttu-id="57edb-120">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о последней ошибке, возникшей для объекта хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="57edb-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the last error that occurred for the message store object.</span></span>  <br/> |
|[<span data-ttu-id="57edb-121">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="57edb-121">Logoff</span></span>](imslogon-logoff.md) <br/> |<span data-ttu-id="57edb-122">Поставщик хранилища, выходит из системы сообщение.</span><span class="sxs-lookup"><span data-stu-id="57edb-122">Logs off a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="57edb-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="57edb-123">OpenEntry</span></span>](imslogon-openentry.md) <br/> |<span data-ttu-id="57edb-124">Открывает папку или объект сообщения и возвращает указатель на объект для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="57edb-124">Opens a folder or message object and returns a pointer to the object to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="57edb-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="57edb-125">CompareEntryIDs</span></span>](imslogon-compareentryids.md) <br/> |<span data-ttu-id="57edb-126">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="57edb-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="57edb-127">Уведомить</span><span class="sxs-lookup"><span data-stu-id="57edb-127">Advise</span></span>](imslogon-advise.md) <br/> |<span data-ttu-id="57edb-128">Регистрирует объект поставщика хранилища сообщений для уведомлений об изменениях в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="57edb-128">Registers an object with a message store provider for notifications about changes in the message store.</span></span>  <br/> |
|[<span data-ttu-id="57edb-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="57edb-129">Unadvise</span></span>](imslogon-unadvise.md) <br/> |<span data-ttu-id="57edb-130">Удаляет регистрацию объекта для уведомление об изменениях хранилища сообщений, ранее созданные с помощью вызова метода **IMSLogon::Advise** .</span><span class="sxs-lookup"><span data-stu-id="57edb-130">Removes an object's registration for notification of message store changes previously established by using a call to the **IMSLogon::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="57edb-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="57edb-131">OpenStatusEntry</span></span>](imslogon-openstatusentry.md) <br/> |<span data-ttu-id="57edb-132">Открывает объект состояния.</span><span class="sxs-lookup"><span data-stu-id="57edb-132">Opens a status object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57edb-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="57edb-133">Remarks</span></span>

<span data-ttu-id="57edb-134">Объект вход в систему хранения сообщения является частью поставщика хранилища открыть сообщение, непосредственно вызывающий MAPI.</span><span class="sxs-lookup"><span data-stu-id="57edb-134">The message store logon object is the part of an open message store provider that MAPI calls directly.</span></span> <span data-ttu-id="57edb-135">Существует однозначного соответствия между объект вход в систему хранилища сообщений, на котором вызовов MAPI и сообщения храниться объект, который метода клиентских приложений. можно рассматривать вход в систему и хранения объектов как один объект, который предоставляет два из них.</span><span class="sxs-lookup"><span data-stu-id="57edb-135">There is a one-to-one correspondence between the message store logon object that MAPI calls and the message store object that client applications call; you can think of the logon and store objects as one object that exposes two interfaces.</span></span> <span data-ttu-id="57edb-136">Создаются два объекта вместе и освобожденное друг с другом.</span><span class="sxs-lookup"><span data-stu-id="57edb-136">The two objects are created together and freed together.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="57edb-137">См. также</span><span class="sxs-lookup"><span data-stu-id="57edb-137">See also</span></span>



[<span data-ttu-id="57edb-138">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="57edb-138">MAPI Interfaces</span></span>](mapi-interfaces.md)

