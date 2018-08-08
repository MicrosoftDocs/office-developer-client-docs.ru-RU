---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808908"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="c0ea9-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0ea9-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="c0ea9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c0ea9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c0ea9-105">Управление формами в библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-105">Manages forms in form libraries.</span></span> <span data-ttu-id="c0ea9-106">Этот интерфейс используется для создания библиотеки форм конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0ea9-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-107">Header file:</span></span>  <br/> |<span data-ttu-id="c0ea9-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="c0ea9-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="c0ea9-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="c0ea9-110">Объекты контейнера формы</span><span class="sxs-lookup"><span data-stu-id="c0ea9-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="c0ea9-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0ea9-112">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="c0ea9-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="c0ea9-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-113">Called by:</span></span>  <br/> |<span data-ttu-id="c0ea9-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="c0ea9-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="c0ea9-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c0ea9-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="c0ea9-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="c0ea9-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="c0ea9-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="c0ea9-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="c0ea9-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c0ea9-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="c0ea9-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c0ea9-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="c0ea9-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="c0ea9-121">Устанавливает формы в контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="c0ea9-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="c0ea9-123">Удаление определенной формы из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="c0ea9-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="c0ea9-125">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="c0ea9-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="c0ea9-127">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="c0ea9-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="c0ea9-129">Возвращает массив свойств, используемых все формы, установленные в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="c0ea9-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="c0ea9-131">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="c0ea9-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="c0ea9-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="c0ea9-133">Возвращает структуру [MAPIERROR](mapierror.md) , содержащую сведения об ошибке предыдущей появление объект контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="c0ea9-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0ea9-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c0ea9-134">See also</span></span>



[<span data-ttu-id="c0ea9-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="c0ea9-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

