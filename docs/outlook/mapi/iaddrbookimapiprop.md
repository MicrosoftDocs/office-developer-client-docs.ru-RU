---
title: IAddrBook IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook
api_type:
- COM
ms.assetid: 9ccacbc0-10d5-40f9-a12b-d090a21d0d49
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e39f2603a1eef45c456b7fb58744b79c6b75f16
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808761"
---
# <a name="iaddrbook--imapiprop"></a><span data-ttu-id="b9649-103">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b9649-103">IAddrBook : IMAPIProp</span></span>

  
  
<span data-ttu-id="b9649-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b9649-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b9649-105">Поддерживает доступ к адресной книге MAPI, а также операции, такие как отображение общие диалоговые окна; Открытие контейнеров, системы обмена сообщениями пользователей и списки рассылки; и разрешение имен для выполнения.</span><span class="sxs-lookup"><span data-stu-id="b9649-105">Supports access to the MAPI address book and includes operations such as displaying common dialog boxes; opening containers, messaging users, and distribution lists; and performing name resolution.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9649-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b9649-106">Header file:</span></span>  <br/> |<span data-ttu-id="b9649-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b9649-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b9649-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="b9649-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b9649-109">Объекты адресной книги</span><span class="sxs-lookup"><span data-stu-id="b9649-109">Address book objects</span></span>  <br/> |
|<span data-ttu-id="b9649-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b9649-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b9649-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b9649-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b9649-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b9649-112">Called by:</span></span>  <br/> |<span data-ttu-id="b9649-113">Клиентские приложения, поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b9649-113">Client applications, service providers</span></span>  <br/> |
|<span data-ttu-id="b9649-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b9649-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b9649-115">IID_IAddrBook</span><span class="sxs-lookup"><span data-stu-id="b9649-115">IID_IAddrBook</span></span>  <br/> |
|<span data-ttu-id="b9649-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b9649-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b9649-117">LPADRBOOK</span><span class="sxs-lookup"><span data-stu-id="b9649-117">LPADRBOOK</span></span>  <br/> |
|<span data-ttu-id="b9649-118">Модель транзакций:</span><span class="sxs-lookup"><span data-stu-id="b9649-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="b9649-119">Не для записи</span><span class="sxs-lookup"><span data-stu-id="b9649-119">Not writable</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b9649-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="b9649-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b9649-121">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="b9649-121">OpenEntry</span></span>](iaddrbook-openentry.md) <br/> |<span data-ttu-id="b9649-122">Открывает запись книги и возвращает указатель на интерфейс, который можно использовать для доступа к операции.</span><span class="sxs-lookup"><span data-stu-id="b9649-122">Opens an address book entry and returns a pointer to an interface that can be used to access the entry.</span></span>  <br/> |
|[<span data-ttu-id="b9649-123">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="b9649-123">CompareEntryIDs</span></span>](iaddrbook-compareentryids.md) <br/> |<span data-ttu-id="b9649-124">Сравнение двух идентификаторы записей, относящихся к конкретной адресной книге, чтобы определить, является ли они ссылаются на один и тот же объект адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b9649-124">Compares two entry identifiers that belong to a particular address book provider to determine whether they refer to the same address book object.</span></span>  <br/> |
|[<span data-ttu-id="b9649-125">Уведомить</span><span class="sxs-lookup"><span data-stu-id="b9649-125">Advise</span></span>](iaddrbook-advise.md) <br/> |<span data-ttu-id="b9649-126">Регистрация клиента или поставщика для получения уведомлений об изменениях в одну или несколько записей в адресной книге.</span><span class="sxs-lookup"><span data-stu-id="b9649-126">Registers a client or service provider to receive notifications about changes to one or more entries in the address book.</span></span>  <br/> |
|[<span data-ttu-id="b9649-127">Unadvise</span><span class="sxs-lookup"><span data-stu-id="b9649-127">Unadvise</span></span>](iaddrbook-unadvise.md) <br/> |<span data-ttu-id="b9649-128">Отмена регистрации уведомлений, ранее созданные записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b9649-128">Cancels a notification registration previously established for an address book entry.</span></span>  <br/> |
|[<span data-ttu-id="b9649-129">CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b9649-129">CreateOneOff</span></span>](iaddrbook-createoneoff.md) <br/> |<span data-ttu-id="b9649-130">Создает запись идентификатор указывает адрес.</span><span class="sxs-lookup"><span data-stu-id="b9649-130">Creates an entry identifier for a one-off address.</span></span>  <br/> |
|[<span data-ttu-id="b9649-131">NewEntry</span><span class="sxs-lookup"><span data-stu-id="b9649-131">NewEntry</span></span>](iaddrbook-newentry.md) <br/> |<span data-ttu-id="b9649-132">Добавляет нового получателя контейнер адресной книги или списка получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b9649-132">Adds a new recipient to an address book container or to the recipient list of an outgoing message.</span></span>  <br/> |
|[<span data-ttu-id="b9649-133">ResolveName</span><span class="sxs-lookup"><span data-stu-id="b9649-133">ResolveName</span></span>](iaddrbook-resolvename.md) <br/> |<span data-ttu-id="b9649-134">Выполняет разрешение имен, назначение идентификаторов запись для получателей в список получателей.</span><span class="sxs-lookup"><span data-stu-id="b9649-134">Performs name resolution, assigning entry identifiers to recipients in a recipient list.</span></span>  <br/> |
|[<span data-ttu-id="b9649-135">Адрес</span><span class="sxs-lookup"><span data-stu-id="b9649-135">Address</span></span>](iaddrbook-address.md) <br/> |<span data-ttu-id="b9649-136">Отображает диалоговое окно Outlook адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b9649-136">Displays the Outlook address book dialog box.</span></span>  <br/> |
|[<span data-ttu-id="b9649-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="b9649-137">Details</span></span>](iaddrbook-details.md) <br/> |<span data-ttu-id="b9649-138">Отображает диалоговое окно, которое предоставляет подробные сведения о записи определенного адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b9649-138">Displays a dialog box that shows details about a particular address book entry.</span></span>  <br/> |
|<span data-ttu-id="b9649-139">**RecipOptions**</span><span class="sxs-lookup"><span data-stu-id="b9649-139">**RecipOptions**</span></span> <br/> | <span data-ttu-id="b9649-140">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="b9649-140">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="b9649-141">**QueryDefaultRecipOpt**</span><span class="sxs-lookup"><span data-stu-id="b9649-141">**QueryDefaultRecipOpt**</span></span> <br/> | <span data-ttu-id="b9649-142">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="b9649-142">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="b9649-143">GetPAB</span><span class="sxs-lookup"><span data-stu-id="b9649-143">GetPAB</span></span>](iaddrbook-getpab.md) <br/> |<span data-ttu-id="b9649-144">Возвращает идентификатор записи контейнера, который используется в качестве Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="b9649-144">Returns the entry identifier of the container that is designated as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b9649-145">SetPAB</span><span class="sxs-lookup"><span data-stu-id="b9649-145">SetPAB</span></span>](iaddrbook-setpab.md) <br/> |<span data-ttu-id="b9649-146">Назначает конкретным контейнером Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="b9649-146">Designates a particular container as the personal address book (PAB).</span></span>  <br/> |
|[<span data-ttu-id="b9649-147">GetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b9649-147">GetDefaultDir</span></span>](iaddrbook-getdefaultdir.md) <br/> |<span data-ttu-id="b9649-148">Возвращает идентификатор записи для контейнер начальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="b9649-148">Returns the entry identifier for the initial address book container.</span></span>  <br/> |
|[<span data-ttu-id="b9649-149">SetDefaultDir</span><span class="sxs-lookup"><span data-stu-id="b9649-149">SetDefaultDir</span></span>](iaddrbook-setdefaultdir.md) <br/> |<span data-ttu-id="b9649-150">Устанавливает указанный контейнер как контейнер адресной книги по умолчанию, который изначально становятся доступными.</span><span class="sxs-lookup"><span data-stu-id="b9649-150">Establishes the specified container as the default address book container that is initially made available.</span></span>  <br/> |
|[<span data-ttu-id="b9649-151">GetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b9649-151">GetSearchPath</span></span>](iaddrbook-getsearchpath.md) <br/> |<span data-ttu-id="b9649-152">Возвращает упорядоченный список идентификаторов запись контейнеров, которые будут включены в процесс разрешения имен, инициированных метод [ResolveName](iaddrbook-resolvename.md) .</span><span class="sxs-lookup"><span data-stu-id="b9649-152">Returns an ordered list of entry identifiers of the containers to be included in the name resolution process initiated by the [ResolveName](iaddrbook-resolvename.md) method.</span></span>  <br/> |
|[<span data-ttu-id="b9649-153">SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="b9649-153">SetSearchPath</span></span>](iaddrbook-setsearchpath.md) <br/> |<span data-ttu-id="b9649-154">Задает новый путь для поиска профиля, который используется для процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="b9649-154">Sets a new search path in the profile that is used for the name resolution process.</span></span>  <br/> |
|[<span data-ttu-id="b9649-155">PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="b9649-155">PrepareRecips</span></span>](iaddrbook-preparerecips.md) <br/> |<span data-ttu-id="b9649-156">Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b9649-156">Prepares a recipient list for later use by the messaging system.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b9649-157">См. также</span><span class="sxs-lookup"><span data-stu-id="b9649-157">See also</span></span>



[<span data-ttu-id="b9649-158">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b9649-158">MAPI Interfaces</span></span>](mapi-interfaces.md)

