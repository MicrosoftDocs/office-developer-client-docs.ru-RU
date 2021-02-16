---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418523"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="187bf-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="187bf-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="187bf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="187bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="187bf-105">Добавляет процедуру бездействия на основе функций [FNIDLE](fnidle.md) в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="187bf-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="187bf-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="187bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="187bf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="187bf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="187bf-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="187bf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="187bf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="187bf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="187bf-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="187bf-110">Called by:</span></span>  <br/> |<span data-ttu-id="187bf-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="187bf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="187bf-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="187bf-112">Parameters</span></span>

<span data-ttu-id="187bf-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="187bf-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="187bf-114">[in] Указатель на процедуру бездействия.</span><span class="sxs-lookup"><span data-stu-id="187bf-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="187bf-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="187bf-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="187bf-116">[in] Указатель на блок памяти, который механизм бездействия должен передать в качестве параметра в процедуру простоя при его вызове.</span><span class="sxs-lookup"><span data-stu-id="187bf-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="187bf-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="187bf-117">_priIdle_</span></span>
  
> <span data-ttu-id="187bf-118">[in] Начальный приоритет для процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="187bf-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="187bf-119">Возможные приоритеты для процедур, определяемой реализацией, больше или меньше нуля, но не нуль.</span><span class="sxs-lookup"><span data-stu-id="187bf-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="187bf-120">Нулевой приоритет зарезервирован для события пользователя, например щелчка мыши или WM_PAINT сообщения.</span><span class="sxs-lookup"><span data-stu-id="187bf-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="187bf-121">Приоритеты больше нуля представляют фоновые задачи, которые имеют более высокий приоритет, чем события пользователя, и отправляются в рамках стандартного цикла циклов сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="187bf-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="187bf-122">Приоритеты меньше нуля представляют задачи бездействия, которые запускались только во время простоя сообщения.</span><span class="sxs-lookup"><span data-stu-id="187bf-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="187bf-123">Примеры приоритетов: 1 для отправки на переднем плане, 2 для вставки символов питания и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="187bf-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="187bf-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="187bf-124">_csecIdle_</span></span>
  
> <span data-ttu-id="187bf-125">[in] Начальное значение времени (в сотых секундах), используемого для указания параметров процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="187bf-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="187bf-126">Значение начального значения времени зависит от того, что передается в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="187bf-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="187bf-127">Значением может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="187bf-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="187bf-128">Минимальный период бездействия пользователя, который должен пройти до первого вызова процедуры простоя MAPI, если флаг FIROWAIT установлен в _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="187bf-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="187bf-129">По идентности этого времени механизм бездействия может вызывать процедуру простоя по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="187bf-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="187bf-130">Минимальный интервал между вызовами процедуры простоя, если флаг FIROINTERVAL установлен _в iroIdle._</span><span class="sxs-lookup"><span data-stu-id="187bf-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="187bf-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="187bf-131">_iroIdle_</span></span>
  
> <span data-ttu-id="187bf-132">[in] Битоваяmas флагов, используемая для настройки начальных параметров процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="187bf-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="187bf-133">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="187bf-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="187bf-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="187bf-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="187bf-135">Используйте этот флаг, чтобы указать, что не следует настраивать обычное время ожидания для спящий режим или возобновления работы.</span><span class="sxs-lookup"><span data-stu-id="187bf-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="187bf-136">По умолчанию без этого флага время спящий режим исключается при расчете времени, за которое у вас исчислялось.</span><span class="sxs-lookup"><span data-stu-id="187bf-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="187bf-137">Если fiRONOADJUSTMENT передается, то при вычислении затмило время сна.</span><span class="sxs-lookup"><span data-stu-id="187bf-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="187bf-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="187bf-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="187bf-139">Процедуру простоя следует отключить при регистрации.</span><span class="sxs-lookup"><span data-stu-id="187bf-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="187bf-140">Действие по умолчанию — включить процедуру простоя, когда **FtgRegisterIdleRoutine** регистрирует ее.</span><span class="sxs-lookup"><span data-stu-id="187bf-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="187bf-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="187bf-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="187bf-142">Время, заданное параметром  _csecIdle,_ — это минимальный интервал между последовательными вызовами процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="187bf-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="187bf-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="187bf-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="187bf-144">Устаревшее.</span><span class="sxs-lookup"><span data-stu-id="187bf-144">Obsolete.</span></span> <span data-ttu-id="187bf-145">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="187bf-145">Do not use.</span></span> 
      
  <span data-ttu-id="187bf-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="187bf-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="187bf-147">Устаревшее.</span><span class="sxs-lookup"><span data-stu-id="187bf-147">Obsolete.</span></span> <span data-ttu-id="187bf-148">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="187bf-148">Do not use.</span></span> 
      
  <span data-ttu-id="187bf-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="187bf-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="187bf-150">Время, заданное параметром  _csecIdle,_ — это минимальный период бездействия пользователя, который должен пройти, прежде чем механизм бездействия MAPI в первый раз вызывает процедуру простоя.</span><span class="sxs-lookup"><span data-stu-id="187bf-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="187bf-151">По идентности этого времени механизм бездействия может вызывать процедуру простоя по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="187bf-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="187bf-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="187bf-152">Return value</span></span>

