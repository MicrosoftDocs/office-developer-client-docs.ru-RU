---
title: IMAPIFormMgr IUnknown
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
ms.openlocfilehash: b4eaf424bd22f5cb7f40778d81a18cca0ef1dcc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581519"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="23ce3-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23ce3-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="23ce3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="23ce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="23ce3-105">Включение средств просмотра формы для получения информации о и активации серверов формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23ce3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="23ce3-106">Header file:</span></span>  <br/> |<span data-ttu-id="23ce3-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="23ce3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="23ce3-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="23ce3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="23ce3-109">Объекты диспетчер форм</span><span class="sxs-lookup"><span data-stu-id="23ce3-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="23ce3-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="23ce3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="23ce3-111">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="23ce3-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="23ce3-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="23ce3-112">Called by:</span></span>  <br/> |<span data-ttu-id="23ce3-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="23ce3-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="23ce3-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="23ce3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="23ce3-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="23ce3-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="23ce3-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="23ce3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="23ce3-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="23ce3-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="23ce3-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="23ce3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="23ce3-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="23ce3-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="23ce3-120">Запускает существующее сообщение при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="23ce3-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="23ce3-122">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="23ce3-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="23ce3-124">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="23ce3-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="23ce3-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="23ce3-126">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="23ce3-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="23ce3-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="23ce3-128">Открывает форму для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="23ce3-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="23ce3-130">Предоставляет диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект данные формы с описанием данной форме.</span><span class="sxs-lookup"><span data-stu-id="23ce3-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="23ce3-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="23ce3-132">Предоставляет диалоговое окно, которое позволяет пользователю выбрать нескольких форм и возвращает массив формы объекты, которые описывают формах.</span><span class="sxs-lookup"><span data-stu-id="23ce3-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="23ce3-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="23ce3-134">Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="23ce3-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="23ce3-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="23ce3-136">Откроется интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для контейнера конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="23ce3-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="23ce3-138">Файлы для загрузки для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="23ce3-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="23ce3-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="23ce3-140">Определяет ли формы можно обработать собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="23ce3-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="23ce3-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="23ce3-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="23ce3-142">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объект диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="23ce3-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23ce3-143">См. также</span><span class="sxs-lookup"><span data-stu-id="23ce3-143">See also</span></span>



[<span data-ttu-id="23ce3-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="23ce3-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

