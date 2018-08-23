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
ms.openlocfilehash: 3f03412c9ab639678c68016ec1a8eff937b6c1a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590990"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="2255a-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2255a-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="2255a-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2255a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2255a-105">Управление формами в библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="2255a-105">Manages forms in form libraries.</span></span> <span data-ttu-id="2255a-106">Этот интерфейс используется для создания библиотеки форм конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="2255a-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2255a-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="2255a-107">Header file:</span></span>  <br/> |<span data-ttu-id="2255a-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="2255a-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2255a-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="2255a-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2255a-110">Объекты контейнера формы</span><span class="sxs-lookup"><span data-stu-id="2255a-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="2255a-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="2255a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2255a-112">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="2255a-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="2255a-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="2255a-113">Called by:</span></span>  <br/> |<span data-ttu-id="2255a-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="2255a-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="2255a-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="2255a-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2255a-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="2255a-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="2255a-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="2255a-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2255a-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="2255a-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2255a-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="2255a-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2255a-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="2255a-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="2255a-121">Устанавливает формы в контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="2255a-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="2255a-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="2255a-123">Удаление определенной формы из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="2255a-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="2255a-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="2255a-125">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="2255a-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="2255a-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="2255a-127">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="2255a-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="2255a-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="2255a-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="2255a-129">Возвращает массив свойств, используемых все формы, установленные в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="2255a-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="2255a-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="2255a-131">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="2255a-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2255a-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="2255a-133">Возвращает структуру [MAPIERROR](mapierror.md) , содержащую сведения об ошибке предыдущей появление объект контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="2255a-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2255a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2255a-134">See also</span></span>



[<span data-ttu-id="2255a-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="2255a-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

