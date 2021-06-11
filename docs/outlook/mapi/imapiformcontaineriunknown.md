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
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407531"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="978f5-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="978f5-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="978f5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="978f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="978f5-105">Управляет формами в библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="978f5-105">Manages forms in form libraries.</span></span> <span data-ttu-id="978f5-106">Этот интерфейс используется для создания библиотек форм, определенных приложениям.</span><span class="sxs-lookup"><span data-stu-id="978f5-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="978f5-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="978f5-107">Header file:</span></span>  <br/> |<span data-ttu-id="978f5-108">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="978f5-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="978f5-109">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="978f5-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="978f5-110">Объекты контейнера форм</span><span class="sxs-lookup"><span data-stu-id="978f5-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="978f5-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="978f5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="978f5-112">Поставщики библиотек форм</span><span class="sxs-lookup"><span data-stu-id="978f5-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="978f5-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="978f5-113">Called by:</span></span>  <br/> |<span data-ttu-id="978f5-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="978f5-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="978f5-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="978f5-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="978f5-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="978f5-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="978f5-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="978f5-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="978f5-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="978f5-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="978f5-119">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="978f5-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="978f5-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="978f5-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="978f5-121">Устанавливает форму в контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="978f5-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="978f5-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="978f5-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="978f5-123">Удаляет определенную форму из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="978f5-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="978f5-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="978f5-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="978f5-125">Устраняет класс сообщения в его форму в контейнере формы и возвращает информационный объект формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="978f5-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="978f5-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="978f5-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="978f5-127">Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.</span><span class="sxs-lookup"><span data-stu-id="978f5-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="978f5-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="978f5-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="978f5-129">Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="978f5-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="978f5-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="978f5-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="978f5-131">Возвращает имя отображения контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="978f5-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="978f5-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="978f5-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="978f5-133">Возвращает в объект контейнера формы структуру [MAPIERROR,](mapierror.md) содержащую сведения о предыдущей ошибке.</span><span class="sxs-lookup"><span data-stu-id="978f5-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="978f5-134">См. также</span><span class="sxs-lookup"><span data-stu-id="978f5-134">See also</span></span>



[<span data-ttu-id="978f5-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="978f5-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

