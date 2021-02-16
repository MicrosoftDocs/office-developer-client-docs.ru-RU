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
# <a name="imapisession--iunknown"></a><span data-ttu-id="9d12c-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d12c-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="9d12c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d12c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d12c-105">Управляет объектами, связанными с сеансом для логотипа MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d12c-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d12c-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9d12c-106">Header file:</span></span>  <br/> |<span data-ttu-id="9d12c-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="9d12c-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="9d12c-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="9d12c-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9d12c-109">Объекты сеанса</span><span class="sxs-lookup"><span data-stu-id="9d12c-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="9d12c-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9d12c-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d12c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="9d12c-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="9d12c-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9d12c-112">Called by:</span></span>  <br/> |<span data-ttu-id="9d12c-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="9d12c-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="9d12c-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9d12c-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9d12c-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="9d12c-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="9d12c-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9d12c-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9d12c-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="9d12c-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9d12c-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="9d12c-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9d12c-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9d12c-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="9d12c-120">Возвращает структуру [MAPIERROR,](mapierror.md) которая содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="9d12c-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="9d12c-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="9d12c-122">Предоставляет доступ к таблице хранилища сообщений, которая содержит сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="9d12c-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="9d12c-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="9d12c-124">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="9d12c-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="9d12c-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="9d12c-126">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="9d12c-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="9d12c-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="9d12c-128">Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="9d12c-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="9d12c-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="9d12c-130">Предоставляет доступ к таблице состояния, которая содержит сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="9d12c-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="9d12c-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="9d12c-132">Открывает объект и возвращает указатель интерфейса для дальнейшего доступа.</span><span class="sxs-lookup"><span data-stu-id="9d12c-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="9d12c-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="9d12c-134">Сравнивает два идентификатора записей, чтобы определить, относятся ли они к одному объекту.</span><span class="sxs-lookup"><span data-stu-id="9d12c-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-135">Консультация</span><span class="sxs-lookup"><span data-stu-id="9d12c-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="9d12c-136">Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="9d12c-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="9d12c-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="9d12c-138">Отменяет отправку уведомлений, которые ранее были настроены с помощью вызова метода **Advise.**</span><span class="sxs-lookup"><span data-stu-id="9d12c-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="9d12c-139">**MessageOptions**</span><span class="sxs-lookup"><span data-stu-id="9d12c-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="9d12c-140">*Не поддерживается и не документируется.*</span><span class="sxs-lookup"><span data-stu-id="9d12c-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9d12c-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="9d12c-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="9d12c-142">*Не поддерживается и не документируется.*</span><span class="sxs-lookup"><span data-stu-id="9d12c-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="9d12c-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="9d12c-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="9d12c-144">Устарело.</span><span class="sxs-lookup"><span data-stu-id="9d12c-144">Deprecated.</span></span> <span data-ttu-id="9d12c-145">Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="9d12c-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="9d12c-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="9d12c-147">Возвращает идентификатор записи объекта, который предоставляет основное удостоверение для сеанса.</span><span class="sxs-lookup"><span data-stu-id="9d12c-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="9d12c-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="9d12c-149">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d12c-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="9d12c-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="9d12c-151">Устанавливает хранилище сообщений как хранилище сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="9d12c-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="9d12c-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="9d12c-153">Возвращает [указатель IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d12c-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="9d12c-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="9d12c-155">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="9d12c-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="9d12c-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="9d12c-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="9d12c-157">Создает числовой маркер, который метод **ShowForm** использует для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="9d12c-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d12c-158">См. также</span><span class="sxs-lookup"><span data-stu-id="9d12c-158">See also</span></span>



[<span data-ttu-id="9d12c-159">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="9d12c-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

