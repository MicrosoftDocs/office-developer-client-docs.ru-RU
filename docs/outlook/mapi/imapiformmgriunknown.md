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
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413061"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="3b5d7-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3b5d7-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="3b5d7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b5d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b5d7-105">Позволяет пользователям форм получать сведения о серверах форм и активировать их.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b5d7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-106">Header file:</span></span>  <br/> |<span data-ttu-id="3b5d7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="3b5d7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="3b5d7-108">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3b5d7-109">Объекты диспетчера форм</span><span class="sxs-lookup"><span data-stu-id="3b5d7-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="3b5d7-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3b5d7-111">Поставщики библиотек форм</span><span class="sxs-lookup"><span data-stu-id="3b5d7-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="3b5d7-112">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-112">Called by:</span></span>  <br/> |<span data-ttu-id="3b5d7-113">Просмотр форм</span><span class="sxs-lookup"><span data-stu-id="3b5d7-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="3b5d7-114">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3b5d7-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="3b5d7-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="3b5d7-116">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3b5d7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3b5d7-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="3b5d7-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3b5d7-118">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="3b5d7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3b5d7-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="3b5d7-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="3b5d7-120">Запускает форму для открытия существующего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="3b5d7-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="3b5d7-122">Устраняет класс сообщений в его форму в контейнере форм и возвращает информационный объект формы для этой формы.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="3b5d7-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="3b5d7-124">Устраняет группу классов сообщений в их формах в контейнере форм и возвращает массив информационных объектов форм для этих форм.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="3b5d7-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="3b5d7-126">Возвращает массив свойств, которые использует группа форм.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="3b5d7-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="3b5d7-128">Запускает форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="3b5d7-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="3b5d7-130">Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект информации о форме, описывая эту форму.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="3b5d7-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="3b5d7-132">Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив объектов информации о форме, описывая эти формы.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="3b5d7-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="3b5d7-134">Представляет диалоговое окно, которое позволяет пользователю выбрать контейнер формы и возвращает интерфейс для выбранного пользователем объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="3b5d7-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="3b5d7-136">Открывает интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для определенного контейнера форм.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="3b5d7-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="3b5d7-138">Скачивает форму для открытия.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="3b5d7-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="3b5d7-140">Определяет, может ли форма обрабатывать собственные конфликты сообщений.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="3b5d7-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3b5d7-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="3b5d7-142">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, возникной в объекте диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="3b5d7-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b5d7-143">См. также</span><span class="sxs-lookup"><span data-stu-id="3b5d7-143">See also</span></span>



[<span data-ttu-id="3b5d7-144">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3b5d7-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

