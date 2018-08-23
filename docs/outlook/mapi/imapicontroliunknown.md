---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 80acb1a1e4663a68efc4692ab67ec27bc369f4b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566518"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="87ef5-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87ef5-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="87ef5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87ef5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87ef5-105">Включает и отключает элемент управления button и выполняет щелчку клиентского приложения включено элемента управления.</span><span class="sxs-lookup"><span data-stu-id="87ef5-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="87ef5-106">Поставщики услуг реализовать объекты элементов управления для создания настраиваемых кнопок в диалоговых окнах, таких как страницы свойств конфигурации, определенные с помощью таблиц отображения.</span><span class="sxs-lookup"><span data-stu-id="87ef5-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="87ef5-107">Дополнительные сведения о том, как для работы с таблицами отображения и управлять объектами можно [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="87ef5-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87ef5-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="87ef5-108">Header file:</span></span>  <br/> |<span data-ttu-id="87ef5-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="87ef5-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="87ef5-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="87ef5-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="87ef5-111">Объекты элементов управления</span><span class="sxs-lookup"><span data-stu-id="87ef5-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="87ef5-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="87ef5-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="87ef5-113">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="87ef5-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="87ef5-114">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="87ef5-114">Called by:</span></span>  <br/> |<span data-ttu-id="87ef5-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="87ef5-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="87ef5-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="87ef5-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="87ef5-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="87ef5-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="87ef5-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="87ef5-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="87ef5-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="87ef5-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="87ef5-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="87ef5-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="87ef5-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="87ef5-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="87ef5-122">Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего элемента управления кнопка.</span><span class="sxs-lookup"><span data-stu-id="87ef5-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="87ef5-123">Активация</span><span class="sxs-lookup"><span data-stu-id="87ef5-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="87ef5-124">Выполняет задачи, как отображение диалогового окна или запуск программный операции при нажатии элемента управления кнопка пользователе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="87ef5-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="87ef5-125">GetState</span><span class="sxs-lookup"><span data-stu-id="87ef5-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="87ef5-126">Получает значение, указывающее, включено ли элемент управления button.</span><span class="sxs-lookup"><span data-stu-id="87ef5-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87ef5-127">См. также</span><span class="sxs-lookup"><span data-stu-id="87ef5-127">See also</span></span>



[<span data-ttu-id="87ef5-128">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="87ef5-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

