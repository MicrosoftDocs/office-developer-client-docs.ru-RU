---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418269"
---
# <a name="changeidleroutine"></a><span data-ttu-id="a4c52-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a4c52-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="a4c52-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4c52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4c52-105">Изменяет некоторые или все характеристики процедуры бездействия на основе [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="a4c52-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a4c52-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="a4c52-106">Header file:</span></span>  <br/> |<span data-ttu-id="a4c52-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a4c52-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a4c52-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="a4c52-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a4c52-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a4c52-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a4c52-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="a4c52-110">Called by:</span></span>  <br/> |<span data-ttu-id="a4c52-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="a4c52-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a><span data-ttu-id="a4c52-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4c52-112">Parameters</span></span>

<span data-ttu-id="a4c52-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="a4c52-113">_ftg_</span></span>
  
> <span data-ttu-id="a4c52-114">[in] Тег функции, определяя процедуру бездействия.</span><span class="sxs-lookup"><span data-stu-id="a4c52-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="a4c52-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="a4c52-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="a4c52-116">[in] Указатель на процедуру бездействия.</span><span class="sxs-lookup"><span data-stu-id="a4c52-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="a4c52-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="a4c52-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="a4c52-118">[in] Указатель на новый блок памяти, который реализация вызова выделяет для процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="a4c52-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="a4c52-119">_priIdle_</span></span>
  
> <span data-ttu-id="a4c52-120">[in] Значение, представляющее новый приоритет для процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="a4c52-121">Возможные приоритеты для процедур, определяемой реализацией, больше или меньше нуля, но не нуль.</span><span class="sxs-lookup"><span data-stu-id="a4c52-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="a4c52-122">Нулевое значение зарезервировано для события пользователя, например щелчка мыши или WM_PAINT сообщения.</span><span class="sxs-lookup"><span data-stu-id="a4c52-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="a4c52-123">Значения больше нуля представляют приоритеты для фоновых задач, которые имеют более высокий приоритет, чем события пользователя, и отправляются в рамках стандартного цикла зациклки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="a4c52-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="a4c52-124">Значения меньше нуля представляют приоритеты для задач бездейства, которые запускались только во время простоя сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4c52-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="a4c52-125">Примеры приоритетов: 1 для отправки на переднем плане, 1 для вставки символов питания и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="a4c52-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="a4c52-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="a4c52-126">_csecIdle_</span></span>
  
> <span data-ttu-id="a4c52-127">[in] Новое время (в сотых секундах) для применения к процедуре простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="a4c52-128">Значение начального значения времени зависит от того, что передается в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="a4c52-129">Это может быть:</span><span class="sxs-lookup"><span data-stu-id="a4c52-129">It can be:</span></span> 
    
  - <span data-ttu-id="a4c52-130">Минимальный период бездействия пользователя, который должен пройти до первого вызова процедуры простоя MAPI, если флаг FIROWAIT установлен в _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="a4c52-131">По идентности этого времени механизм бездействия может вызывать процедуру простоя по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a4c52-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="a4c52-132">Минимальный интервал между вызовами процедуры простоя, если флаг FIROINTERVAL установлен _в iroIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="a4c52-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="a4c52-133">_iroIdle_</span></span>
  
> <span data-ttu-id="a4c52-134">[in] Битоваяmas флагов, обозначающее новые параметры вызова процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="a4c52-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="a4c52-135">Необходимо установить только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="a4c52-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="a4c52-136">FIROINTERVAL: время, заданное параметром  _csecIdle,_ — это минимальный интервал между последовательными вызовами процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="a4c52-137">FIROONCEONLY: устаревшее.</span><span class="sxs-lookup"><span data-stu-id="a4c52-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="a4c52-138">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="a4c52-138">Do not use.</span></span> 
      
  - <span data-ttu-id="a4c52-139">FIROPERBLOCK: устаревшее.</span><span class="sxs-lookup"><span data-stu-id="a4c52-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="a4c52-140">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="a4c52-140">Do not use.</span></span> 
      
  - <span data-ttu-id="a4c52-141">FIROWAIT: время, заданное параметром  _csecIdle,_ — это минимальный период бездействия пользователя, который должен пройти, прежде чем механизм бездействия MAPI впервые вызывает процедуру простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="a4c52-142">По идентности этого времени механизм бездействия может вызывать процедуру простоя по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="a4c52-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="a4c52-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="a4c52-143">_ircIdle_</span></span>
  
> <span data-ttu-id="a4c52-144">[in] Битоваяmas флагов, используемых для того, чтобы указать изменения, которые необходимо внести в процедуру простоя.</span><span class="sxs-lookup"><span data-stu-id="a4c52-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="a4c52-145">Следующие флаги можно установить в любом сочетании:</span><span class="sxs-lookup"><span data-stu-id="a4c52-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="a4c52-146">FIRCCSEC: изменение времени, связанного с процедурой простоя, то есть изменение, обозначенное значением, переданным в _параметре csecIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="a4c52-147">FIRCКЛЮЧЕВЫХ: изменение параметров процедуры простоя, то есть изменение, заданное значением, переданным в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="a4c52-148">FIRCPFN: изменение указателя процедуры бездействия, то есть изменение, заданное значением, переданным в _параметре pfnIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="a4c52-149">FIRCPRI: изменение приоритета процедуры простоя, то есть изменение, заданное значением, переданным в _параметре priIdle._</span><span class="sxs-lookup"><span data-stu-id="a4c52-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="a4c52-150">FIRCPV: изменение блока памяти процедуры простоя, то есть изменение, заданное значением, переданным в _параметре pvIdleParam._</span><span class="sxs-lookup"><span data-stu-id="a4c52-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a4c52-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4c52-151">Return value</span></span>

<span data-ttu-id="a4c52-152">Нет.</span><span class="sxs-lookup"><span data-stu-id="a4c52-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4c52-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="a4c52-153">Remarks</span></span>

<span data-ttu-id="a4c52-154">Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE:](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="a4c52-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="a4c52-155">**Простаиваемая подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="a4c52-155">**Idle routine function**</span></span>|<span data-ttu-id="a4c52-156">**Использование**</span><span class="sxs-lookup"><span data-stu-id="a4c52-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a4c52-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="a4c52-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="a4c52-158">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="a4c52-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="a4c52-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a4c52-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="a4c52-160">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4c52-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a4c52-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a4c52-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="a4c52-162">Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="a4c52-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="a4c52-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="a4c52-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="a4c52-164">Добавляет процедуру бездействия в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="a4c52-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="a4c52-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="a4c52-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="a4c52-166">Выключает механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="a4c52-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="a4c52-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="a4c52-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="a4c52-168">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="a4c52-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="a4c52-169">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="a4c52-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="a4c52-170">Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="a4c52-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="a4c52-171">Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a4c52-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

