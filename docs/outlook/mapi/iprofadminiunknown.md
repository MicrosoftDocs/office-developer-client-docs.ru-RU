---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577417"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="ab875-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ab875-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="ab875-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab875-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab875-105">Поддерживает управления профилями.</span><span class="sxs-lookup"><span data-stu-id="ab875-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ab875-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="ab875-106">Header file:</span></span>  <br/> |<span data-ttu-id="ab875-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="ab875-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="ab875-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="ab875-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ab875-109">Объект администрирования профилей</span><span class="sxs-lookup"><span data-stu-id="ab875-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="ab875-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="ab875-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ab875-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="ab875-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="ab875-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="ab875-112">Called by:</span></span>  <br/> |<span data-ttu-id="ab875-113">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="ab875-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="ab875-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ab875-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ab875-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="ab875-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="ab875-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="ab875-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ab875-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="ab875-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ab875-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="ab875-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ab875-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="ab875-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="ab875-120">Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли в объект администрирования профилей.</span><span class="sxs-lookup"><span data-stu-id="ab875-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="ab875-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="ab875-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="ab875-122">Предоставляет доступ к таблице профилей таблицу, содержащую сведения обо всех доступных профилей.</span><span class="sxs-lookup"><span data-stu-id="ab875-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="ab875-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="ab875-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="ab875-124">Создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="ab875-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="ab875-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="ab875-126">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="ab875-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="ab875-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="ab875-128">Рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="ab875-128">Deprecated.</span></span> <span data-ttu-id="ab875-129">Изменение пароля для профиля.</span><span class="sxs-lookup"><span data-stu-id="ab875-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="ab875-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="ab875-131">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="ab875-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="ab875-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="ab875-133">Назначает новое имя профиля.</span><span class="sxs-lookup"><span data-stu-id="ab875-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab875-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="ab875-135">Устанавливает или удаляет профиль клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ab875-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="ab875-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="ab875-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="ab875-137">Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="ab875-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab875-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ab875-138">See also</span></span>



[<span data-ttu-id="ab875-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ab875-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