<span data-ttu-id="187bf-153">Функция **FtgRegisterIdleRoutine** возвращает тег функции, определяющий процедуру бездействия, добавленную в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="187bf-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="187bf-154">Если **FtgRegisterIdleRoutine** не удается зарегистрировать процедуру бездействия для клиентского приложения или поставщика услуг, например из-за проблем с памятью, возвращается NULL.</span><span class="sxs-lookup"><span data-stu-id="187bf-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="187bf-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="187bf-155">Remarks</span></span>

<span data-ttu-id="187bf-156">Следующие функции работают с механизмом бездействия MAPI и процедурами бездействия на основе прототипа функции [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="187bf-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="187bf-157">**Простаиваемая подпрограмма**</span><span class="sxs-lookup"><span data-stu-id="187bf-157">**Idle routine function**</span></span>|<span data-ttu-id="187bf-158">**Использование**</span><span class="sxs-lookup"><span data-stu-id="187bf-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="187bf-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="187bf-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="187bf-160">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="187bf-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="187bf-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="187bf-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="187bf-162">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="187bf-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="187bf-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="187bf-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="187bf-164">Отключает или повторно включает зарегистрированную процедуру бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="187bf-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="187bf-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="187bf-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="187bf-166">Добавляет процедуру бездействия в систему MAPI с включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="187bf-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="187bf-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="187bf-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="187bf-168">Выключает механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="187bf-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="187bf-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="187bf-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="187bf-170">Инициализирует механизм бездействия MAPI для вызывающим приложением.</span><span class="sxs-lookup"><span data-stu-id="187bf-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="187bf-171">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве входного параметра тег функции, возвращенный **FtgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="187bf-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="187bf-172">Когда все задачи переднего плана для платформы простаивают, механизм бездействия MAPI вызывает процедуру простоя с наивысшим приоритетом, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="187bf-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="187bf-173">Порядок вызовов между процедурами бездействия с одинаковым приоритетом не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="187bf-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="187bf-174">Ниже приводится пример использования флага FIRONOADJUSTMENT в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="187bf-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="187bf-175">Зарегистрируйте процедуру простоя с 5-минутной задержкой.</span><span class="sxs-lookup"><span data-stu-id="187bf-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="187bf-176">Гибернайте или спящий режим компьютера через 1 минуту (4 минуты на стороне времени).</span><span class="sxs-lookup"><span data-stu-id="187bf-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="187bf-177">Возобновит работу компьютера через 10 минут.</span><span class="sxs-lookup"><span data-stu-id="187bf-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="187bf-178">По умолчанию без FIRONOADJUSTMENT вам все равно придется подождать 4 минуты, чтобы запустить процедуру.</span><span class="sxs-lookup"><span data-stu-id="187bf-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="187bf-179">То есть ваш timer был настроен для того, чтобы разрешить, сколько времени компьютер заснул.</span><span class="sxs-lookup"><span data-stu-id="187bf-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="187bf-180">Однако если передать FIRONOADJUSTMENT, процедура простоя будет немедленно запускаться, так как прошло более 5 минут реального времени.</span><span class="sxs-lookup"><span data-stu-id="187bf-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

