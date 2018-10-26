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
ms.openlocfilehash: 42d09fd92edf4dc221b73dac4948e78a7c6898ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589331"
---
# <a name="imapiprogress--iunknown"></a><span data-ttu-id="81b50-103">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81b50-103">IMAPIProgress : IUnknown</span></span>

  
  
<span data-ttu-id="81b50-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81b50-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81b50-105">Реализует объект хода выполнения, который предоставляет клиентских приложений с индикатором хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="81b50-105">Implements a progress object that provides client applications with a progress indicator.</span></span> <span data-ttu-id="81b50-106">Индикатор выполнения отображается пользовательский интерфейс, который показывает процент завершения операции, такие как копирование папок между хранилищами сообщений.</span><span class="sxs-lookup"><span data-stu-id="81b50-106">A progress indicator is a user-interface display that shows the percentage of completion of an operation, such as copying folders between message stores.</span></span> <span data-ttu-id="81b50-107">MAPI и клиентских приложениях внедрение объектов хода выполнения и их использовании поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="81b50-107">MAPI and client applications implement progress objects and service providers use them.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81b50-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="81b50-108">Header file:</span></span>  <br/> |<span data-ttu-id="81b50-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81b50-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="81b50-110">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="81b50-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="81b50-111">Объекты хода выполнения</span><span class="sxs-lookup"><span data-stu-id="81b50-111">Progress objects</span></span>  <br/> |
|<span data-ttu-id="81b50-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="81b50-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="81b50-113">MAPI и клиентских приложениях</span><span class="sxs-lookup"><span data-stu-id="81b50-113">MAPI and client applications</span></span>  <br/> |
|<span data-ttu-id="81b50-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="81b50-114">Called by:</span></span>  <br/> |<span data-ttu-id="81b50-115">Поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="81b50-115">Service providers</span></span>  <br/> |
|<span data-ttu-id="81b50-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="81b50-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="81b50-117">IID_IMAPIProgress</span><span class="sxs-lookup"><span data-stu-id="81b50-117">IID_IMAPIProgress</span></span>  <br/> |
|<span data-ttu-id="81b50-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="81b50-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="81b50-119">LPMAPIPROGRESS</span><span class="sxs-lookup"><span data-stu-id="81b50-119">LPMAPIPROGRESS</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="81b50-120">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="81b50-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="81b50-121">Ход выполнения</span><span class="sxs-lookup"><span data-stu-id="81b50-121">Progress</span></span>](imapiprogress-progress.md) <br/> |<span data-ttu-id="81b50-122">Обновляет индикатор хода выполнения с отображением хода выполнения после внесения до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="81b50-122">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span>  <br/> |
|[<span data-ttu-id="81b50-123">GetFlags</span><span class="sxs-lookup"><span data-stu-id="81b50-123">GetFlags</span></span>](imapiprogress-getflags.md) <br/> |<span data-ttu-id="81b50-124">Возвращает флаг, параметры из объекта о ходе выполнения для уровня операции, на котором рассчитывается сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="81b50-124">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>  <br/> |
|[<span data-ttu-id="81b50-125">GetMax</span><span class="sxs-lookup"><span data-stu-id="81b50-125">GetMax</span></span>](imapiprogress-getmax.md) <br/> |<span data-ttu-id="81b50-126">Возвращает максимальное число элементов в операции, для которых выполняется отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="81b50-126">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="81b50-127">GetMin</span><span class="sxs-lookup"><span data-stu-id="81b50-127">GetMin</span></span>](imapiprogress-getmin.md) <br/> |<span data-ttu-id="81b50-128">Возвращает минимальное значение в метод [SetLimits](imapiprogress-setlimits.md) , для которых выполняется отображаются сведения.</span><span class="sxs-lookup"><span data-stu-id="81b50-128">Returns the minimum value in the [SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span>  <br/> |
|[<span data-ttu-id="81b50-129">SetLimits</span><span class="sxs-lookup"><span data-stu-id="81b50-129">SetLimits</span></span>](imapiprogress-setlimits.md) <br/> |<span data-ttu-id="81b50-130">Задает нижний и верхний ограничения на число элементов в операции и флаги, определяющие порядок вычисления сведения о ходе выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="81b50-130">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81b50-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="81b50-131">Remarks</span></span>

<span data-ttu-id="81b50-132">MAPI включает параметр _lpProgress_ во многих методов, выполняющих потенциально длительных операций.</span><span class="sxs-lookup"><span data-stu-id="81b50-132">MAPI includes an  _lpProgress_ parameter in many of the methods that perform potentially lengthy operations.</span></span>  <span data-ttu-id="81b50-133">_lpProgress_ указывает реализации клиентского объекта хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="81b50-133">_lpProgress_ points to a client implementation of a progress object.</span></span> <span data-ttu-id="81b50-134">Клиенты, реализующие интерфейс **IMAPIProgress** установите для этого параметра для указания на их реализации; Клиенты, которые не реализует **IMAPIProgress** параметру значение NULL.</span><span class="sxs-lookup"><span data-stu-id="81b50-134">Clients that implement the **IMAPIProgress** interface set this parameter to point to their implementation; clients that do not implement **IMAPIProgress** set the parameter to NULL.</span></span> <span data-ttu-id="81b50-135">Чтобы отобразить индикатор выполнения во время обработки операции, поставщиков услуг использовать объект ход выполнения, полученных от клиента, если он доступен или для реализации интерфейса MAPI (указывается при _lpProgress_ имеет значение NULL).</span><span class="sxs-lookup"><span data-stu-id="81b50-135">To display a progress indicator during processing of the operation, service providers use the progress object supplied by the client, if available, or a MAPI implementation (indicated when  _lpProgress_ is set to NULL).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="81b50-136">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="81b50-136">MFCMAPI reference</span></span>

<span data-ttu-id="81b50-137">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="81b50-137">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="81b50-138">**Файлы**</span><span class="sxs-lookup"><span data-stu-id="81b50-138">**Files**</span></span>|<span data-ttu-id="81b50-139">**Функция**</span><span class="sxs-lookup"><span data-stu-id="81b50-139">**Function**</span></span>|<span data-ttu-id="81b50-140">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="81b50-140">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="81b50-141">MapiProgress.h и MapiProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="81b50-141">MapiProgress.h and MapiProgress.cpp</span></span>  <br/> |<span data-ttu-id="81b50-142">Не применимо</span><span class="sxs-lookup"><span data-stu-id="81b50-142">Not applicable</span></span>  <br/> |<span data-ttu-id="81b50-143">Если включен параметр IMAPIProgress mfcmapi (en) передает реализацию **IMAPIProgress** все функции, которые вызывает mfcmapi (en), который принимает реализацию.</span><span class="sxs-lookup"><span data-stu-id="81b50-143">If the IMAPIProgress setting is enabled, MFCMAPI will pass an **IMAPIProgress** implementation to all functions that MFCMAPI invokes that accept an implementation.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81b50-144">См. также</span><span class="sxs-lookup"><span data-stu-id="81b50-144">See also</span></span>



[<span data-ttu-id="81b50-145">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="81b50-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="81b50-146">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="81b50-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

