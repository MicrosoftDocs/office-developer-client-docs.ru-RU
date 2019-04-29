---
title: IMAPIProgress IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress
api_type:
- COM
ms.assetid: 7a872296-0378-456f-b4d6-cb4d96b09d6e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3a3d54ac9485cc3915d3606bb84b4f3191d1ca5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419648"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="3ec7b-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ec7b-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="3ec7b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec7b-105">Реализует объект Progress, который предоставляет клиентские приложения с индикатором хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="3ec7b-106">Индикатор выполнения — это отображение пользовательского интерфейса, которое показывает процент выполнения операции, например копирование папок между хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="3ec7b-107">MAPI и клиентские приложения реализуют объекты хода выполнения, а поставщики услуг используют их.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ec7b-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-108">Header file:</span></span>  <br/> |<span data-ttu-id="3ec7b-109">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="3ec7b-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3ec7b-110">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="3ec7b-111">Объекты хода выполнения</span><span class="sxs-lookup"><span data-stu-id="3ec7b-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="3ec7b-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="3ec7b-113">MAPI и клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="3ec7b-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="3ec7b-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-114">Called by:</span></span>  <br/> |<span data-ttu-id="3ec7b-115">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="3ec7b-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="3ec7b-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3ec7b-117">Иид_имапипрогресс</span><span class="sxs-lookup"><span data-stu-id="3ec7b-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="3ec7b-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="3ec7b-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="3ec7b-119">ЛПМАПИПРОГРЕСС</span><span class="sxs-lookup"><span data-stu-id="3ec7b-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3ec7b-120">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="3ec7b-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3ec7b-121">Progress</span><span class="sxs-lookup"><span data-stu-id="3ec7b-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="3ec7b-122">Обновляет индикатор хода выполнения с отображением хода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="3ec7b-123">Флаги</span><span class="sxs-lookup"><span data-stu-id="3ec7b-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="3ec7b-124">Возвращает параметры флага из объекта Progress для уровня операции, на котором рассчитываются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="3ec7b-125">Жетмакс</span><span class="sxs-lookup"><span data-stu-id="3ec7b-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="3ec7b-126">Возвращает максимальное количество элементов в операции, для которых отображаются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3ec7b-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="3ec7b-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="3ec7b-128">Возвращает минимальное значение в методе [SetLimits](imapiprogress-setlimits.md) , для которого отображаются сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="3ec7b-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="3ec7b-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="3ec7b-130">Задает нижний и верхний пределы числа элементов в операции, а также флаги, которые контролируют способ вычисления сведений о ходе выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ec7b-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ec7b-131">Remarks</span></span>

<span data-ttu-id="3ec7b-132">MAPI включает параметр _лппрогресс_ во многих методах, которые выполняют потенциально длительные операции.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="3ec7b-133">_лппрогресс_ указывает на клиентскую реализацию объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="3ec7b-134">Клиенты, реализующие интерфейс **IMAPIProgress** , задают этот параметр, чтобы указать их реализацию; Клиенты, не реализующие **IMAPIProgress** , устанавливают для параметра значение null.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="3ec7b-135">Чтобы во время обработки операции отображался индикатор хода выполнения, поставщики услуг используют объект хода выполнения, предоставленный клиентом, если он доступен, или реализация MAPI (указывается, когда _лппрогресс_ имеет значение null).</span><span class="sxs-lookup"><span data-stu-id="3ec7b-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3ec7b-136">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3ec7b-136">MFCMAPI reference</span></span>

<span data-ttu-id="3ec7b-137">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3ec7b-138">**Files**</span><span class="sxs-lookup"><span data-stu-id="3ec7b-138">**Files**</span></span>|<span data-ttu-id="3ec7b-139">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3ec7b-139">**Function**</span></span>|<span data-ttu-id="3ec7b-140">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3ec7b-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ec7b-141">Мапипрогресс. h и Мапипрогресс. cpp</span><span class="sxs-lookup"><span data-stu-id="3ec7b-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="3ec7b-142">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3ec7b-142">Not applicable</span></span>  <br/> |<span data-ttu-id="3ec7b-143">Если параметр IMAPIProgress включен, то MFCMAPI передает реализацию **IMAPIProgress** всем функциям, которые MFCMAPI вызывают реализацию.</span><span class="sxs-lookup"><span data-stu-id="3ec7b-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ec7b-144">См. также</span><span class="sxs-lookup"><span data-stu-id="3ec7b-144">See also</span></span>



[<span data-ttu-id="3ec7b-145">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="3ec7b-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3ec7b-146">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="3ec7b-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

