---
title: Имапиформконтаинер IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342191"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="263d8-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="263d8-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="263d8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="263d8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="263d8-105">Управляет формами в библиотеках форм.</span><span class="sxs-lookup"><span data-stu-id="263d8-105">Manages forms in form libraries.</span></span> <span data-ttu-id="263d8-106">Этот интерфейс используется для создания библиотек форм, характерных для приложений.</span><span class="sxs-lookup"><span data-stu-id="263d8-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="263d8-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="263d8-107">Header file:</span></span>  <br/> |<span data-ttu-id="263d8-108">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="263d8-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="263d8-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="263d8-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="263d8-110">Объекты контейнера формы</span><span class="sxs-lookup"><span data-stu-id="263d8-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="263d8-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="263d8-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="263d8-112">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="263d8-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="263d8-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="263d8-113">Called by:</span></span>  <br/> |<span data-ttu-id="263d8-114">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="263d8-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="263d8-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="263d8-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="263d8-116">Иид_имапиформконтаинер</span><span class="sxs-lookup"><span data-stu-id="263d8-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="263d8-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="263d8-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="263d8-118">ЛПМАПИФОРМКОНТАИНЕР</span><span class="sxs-lookup"><span data-stu-id="263d8-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="263d8-119">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="263d8-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="263d8-120">Инсталлформ</span><span class="sxs-lookup"><span data-stu-id="263d8-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="263d8-121">Устанавливает форму в контейнер форм.</span><span class="sxs-lookup"><span data-stu-id="263d8-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="263d8-122">Ремовеформ</span><span class="sxs-lookup"><span data-stu-id="263d8-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="263d8-123">Удаляет определенную форму из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="263d8-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="263d8-124">Ресолвемессажекласс</span><span class="sxs-lookup"><span data-stu-id="263d8-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="263d8-125">Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.</span><span class="sxs-lookup"><span data-stu-id="263d8-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="263d8-126">Ресолвемултиплемессажеклассес</span><span class="sxs-lookup"><span data-stu-id="263d8-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="263d8-127">Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="263d8-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="263d8-128">Калкформпропсет</span><span class="sxs-lookup"><span data-stu-id="263d8-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="263d8-129">Возвращает массив свойств, используемых всеми формами, установленными в контейнере форм.</span><span class="sxs-lookup"><span data-stu-id="263d8-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="263d8-130">Вывод на экран</span><span class="sxs-lookup"><span data-stu-id="263d8-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="263d8-131">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="263d8-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="263d8-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="263d8-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="263d8-133">Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения о предыдущей ошибке, возникшей в объекте контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="263d8-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="263d8-134">См. также</span><span class="sxs-lookup"><span data-stu-id="263d8-134">See also</span></span>



[<span data-ttu-id="263d8-135">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="263d8-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

