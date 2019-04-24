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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328289"
---
# <a name="imapisession--iunknown"></a><span data-ttu-id="f515e-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f515e-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="f515e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f515e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f515e-105">Управляет объектами, связанными с сеансом входа MAPI.</span><span class="sxs-lookup"><span data-stu-id="f515e-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f515e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="f515e-106">Header file:</span></span>  <br/> |<span data-ttu-id="f515e-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="f515e-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="f515e-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="f515e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f515e-109">Объекты Session</span><span class="sxs-lookup"><span data-stu-id="f515e-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="f515e-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f515e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f515e-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="f515e-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="f515e-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f515e-112">Called by:</span></span>  <br/> |<span data-ttu-id="f515e-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="f515e-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="f515e-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="f515e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f515e-115">Иид_имаписессион</span><span class="sxs-lookup"><span data-stu-id="f515e-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="f515e-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="f515e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f515e-117">ЛПМАПИСЕССИОН</span><span class="sxs-lookup"><span data-stu-id="f515e-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f515e-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="f515e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f515e-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="f515e-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="f515e-120">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="f515e-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="f515e-121">Жетмсгсторестабле</span><span class="sxs-lookup"><span data-stu-id="f515e-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="f515e-122">Предоставляет доступ к таблице хранилища сообщений, в которой содержатся сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="f515e-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="f515e-123">Опенмсгсторе</span><span class="sxs-lookup"><span data-stu-id="f515e-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="f515e-124">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="f515e-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f515e-125">Опенаддрессбук</span><span class="sxs-lookup"><span data-stu-id="f515e-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="f515e-126">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="f515e-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f515e-127">Опенпрофилесектион</span><span class="sxs-lookup"><span data-stu-id="f515e-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="f515e-128">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="f515e-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f515e-129">Жетстатустабле</span><span class="sxs-lookup"><span data-stu-id="f515e-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="f515e-130">Предоставляет доступ к таблице Status (таблица), в которой содержатся сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="f515e-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="f515e-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="f515e-132">Открывает объект и возвращает указатель интерфейса для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="f515e-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="f515e-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="f515e-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="f515e-134">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="f515e-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="f515e-135">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="f515e-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="f515e-136">Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="f515e-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="f515e-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="f515e-138">ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **advise** .</span><span class="sxs-lookup"><span data-stu-id="f515e-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="f515e-139">**Мессажеоптионс**</span><span class="sxs-lookup"><span data-stu-id="f515e-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="f515e-140">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="f515e-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="f515e-141">**Куеридефаултмессажеопт**</span><span class="sxs-lookup"><span data-stu-id="f515e-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="f515e-142">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="f515e-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="f515e-143">Енумадртипес</span><span class="sxs-lookup"><span data-stu-id="f515e-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="f515e-144">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="f515e-144">Deprecated.</span></span> <span data-ttu-id="f515e-145">Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="f515e-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-146">Куеридентити</span><span class="sxs-lookup"><span data-stu-id="f515e-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="f515e-147">Возвращает идентификатор записи объекта, который предоставляет основной идентификатор для сеанса.</span><span class="sxs-lookup"><span data-stu-id="f515e-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="f515e-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="f515e-149">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="f515e-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-150">Сетдефаултсторе</span><span class="sxs-lookup"><span data-stu-id="f515e-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="f515e-151">Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="f515e-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="f515e-152">Админсервицес</span><span class="sxs-lookup"><span data-stu-id="f515e-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="f515e-153">Возвращает указатель [имсгсервицеадмин](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f515e-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="f515e-154">Шовформ</span><span class="sxs-lookup"><span data-stu-id="f515e-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="f515e-155">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="f515e-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="f515e-156">Препареформ</span><span class="sxs-lookup"><span data-stu-id="f515e-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="f515e-157">Создает числовой маркер, который метод **шовформ** использует для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="f515e-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f515e-158">См. также</span><span class="sxs-lookup"><span data-stu-id="f515e-158">See also</span></span>



[<span data-ttu-id="f515e-159">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="f515e-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

