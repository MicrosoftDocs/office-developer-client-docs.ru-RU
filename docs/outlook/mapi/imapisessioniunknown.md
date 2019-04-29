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
# <a name="imapisession--iunknown"></a><span data-ttu-id="ed5b1-103">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed5b1-103">IMAPISession : IUnknown</span></span>

  
  
<span data-ttu-id="ed5b1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed5b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed5b1-105">Управляет объектами, связанными с сеансом входа MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-105">Manages objects associated with a MAPI logon session.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed5b1-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="ed5b1-107">Мапикс. h</span><span class="sxs-lookup"><span data-stu-id="ed5b1-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ed5b1-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ed5b1-109">Объекты Session</span><span class="sxs-lookup"><span data-stu-id="ed5b1-109">Session objects</span></span>  <br/> |
|<span data-ttu-id="ed5b1-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ed5b1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ed5b1-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ed5b1-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-112">Called by:</span></span>  <br/> |<span data-ttu-id="ed5b1-113">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="ed5b1-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="ed5b1-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ed5b1-115">Иид_имаписессион</span><span class="sxs-lookup"><span data-stu-id="ed5b1-115">IID_IMAPISession</span></span>  <br/> |
|<span data-ttu-id="ed5b1-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ed5b1-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ed5b1-117">ЛПМАПИСЕССИОН</span><span class="sxs-lookup"><span data-stu-id="ed5b1-117">LPMAPISESSION</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ed5b1-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="ed5b1-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ed5b1-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ed5b1-119">GetLastError</span></span>](imapisession-getlasterror.md) <br/> |<span data-ttu-id="ed5b1-120">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous session error.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-121">Жетмсгсторестабле</span><span class="sxs-lookup"><span data-stu-id="ed5b1-121">GetMsgStoresTable</span></span>](imapisession-getmsgstorestable.md) <br/> |<span data-ttu-id="ed5b1-122">Предоставляет доступ к таблице хранилища сообщений, в которой содержатся сведения обо всех хранилищах сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-122">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-123">Опенмсгсторе</span><span class="sxs-lookup"><span data-stu-id="ed5b1-123">OpenMsgStore</span></span>](imapisession-openmsgstore.md) <br/> |<span data-ttu-id="ed5b1-124">Открывает хранилище сообщений и возвращает указатель [IMsgStore](imsgstoreimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-124">Opens a message store and returns an [IMsgStore](imsgstoreimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-125">Опенаддрессбук</span><span class="sxs-lookup"><span data-stu-id="ed5b1-125">OpenAddressBook</span></span>](imapisession-openaddressbook.md) <br/> |<span data-ttu-id="ed5b1-126">Открывает интегрированную адресную книгу MAPI, возвращая указатель [IAddrBook](iaddrbookimapiprop.md) для получения доступа.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-126">Opens the MAPI integrated address book, returning an [IAddrBook](iaddrbookimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-127">Опенпрофилесектион</span><span class="sxs-lookup"><span data-stu-id="ed5b1-127">OpenProfileSection</span></span>](imapisession-openprofilesection.md) <br/> |<span data-ttu-id="ed5b1-128">Открывает раздел текущего профиля и возвращает указатель [ипрофсект](iprofsectimapiprop.md) для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-128">Opens a section of the current profile and returns an [IProfSect](iprofsectimapiprop.md) pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-129">Жетстатустабле</span><span class="sxs-lookup"><span data-stu-id="ed5b1-129">GetStatusTable</span></span>](imapisession-getstatustable.md) <br/> |<span data-ttu-id="ed5b1-130">Предоставляет доступ к таблице Status (таблица), в которой содержатся сведения обо всех ресурсах MAPI в сеансе.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-130">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-131">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="ed5b1-131">OpenEntry</span></span>](imapisession-openentry.md) <br/> |<span data-ttu-id="ed5b1-132">Открывает объект и возвращает указатель интерфейса для получения дальнейших прав.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-132">Opens an object and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-133">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="ed5b1-133">CompareEntryIDs</span></span>](imapisession-compareentryids.md) <br/> |<span data-ttu-id="ed5b1-134">Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на один и тот же объект.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-134">Compares two entry identifiers to determine whether they refer to the same object.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-135">Рекомендуем</span><span class="sxs-lookup"><span data-stu-id="ed5b1-135">Advise</span></span>](imapisession-advise.md) <br/> |<span data-ttu-id="ed5b1-136">Регистрируется для получения уведомлений об указанных событиях, влияющих на сеанс.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-136">Registers to receive notification of specified events that affect the session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-137">Unadvise</span><span class="sxs-lookup"><span data-stu-id="ed5b1-137">Unadvise</span></span>](imapisession-unadvise.md) <br/> |<span data-ttu-id="ed5b1-138">ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **advise** .</span><span class="sxs-lookup"><span data-stu-id="ed5b1-138">Cancels the sending of notifications previously set up with a call to the **Advise** method.</span></span>  <br/> |
|<span data-ttu-id="ed5b1-139">**Мессажеоптионс**</span><span class="sxs-lookup"><span data-stu-id="ed5b1-139">**MessageOptions**</span></span> <br/> | <span data-ttu-id="ed5b1-140">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="ed5b1-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="ed5b1-141">**Куеридефаултмессажеопт**</span><span class="sxs-lookup"><span data-stu-id="ed5b1-141">**QueryDefaultMessageOpt**</span></span> <br/> | <span data-ttu-id="ed5b1-142">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="ed5b1-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-143">Енумадртипес</span><span class="sxs-lookup"><span data-stu-id="ed5b1-143">EnumAdrTypes</span></span>](imapisession-enumadrtypes.md) <br/> |<span data-ttu-id="ed5b1-144">Устаревшие.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-144">Deprecated.</span></span> <span data-ttu-id="ed5b1-145">Возвращает типы адресов, которые могут обрабатываться всеми поставщиками транспорта в сеансе.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-145">Returns the address types that can be handled by all of the transport providers in the session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-146">Куеридентити</span><span class="sxs-lookup"><span data-stu-id="ed5b1-146">QueryIdentity</span></span>](imapisession-queryidentity.md) <br/> |<span data-ttu-id="ed5b1-147">Возвращает идентификатор записи объекта, который предоставляет основной идентификатор для сеанса.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-147">Returns the entry identifier of the object that provides the primary identity for the session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-148">Logoff</span><span class="sxs-lookup"><span data-stu-id="ed5b1-148">Logoff</span></span>](imapisession-logoff.md) <br/> |<span data-ttu-id="ed5b1-149">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-149">Ends a MAPI session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-150">Сетдефаултсторе</span><span class="sxs-lookup"><span data-stu-id="ed5b1-150">SetDefaultStore</span></span>](imapisession-setdefaultstore.md) <br/> |<span data-ttu-id="ed5b1-151">Устанавливает хранилище сообщений в качестве хранилища сообщений по умолчанию для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-151">Establishes a message store as the default message store for the session.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-152">Админсервицес</span><span class="sxs-lookup"><span data-stu-id="ed5b1-152">AdminServices</span></span>](imapisession-adminservices.md) <br/> |<span data-ttu-id="ed5b1-153">Возвращает указатель [имсгсервицеадмин](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-153">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-154">Шовформ</span><span class="sxs-lookup"><span data-stu-id="ed5b1-154">ShowForm</span></span>](imapisession-showform.md) <br/> |<span data-ttu-id="ed5b1-155">Отображает форму.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-155">Displays a form.</span></span>  <br/> |
|[<span data-ttu-id="ed5b1-156">Препареформ</span><span class="sxs-lookup"><span data-stu-id="ed5b1-156">PrepareForm</span></span>](imapisession-prepareform.md) <br/> |<span data-ttu-id="ed5b1-157">Создает числовой маркер, который метод **шовформ** использует для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="ed5b1-157">Creates a numeric token that the **ShowForm** method uses to access a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed5b1-158">См. также</span><span class="sxs-lookup"><span data-stu-id="ed5b1-158">See also</span></span>



[<span data-ttu-id="ed5b1-159">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ed5b1-159">MAPI Interfaces</span></span>](mapi-interfaces.md)

