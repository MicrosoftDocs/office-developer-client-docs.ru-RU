---
title: Иаблогон IUnknown
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
# <a name="iablogon--iunknown"></a><span data-ttu-id="cffb4-103">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cffb4-103">IABLogon : IUnknown</span></span>

  
  
<span data-ttu-id="cffb4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cffb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cffb4-105">Доступ к ресурсам в поставщике адресных книг.</span><span class="sxs-lookup"><span data-stu-id="cffb4-105">Accesses resources in an address book provider.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cffb4-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="cffb4-106">Header file:</span></span>  <br/> |<span data-ttu-id="cffb4-107">Маписпи. h</span><span class="sxs-lookup"><span data-stu-id="cffb4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="cffb4-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="cffb4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cffb4-109">Объекты входа в адресную книгу</span><span class="sxs-lookup"><span data-stu-id="cffb4-109">Address book logon objects</span></span>  <br/> |
|<span data-ttu-id="cffb4-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="cffb4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cffb4-111">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="cffb4-111">Address book providers</span></span>  <br/> |
|<span data-ttu-id="cffb4-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="cffb4-112">Called by:</span></span>  <br/> |<span data-ttu-id="cffb4-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="cffb4-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="cffb4-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="cffb4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cffb4-115">IID_IABLogon</span><span class="sxs-lookup"><span data-stu-id="cffb4-115">IID_IABLogon</span></span>  <br/> |
|<span data-ttu-id="cffb4-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="cffb4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="cffb4-117">лпаблогон</span><span class="sxs-lookup"><span data-stu-id="cffb4-117">LPABLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cffb4-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="cffb4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cffb4-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="cffb4-119">GetLastError</span></span>](iablogon-getlasterror.md) <br/> |<span data-ttu-id="cffb4-120">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="cffb4-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-121">Logoff</span><span class="sxs-lookup"><span data-stu-id="cffb4-121">Logoff</span></span>](iablogon-logoff.md) <br/> |<span data-ttu-id="cffb4-122">Инициирует процесс выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="cffb4-122">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-123">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="cffb4-123">OpenEntry</span></span>](iablogon-openentry.md) <br/> |<span data-ttu-id="cffb4-124">Открывает контейнер, пользователя обмена сообщениями или список рассылки и возвращает указатель на реализацию интерфейса для предоставления дальнейших прав доступа.</span><span class="sxs-lookup"><span data-stu-id="cffb4-124">Opens a container, messaging user, or distribution list, and returns a pointer to an interface implementation to provide further access.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="cffb4-125">CompareEntryIDs</span></span>](iablogon-compareentryids.md) <br/> |<span data-ttu-id="cffb4-126">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="cffb4-126">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-127">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="cffb4-127">Advise</span></span>](iablogon-advise.md) <br/> |<span data-ttu-id="cffb4-128">Регистрирует вызывающий абонент для получения уведомления об указанных событиях, влияющих на контейнер, пользователя обмена сообщениями или список рассылки.</span><span class="sxs-lookup"><span data-stu-id="cffb4-128">Registers the caller to receive notification of specified events that affect a container, messaging user, or distribution list.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="cffb4-129">Unadvise</span></span>](iablogon-unadvise.md) <br/> |<span data-ttu-id="cffb4-130">Отменяет уведомления, которые ранее были настроены с помощью вызова метода **advise** .</span><span class="sxs-lookup"><span data-stu-id="cffb4-130">Cancels notifications that were previously set up with a call to the **Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-131">опенстатусентри</span><span class="sxs-lookup"><span data-stu-id="cffb4-131">OpenStatusEntry</span></span>](iablogon-openstatusentry.md) <br/> |<span data-ttu-id="cffb4-132">Открывает объект Status поставщика.</span><span class="sxs-lookup"><span data-stu-id="cffb4-132">Opens the provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-133">опентемплатеид</span><span class="sxs-lookup"><span data-stu-id="cffb4-133">OpenTemplateID</span></span>](iablogon-opentemplateid.md) <br/> |<span data-ttu-id="cffb4-134">Открывает запись получателя, которая содержит данные, находящиеся в поставщике адресной книги узла.</span><span class="sxs-lookup"><span data-stu-id="cffb4-134">Opens a recipient entry that has data residing in a host address book provider.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-135">жетонеоффтабле</span><span class="sxs-lookup"><span data-stu-id="cffb4-135">GetOneOffTable</span></span>](iablogon-getoneofftable.md) <br/> |<span data-ttu-id="cffb4-136">Возвращает таблицу из одноразовых шаблонов для создания получателей, добавляемых в список получателей исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="cffb4-136">Returns a table of one-off templates for creating recipients to be added to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="cffb4-137">препаререЦипс</span><span class="sxs-lookup"><span data-stu-id="cffb4-137">PrepareRecips</span></span>](iablogon-preparerecips.md) <br/> |<span data-ttu-id="cffb4-138">Подготавливает список получателей для последующего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cffb4-138">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cffb4-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="cffb4-139">Remarks</span></span>

<span data-ttu-id="cffb4-140">Общие сведения о методах интерфейса **иаблогон** можно найти в статье [Реализация входа в систему поставщика услуг](implementing-service-provider-logon.md).</span><span class="sxs-lookup"><span data-stu-id="cffb4-140">For general information about the methods of the **IABLogon** interface, see [Implementing Service Provider Logon](implementing-service-provider-logon.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cffb4-141">См. также</span><span class="sxs-lookup"><span data-stu-id="cffb4-141">See also</span></span>



[<span data-ttu-id="cffb4-142">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="cffb4-142">MAPI Interfaces</span></span>](mapi-interfaces.md)

