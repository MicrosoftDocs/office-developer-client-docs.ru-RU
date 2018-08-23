---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4421fcde6ccd2f2ac6245927d9d5d63ddc5200af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573518"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="84503-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84503-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="84503-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84503-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84503-105">Доступ к ресурсам в поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="84503-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="84503-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="84503-106">Header file:</span></span>  <br/> |<span data-ttu-id="84503-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="84503-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="84503-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="84503-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="84503-109">Адресной книги входа объектов</span><span class="sxs-lookup"><span data-stu-id="84503-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="84503-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="84503-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="84503-111">Поставщиками адресных книг</span><span class="sxs-lookup"><span data-stu-id="84503-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="84503-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="84503-112">Called by:</span></span>  <br/> |<span data-ttu-id="84503-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="84503-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="84503-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="84503-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="84503-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="84503-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="84503-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="84503-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="84503-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="84503-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="84503-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="84503-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="84503-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="84503-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="84503-120">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем Ошибка поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="84503-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="84503-121">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="84503-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="84503-122">Запускает процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="84503-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="84503-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="84503-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="84503-124">Открывает контейнер, системы обмена сообщениями пользователя или список рассылки и возвращает указатель на реализацию интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="84503-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="84503-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="84503-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="84503-126">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="84503-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="84503-127">Уведомить</span><span class="sxs-lookup"><span data-stu-id="84503-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="84503-128">Регистрирует вызывающего абонента для получения уведомлений о указанного события, которые влияют на container, системы обмена сообщениями пользователя или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="84503-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="84503-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="84503-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="84503-130">Запрос уведомления, которые ранее были настроены с помощью вызова метода **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="84503-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="84503-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="84503-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="84503-132">Открывает объект состояние поставщика.</span><span class="sxs-lookup"><span data-stu-id="84503-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="84503-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="84503-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="84503-134">Открывает запись получателя, который содержит данные, хранимые в адресной книге узла.</span><span class="sxs-lookup"><span data-stu-id="84503-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="84503-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="84503-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="84503-136">Возвращает таблицу одноразовых шаблоны для создания получателей для добавления в список получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="84503-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="84503-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="84503-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="84503-138">Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="84503-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84503-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="84503-139">Remarks</span></span>

<span data-ttu-id="84503-140">Общие сведения о методах **IABLogon** интерфейса [Реализации службы поставщика входа в систему](implementing-service-provider-logon.md)см.</span><span class="sxs-lookup"><span data-stu-id="84503-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="84503-141">См. также</span><span class="sxs-lookup"><span data-stu-id="84503-141">See also</span></span>



[<span data-ttu-id="84503-142">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="84503-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

