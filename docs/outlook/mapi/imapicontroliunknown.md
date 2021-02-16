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
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414041"
---
# <a name="imapicontrol--iunknown"></a><span data-ttu-id="3dc43-103">IMAPIControl : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3dc43-103">IMAPIControl : IUnknown</span></span>

  
  
<span data-ttu-id="3dc43-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3dc43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3dc43-105">Включает и отключает кнопку и выполняет задачи, когда пользователь клиентского приложения щелкает включенный.</span><span class="sxs-lookup"><span data-stu-id="3dc43-105">Enables and disables a button control, and performs tasks when a user of a client application clicks the enabled control.</span></span> <span data-ttu-id="3dc43-106">Поставщики услуг реализуют объекты управления для создания пользовательских кнопок в диалоговых окнах, таких как таблицы свойств конфигурации, определяемые с помощью таблиц отображения.</span><span class="sxs-lookup"><span data-stu-id="3dc43-106">Service providers implement control objects to create custom buttons on dialog boxes, such as configuration property sheets, that are defined by using display tables.</span></span> 
  
<span data-ttu-id="3dc43-107">Дополнительные сведения о работе с таблицами отображения и объектами управления см. [в таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="3dc43-107">For more information about how to work with display tables and control objects, see [Display Tables](display-tables.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3dc43-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3dc43-108">Header file:</span></span>  <br/> |<span data-ttu-id="3dc43-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3dc43-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3dc43-110">Выставим:</span><span class="sxs-lookup"><span data-stu-id="3dc43-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3dc43-111">Объекты управления</span><span class="sxs-lookup"><span data-stu-id="3dc43-111">Control objects</span></span>  <br/> |
|<span data-ttu-id="3dc43-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3dc43-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3dc43-113">Поставщики служб</span><span class="sxs-lookup"><span data-stu-id="3dc43-113">Service providers</span></span>  <br/> |
|<span data-ttu-id="3dc43-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3dc43-114">Called by:</span></span>  <br/> |<span data-ttu-id="3dc43-115">MAPI</span><span class="sxs-lookup"><span data-stu-id="3dc43-115">MAPI</span></span>  <br/> |
|<span data-ttu-id="3dc43-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3dc43-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3dc43-117">IID_IMAPIControl</span><span class="sxs-lookup"><span data-stu-id="3dc43-117">IID_IMAPIControl</span></span>  <br/> |
|<span data-ttu-id="3dc43-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3dc43-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="3dc43-119">LPMAPICONTROL</span><span class="sxs-lookup"><span data-stu-id="3dc43-119">LPMAPICONTROL</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3dc43-120">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="3dc43-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3dc43-121">GetLastError</span><span class="sxs-lookup"><span data-stu-id="3dc43-121">GetLastError</span></span>](imapicontrol-getlasterror.md) <br/> |<span data-ttu-id="3dc43-122">Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке управления кнопкой.</span><span class="sxs-lookup"><span data-stu-id="3dc43-122">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous button control error.</span></span>  <br/> |
|[<span data-ttu-id="3dc43-123">Activate</span><span class="sxs-lookup"><span data-stu-id="3dc43-123">Activate</span></span>](imapicontrol-activate.md) <br/> |<span data-ttu-id="3dc43-124">Выполняет такую задачу, как отображение диалогового окна или запуск программной операции, когда пользователь клиентского приложения нажимает кнопку управления.</span><span class="sxs-lookup"><span data-stu-id="3dc43-124">Performs a task such as displaying a dialog box or starting a programmatic operation when a client application user clicks the button control.</span></span>  <br/> |
|[<span data-ttu-id="3dc43-125">GetState</span><span class="sxs-lookup"><span data-stu-id="3dc43-125">GetState</span></span>](imapicontrol-getstate.md) <br/> |<span data-ttu-id="3dc43-126">Извлекает значение, которое указывает, включен ли или отключен контроль кнопок.</span><span class="sxs-lookup"><span data-stu-id="3dc43-126">Retrieves a value that indicates whether the button control is enabled or disabled.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3dc43-127">См. также</span><span class="sxs-lookup"><span data-stu-id="3dc43-127">See also</span></span>



[<span data-ttu-id="3dc43-128">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3dc43-128">MAPI Interfaces</span></span>](mapi-interfaces.md)

