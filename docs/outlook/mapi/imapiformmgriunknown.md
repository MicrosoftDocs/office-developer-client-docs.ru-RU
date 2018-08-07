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
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808951"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="b2fae-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2fae-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="b2fae-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b2fae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b2fae-105">Включение средств просмотра формы для получения информации о и активации серверов формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2fae-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b2fae-106">Header file:</span></span>  <br/> |<span data-ttu-id="b2fae-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b2fae-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b2fae-108">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="b2fae-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b2fae-109">Объекты диспетчер форм</span><span class="sxs-lookup"><span data-stu-id="b2fae-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="b2fae-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b2fae-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b2fae-111">Поставщики библиотеки форм</span><span class="sxs-lookup"><span data-stu-id="b2fae-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="b2fae-112">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b2fae-112">Called by:</span></span>  <br/> |<span data-ttu-id="b2fae-113">Средства просмотра формы</span><span class="sxs-lookup"><span data-stu-id="b2fae-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="b2fae-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b2fae-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b2fae-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="b2fae-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="b2fae-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b2fae-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="b2fae-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="b2fae-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b2fae-118">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="b2fae-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b2fae-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="b2fae-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="b2fae-120">Запускает существующее сообщение при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="b2fae-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="b2fae-122">Разрешает класс сообщения в его формы в контейнере формы и возвращает объект сведения формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b2fae-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="b2fae-124">Разрешает группу классов сообщений в формах в контейнере формы и возвращает массив формы объекты для этих форм.</span><span class="sxs-lookup"><span data-stu-id="b2fae-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b2fae-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="b2fae-126">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="b2fae-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="b2fae-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="b2fae-128">Открывает форму для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="b2fae-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="b2fae-130">Предоставляет диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект данные формы с описанием данной форме.</span><span class="sxs-lookup"><span data-stu-id="b2fae-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="b2fae-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="b2fae-132">Предоставляет диалоговое окно, которое позволяет пользователю выбрать нескольких форм и возвращает массив формы объекты, которые описывают формах.</span><span class="sxs-lookup"><span data-stu-id="b2fae-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="b2fae-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="b2fae-134">Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="b2fae-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="b2fae-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="b2fae-136">Откроется интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для контейнера конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="b2fae-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="b2fae-138">Файлы для загрузки для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b2fae-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="b2fae-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="b2fae-140">Определяет ли формы можно обработать собственный конфликтов сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2fae-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="b2fae-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b2fae-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="b2fae-142">Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объект диспетчер форм.</span><span class="sxs-lookup"><span data-stu-id="b2fae-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2fae-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b2fae-143">See also</span></span>



[<span data-ttu-id="b2fae-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b2fae-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

