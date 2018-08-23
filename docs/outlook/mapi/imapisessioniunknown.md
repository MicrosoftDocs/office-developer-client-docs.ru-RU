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
ms.openlocfilehash: 163bce38d665a8566fd703420ff1f7b2f44f7c63
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571810"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="05dd2-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="05dd2-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="05dd2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05dd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05dd2-105">Управляет объекты, связанные с сеанса входа MAPI.</span><span class="sxs-lookup"><span data-stu-id="05dd2-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="05dd2-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="05dd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="05dd2-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="05dd2-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="05dd2-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="05dd2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="05dd2-109">Объекты сеанса</span><span class="sxs-lookup"><span data-stu-id="05dd2-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="05dd2-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="05dd2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="05dd2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="05dd2-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="05dd2-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="05dd2-112">Called by:</span></span>  <br/> |<span data-ttu-id="05dd2-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="05dd2-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="05dd2-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="05dd2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="05dd2-115">IID_IMAPISession</span><span class="sxs-lookup"><span data-stu-id="05dd2-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="05dd2-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="05dd2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="05dd2-117">LPMAPISESSION</span><span class="sxs-lookup"><span data-stu-id="05dd2-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="05dd2-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="05dd2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="05dd2-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="05dd2-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="05dd2-120">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="05dd2-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-121">GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="05dd2-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="05dd2-122">Предоставляет доступ к таблице хранилища сообщений, который содержит сведения о всех хранилищ сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="05dd2-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-123">OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="05dd2-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="05dd2-124">Открывает хранилища сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="05dd2-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-125">OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="05dd2-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="05dd2-126">Открывает интегрированной адресной книги MAPI, возвращает указатель [IAddrBook](iaddrbookimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="05dd2-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-127">OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="05dd2-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="05dd2-128">Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="05dd2-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-129">GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="05dd2-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="05dd2-130">Предоставляет доступ к таблице состояния, таблицу, содержащую сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="05dd2-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="05dd2-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="05dd2-132">Открывает объект и возвращает указатель интерфейса для дальнейшей доступа.</span><span class="sxs-lookup"><span data-stu-id="05dd2-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="05dd2-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="05dd2-134">Сравнение двух идентификаторы записей для определения, является ли они ссылаются на тот же объект.</span><span class="sxs-lookup"><span data-stu-id="05dd2-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-135">Уведомить</span><span class="sxs-lookup"><span data-stu-id="05dd2-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="05dd2-136">Регистрация для получения уведомлений о указанного события, которые влияют на сеанс.</span><span class="sxs-lookup"><span data-stu-id="05dd2-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="05dd2-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="05dd2-138">Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="05dd2-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="05dd2-139">**Параметры сообщения**</span><span class="sxs-lookup"><span data-stu-id="05dd2-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="05dd2-140">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="05dd2-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="05dd2-141">**QueryDefaultMessageOpt**</span><span class="sxs-lookup"><span data-stu-id="05dd2-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="05dd2-142">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="05dd2-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="05dd2-143">EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="05dd2-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="05dd2-144">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="05dd2-144">Deprecated.</span></span> <span data-ttu-id="05dd2-145">Возвращает типы адресов, которые могут быть обработаны всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="05dd2-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-146">QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="05dd2-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="05dd2-147">Возвращает идентификатор записи объекта, который содержит основной идентификатор для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="05dd2-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-148">Выход из системы</span><span class="sxs-lookup"><span data-stu-id="05dd2-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="05dd2-149">Завершение сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="05dd2-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-150">SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="05dd2-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="05dd2-151">Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для сеанса.</span><span class="sxs-lookup"><span data-stu-id="05dd2-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-152">AdminServices</span><span class="sxs-lookup"><span data-stu-id="05dd2-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="05dd2-153">Возвращает указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="05dd2-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-154">ShowForm</span><span class="sxs-lookup"><span data-stu-id="05dd2-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="05dd2-155">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="05dd2-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="05dd2-156">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="05dd2-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="05dd2-157">Создает числовое маркера, который использует метод **ShowForm** для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="05dd2-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05dd2-158">См. также</span><span class="sxs-lookup"><span data-stu-id="05dd2-158">See also</span></span>



[<span data-ttu-id="05dd2-159">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="05dd2-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

