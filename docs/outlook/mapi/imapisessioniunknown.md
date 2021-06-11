---
title: IMAPISession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession
api_type:
- COM
ms.assetid: 5650fa2a-6e62-451c-964e-363f7bee2344
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1c1a66f61fe1533e436f4e35a542f53d938b4d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413383"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="20c4a-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20c4a-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="20c4a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20c4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20c4a-105">Управляет объектами, связанными с сеансом логотипа MAPI.</span><span class="sxs-lookup"><span data-stu-id="20c4a-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20c4a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="20c4a-106">Header file:</span></span>  <br/> |<span data-ttu-id="20c4a-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="20c4a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="20c4a-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="20c4a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="20c4a-109">Объекты сеанса</span><span class="sxs-lookup"><span data-stu-id="20c4a-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="20c4a-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="20c4a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="20c4a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="20c4a-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="20c4a-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="20c4a-112">Called by:</span></span>  <br/> |<span data-ttu-id="20c4a-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="20c4a-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="20c4a-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="20c4a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="20c4a-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="20c4a-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="20c4a-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="20c4a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="20c4a-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="20c4a-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="20c4a-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="20c4a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="20c4a-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="20c4a-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="20c4a-120">Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="20c4a-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="20c4a-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="20c4a-122">Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="20c4a-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="20c4a-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="20c4a-124">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="20c4a-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="20c4a-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="20c4a-126">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="20c4a-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="20c4a-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="20c4a-128">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="20c4a-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="20c4a-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="20c4a-130">Предоставляет доступ к таблице состояние, таблице, которая содержит сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="20c4a-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="20c4a-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="20c4a-132">Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="20c4a-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="20c4a-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="20c4a-134">Сравнивает два идентификатора записи, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="20c4a-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-135">Консультирование</span><span class="sxs-lookup"><span data-stu-id="20c4a-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="20c4a-136">Регистрируется для получения уведомления о указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="20c4a-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="20c4a-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="20c4a-138">Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода **Advise.**</span><span class="sxs-lookup"><span data-stu-id="20c4a-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="20c4a-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="20c4a-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="20c4a-140">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="20c4a-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="20c4a-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="20c4a-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="20c4a-142">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="20c4a-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="20c4a-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="20c4a-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="20c4a-144">Устарело.</span><span class="sxs-lookup"><span data-stu-id="20c4a-144">Deprecated.</span></span> <span data-ttu-id="20c4a-145">Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="20c4a-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="20c4a-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="20c4a-147">Возвращает идентификатор входа объекта, который предоставляет основное удостоверение сеанса.</span><span class="sxs-lookup"><span data-stu-id="20c4a-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="20c4a-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="20c4a-149">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="20c4a-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="20c4a-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="20c4a-151">Создает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="20c4a-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="20c4a-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="20c4a-153">Возвращает [указатель IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="20c4a-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="20c4a-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="20c4a-155">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="20c4a-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="20c4a-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="20c4a-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="20c4a-157">Создает числимый маркер, который метод **ShowForm** использует для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="20c4a-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="20c4a-158">См. также</span><span class="sxs-lookup"><span data-stu-id="20c4a-158">See also</span></span>



[<span data-ttu-id="20c4a-159">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="20c4a-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

