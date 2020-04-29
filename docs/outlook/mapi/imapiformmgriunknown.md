---
title: Имапиформмгр IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413061"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="9b48d-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b48d-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="9b48d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b48d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b48d-105">Позволяет читателям форм получать сведения о серверах форм и активировать их.</span><span class="sxs-lookup"><span data-stu-id="9b48d-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b48d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9b48d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b48d-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="9b48d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9b48d-108">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="9b48d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9b48d-109">Объекты диспетчера форм</span><span class="sxs-lookup"><span data-stu-id="9b48d-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="9b48d-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="9b48d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9b48d-111">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="9b48d-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="9b48d-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="9b48d-112">Called by:</span></span>  <br/> |<span data-ttu-id="9b48d-113">Средства просмотра форм</span><span class="sxs-lookup"><span data-stu-id="9b48d-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="9b48d-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9b48d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9b48d-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="9b48d-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="9b48d-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="9b48d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9b48d-117">лпмапиформмгр</span><span class="sxs-lookup"><span data-stu-id="9b48d-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9b48d-118">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="9b48d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9b48d-119">лоадформ</span><span class="sxs-lookup"><span data-stu-id="9b48d-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="9b48d-120">Запускает форму, чтобы открыть существующее сообщение.</span><span class="sxs-lookup"><span data-stu-id="9b48d-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-121">ресолвемессажекласс</span><span class="sxs-lookup"><span data-stu-id="9b48d-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="9b48d-122">Разрешает класс сообщения в форму в контейнере формы и возвращает объект сведений о форме для этой формы.</span><span class="sxs-lookup"><span data-stu-id="9b48d-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-123">ресолвемултиплемессажеклассес</span><span class="sxs-lookup"><span data-stu-id="9b48d-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="9b48d-124">Разрешает группу классов сообщений в свои формы в контейнере формы и возвращает массив объектов данных формы для этих форм.</span><span class="sxs-lookup"><span data-stu-id="9b48d-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-125">калкформпропсет</span><span class="sxs-lookup"><span data-stu-id="9b48d-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="9b48d-126">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="9b48d-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="9b48d-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="9b48d-128">Запускает форму, чтобы создать новое сообщение на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="9b48d-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-129">селектформ</span><span class="sxs-lookup"><span data-stu-id="9b48d-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="9b48d-130">Отображает диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект сведений о форме, который описывает эту форму.</span><span class="sxs-lookup"><span data-stu-id="9b48d-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-131">селектмултиплеформс</span><span class="sxs-lookup"><span data-stu-id="9b48d-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="9b48d-132">Отображает диалоговое окно, позволяющее пользователю выбрать несколько форм и возвратить массив объектов сведений о форме, описывающих эти формы.</span><span class="sxs-lookup"><span data-stu-id="9b48d-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-133">селектформконтаинер</span><span class="sxs-lookup"><span data-stu-id="9b48d-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="9b48d-134">Отображает диалоговое окно, позволяющее пользователю выбрать контейнер формы и возврат интерфейса для объекта контейнера, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="9b48d-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-135">опенформконтаинер</span><span class="sxs-lookup"><span data-stu-id="9b48d-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="9b48d-136">Открывает интерфейс [имапиформконтаинер](imapiformcontaineriunknown.md) для определенного контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="9b48d-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-137">препареформ</span><span class="sxs-lookup"><span data-stu-id="9b48d-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="9b48d-138">Загружает форму для открытия.</span><span class="sxs-lookup"><span data-stu-id="9b48d-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-139">исинконфликт</span><span class="sxs-lookup"><span data-stu-id="9b48d-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="9b48d-140">Определяет, может ли форма обрабатывать свои собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b48d-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="9b48d-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9b48d-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="9b48d-142">Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="9b48d-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b48d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="9b48d-143">See also</span></span>



[<span data-ttu-id="9b48d-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="9b48d-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

