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
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434118"
---
# <a name="iprofadmin--iunknown"></a><span data-ttu-id="b62b5-103">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b62b5-103">IProfAdmin : IUnknown</span></span>

  
  
<span data-ttu-id="b62b5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b62b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b62b5-105">Поддерживает администрирование профилей.</span><span class="sxs-lookup"><span data-stu-id="b62b5-105">Supports the administration of profiles.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b62b5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b62b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="b62b5-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="b62b5-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="b62b5-108">Выставим:</span><span class="sxs-lookup"><span data-stu-id="b62b5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b62b5-109">Объект администрирования профилей</span><span class="sxs-lookup"><span data-stu-id="b62b5-109">Profile administration object</span></span>  <br/> |
|<span data-ttu-id="b62b5-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b62b5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b62b5-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b62b5-111">MAPI</span></span>  <br/> |
|<span data-ttu-id="b62b5-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b62b5-112">Called by:</span></span>  <br/> |<span data-ttu-id="b62b5-113">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="b62b5-113">Client applications</span></span>  <br/> |
|<span data-ttu-id="b62b5-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b62b5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b62b5-115">IID_IProfAdmin</span><span class="sxs-lookup"><span data-stu-id="b62b5-115">IID_IProfAdmin</span></span>  <br/> |
|<span data-ttu-id="b62b5-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b62b5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b62b5-117">LPPROFADMIN</span><span class="sxs-lookup"><span data-stu-id="b62b5-117">LPPROFADMIN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b62b5-118">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="b62b5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b62b5-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b62b5-119">GetLastError</span></span>](iprofadmin-getlasterror.md) <br/> |<span data-ttu-id="b62b5-120">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования профиля.</span><span class="sxs-lookup"><span data-stu-id="b62b5-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error that occurred to a profile administration object.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-121">GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="b62b5-121">GetProfileTable</span></span>](iprofadmin-getprofiletable.md) <br/> |<span data-ttu-id="b62b5-122">Предоставляет доступ к таблице профилей, которая содержит сведения обо всех доступных профилях.</span><span class="sxs-lookup"><span data-stu-id="b62b5-122">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-123">CreateProfile</span><span class="sxs-lookup"><span data-stu-id="b62b5-123">CreateProfile</span></span>](iprofadmin-createprofile.md) <br/> |<span data-ttu-id="b62b5-124">Создает новый профиль.</span><span class="sxs-lookup"><span data-stu-id="b62b5-124">Creates a new profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-125">DeleteProfile</span><span class="sxs-lookup"><span data-stu-id="b62b5-125">DeleteProfile</span></span>](iprofadmin-deleteprofile.md) <br/> |<span data-ttu-id="b62b5-126">Удаляет профиль.</span><span class="sxs-lookup"><span data-stu-id="b62b5-126">Deletes a profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-127">ChangeProfilePassword</span><span class="sxs-lookup"><span data-stu-id="b62b5-127">ChangeProfilePassword</span></span>](iprofadmin-changeprofilepassword.md) <br/> |<span data-ttu-id="b62b5-128">Устарело.</span><span class="sxs-lookup"><span data-stu-id="b62b5-128">Deprecated.</span></span> <span data-ttu-id="b62b5-129">Изменяет пароль для профиля.</span><span class="sxs-lookup"><span data-stu-id="b62b5-129">Changes the password for a profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-130">CopyProfile</span><span class="sxs-lookup"><span data-stu-id="b62b5-130">CopyProfile</span></span>](iprofadmin-copyprofile.md) <br/> |<span data-ttu-id="b62b5-131">Копирует профиль.</span><span class="sxs-lookup"><span data-stu-id="b62b5-131">Copies a profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-132">RenameProfile</span><span class="sxs-lookup"><span data-stu-id="b62b5-132">RenameProfile</span></span>](iprofadmin-renameprofile.md) <br/> |<span data-ttu-id="b62b5-133">Назначает новое имя для профиля.</span><span class="sxs-lookup"><span data-stu-id="b62b5-133">Assigns a new name to a profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-134">SetDefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b62b5-134">SetDefaultProfile</span></span>](iprofadmin-setdefaultprofile.md) <br/> |<span data-ttu-id="b62b5-135">Задает или очищает профиль клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b62b5-135">Sets or clears a client's default profile.</span></span>  <br/> |
|[<span data-ttu-id="b62b5-136">AdminServices</span><span class="sxs-lookup"><span data-stu-id="b62b5-136">AdminServices</span></span>](iprofadmin-adminservices.md) <br/> |<span data-ttu-id="b62b5-137">Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="b62b5-137">Provides access to a message service administration object for making changes to the message services in a profile.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b62b5-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b62b5-138">See also</span></span>



[<span data-ttu-id="b62b5-139">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b62b5-139">MAPI Interfaces</span></span>](mapi-interfaces.md)

