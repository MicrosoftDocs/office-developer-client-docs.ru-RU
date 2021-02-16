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
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431080"
---
# <a name="iablogon--iunknown"></a><span data-ttu-id="ed7f5-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed7f5-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="ed7f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed7f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed7f5-105">Доступ к ресурсам в поставщике адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed7f5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed7f5-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="ed7f5-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="ed7f5-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ed7f5-109">Объекты для логотипа адресной книги</span><span class="sxs-lookup"><span data-stu-id="ed7f5-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="ed7f5-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed7f5-111">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="ed7f5-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="ed7f5-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-112">Called by:</span></span>  <br/> |<span data-ttu-id="ed7f5-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="ed7f5-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="ed7f5-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ed7f5-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="ed7f5-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="ed7f5-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ed7f5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ed7f5-117">LPABLOGON</span><span class="sxs-lookup"><span data-stu-id="ed7f5-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ed7f5-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="ed7f5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ed7f5-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ed7f5-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="ed7f5-120">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="ed7f5-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="ed7f5-122">Инициирует процесс выйдите из нее.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ed7f5-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="ed7f5-124">Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для обеспечения дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ed7f5-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="ed7f5-126">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-127">Консультация</span><span class="sxs-lookup"><span data-stu-id="ed7f5-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="ed7f5-128">Регистрирует вызываемого пользователя для получения уведомлений об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ed7f5-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="ed7f5-130">Отменяет уведомления, которые ранее были настроены с помощью вызова метода **Advise.**</span><span class="sxs-lookup"><span data-stu-id="ed7f5-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-131">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="ed7f5-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="ed7f5-132">Открывает объект состояния поставщика.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-133">OpenTemplateID</span><span class="sxs-lookup"><span data-stu-id="ed7f5-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="ed7f5-134">Открывает запись получателя с данными, которые есть в поставщике адресной книги хост-адреса.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-135">GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="ed7f5-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="ed7f5-136">Возвращает таблицу разных шаблонов для создания получателей, добавляемой в список получателей исходяного сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="ed7f5-137">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="ed7f5-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="ed7f5-138">Подготавливает список получателей к дальнейшему использованию системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ed7f5-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed7f5-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ed7f5-139">Remarks</span></span>

<span data-ttu-id="ed7f5-140">Общие сведения о методах интерфейса **IABLogon** см. в этой [теме.](implementing-service-provider-logon.md)</span><span class="sxs-lookup"><span data-stu-id="ed7f5-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ed7f5-141">См. также</span><span class="sxs-lookup"><span data-stu-id="ed7f5-141">See also</span></span>



[<span data-ttu-id="ed7f5-142">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ed7f5-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

