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
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="d6b96-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6b96-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="d6b96-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d6b96-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d6b96-105">Добавляет режим простоя на основе функций [FNIDLE](fnidle.md) в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6b96-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d6b96-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="d6b96-106">Header file:</span></span>  <br/> |<span data-ttu-id="d6b96-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d6b96-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d6b96-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="d6b96-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d6b96-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d6b96-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d6b96-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="d6b96-110">Called by:</span></span>  <br/> |<span data-ttu-id="d6b96-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="d6b96-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="d6b96-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="d6b96-112">Parameters</span></span>

<span data-ttu-id="d6b96-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="d6b96-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="d6b96-114">[in] Указатель на режим простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="d6b96-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="d6b96-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="d6b96-116">[in] Указатель на блок памяти, который праздный двигатель должен передавать в качестве параметра режиму простоя при вызове.</span><span class="sxs-lookup"><span data-stu-id="d6b96-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="d6b96-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="d6b96-117">_priIdle_</span></span>
  
> <span data-ttu-id="d6b96-118">[in] Начальный приоритет для обычного простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="d6b96-119">Возможные приоритеты для процедур, определенных реализацией, больше или меньше нуля, но не ноль.</span><span class="sxs-lookup"><span data-stu-id="d6b96-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="d6b96-120">Нулевой приоритет зарезервирован для события пользователя, например щелчка мыши или WM_PAINT сообщения.</span><span class="sxs-lookup"><span data-stu-id="d6b96-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="d6b96-121">Приоритеты, более нулевые, представляют фоновые задачи, которые имеют более высокий приоритет, чем события пользователя, и отправляются в рамках стандартной Windows помпы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6b96-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="d6b96-122">Приоритеты менее нуля представляют задачи, которые работают только во время простоя насоса сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6b96-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="d6b96-123">Примеры приоритетов: 1 для представления переднего плана, 2 для вставки символов с изменением питания и 3 для скачивания новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="d6b96-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="d6b96-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="d6b96-124">_csecIdle_</span></span>
  
> <span data-ttu-id="d6b96-125">[in] Начальное значение времени, в сотые секунды, для использования при указании параметров простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="d6b96-126">Значение начального значения времени варьируется в зависимости от того, что передается в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="d6b96-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="d6b96-127">Значение может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="d6b96-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="d6b96-128">Минимальный период бездействия пользователей, который должен пройти до того, как простой двигатель MAPI впервые вызывает режим простоя, если флаг FIROWAIT установлен в _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="d6b96-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="d6b96-129">После этого времени, простаивающим двигателем можно вызвать праздный режим так часто, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="d6b96-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="d6b96-130">Минимальный интервал между вызовами в режим простоя, если флаг FIROINTERVAL задан в _iroIdle._</span><span class="sxs-lookup"><span data-stu-id="d6b96-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="d6b96-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="d6b96-131">_iroIdle_</span></span>
  
> <span data-ttu-id="d6b96-132">[in] Битмаска флагов, используемая для настройки начальных параметров обычного простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="d6b96-133">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d6b96-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="d6b96-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="d6b96-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="d6b96-135">Используйте этот флаг, чтобы указать, что простой обычный отметок времени не следует настраивать для сна или возобновления.</span><span class="sxs-lookup"><span data-stu-id="d6b96-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="d6b96-136">Поведение по умолчанию без этого флага в том, что время сна исключается при расчете просчитаного времени.</span><span class="sxs-lookup"><span data-stu-id="d6b96-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="d6b96-137">Если FIRONOADJUSTMENT передается, то при расчете пройденного времени включается время сна.</span><span class="sxs-lookup"><span data-stu-id="d6b96-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="d6b96-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="d6b96-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="d6b96-139">Режим простоя должен быть отключен при регистрации.</span><span class="sxs-lookup"><span data-stu-id="d6b96-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="d6b96-140">По умолчанию необходимо включить режим простоя при регистрации **ftgRegisterIdleRoutine.**</span><span class="sxs-lookup"><span data-stu-id="d6b96-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="d6b96-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="d6b96-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="d6b96-142">Время, указанное параметром  _csecIdle,_ — это минимальный интервал между последовательными вызовами в режим простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="d6b96-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="d6b96-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="d6b96-p107">Устаревший. Не используйте. </span><span class="sxs-lookup"><span data-stu-id="d6b96-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="d6b96-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="d6b96-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="d6b96-p108">Устаревший. Не используйте. </span><span class="sxs-lookup"><span data-stu-id="d6b96-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="d6b96-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="d6b96-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="d6b96-150">Время, указанное параметром  _csecIdle,_ — это минимальный период бездействия пользователя, который должен пройти до первого вызова простаивающим двигателем MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6b96-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="d6b96-151">После этого времени, простаивающим двигателем можно вызвать праздный режим так часто, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="d6b96-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d6b96-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6b96-152">Return value</span></span>

<span data-ttu-id="d6b96-153">Функция **FtgRegisterIdleRoutine** возвращает тег функции, определяющий режим простоя, добавленный в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6b96-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="d6b96-154">Если **FtgRegisterIdleRoutine** не может зарегистрировать режим простоя для клиентского приложения или поставщика услуг, например из-за проблем с памятью, он возвращает NULL.</span><span class="sxs-lookup"><span data-stu-id="d6b96-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d6b96-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="d6b96-155">Remarks</span></span>

<span data-ttu-id="d6b96-156">Следующие функции выполняются с простаивающим двигателем MAPI и простаивающим режимом на основе прототипа функции [FNIDLE.](fnidle.md)</span><span class="sxs-lookup"><span data-stu-id="d6b96-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="d6b96-157">**Простаиваемая рутинная функция**</span><span class="sxs-lookup"><span data-stu-id="d6b96-157">**Idle routine function**</span></span>|<span data-ttu-id="d6b96-158">**Использование**</span><span class="sxs-lookup"><span data-stu-id="d6b96-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6b96-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6b96-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="d6b96-160">Изменяет характеристики зарегистрированного режима простоя.</span><span class="sxs-lookup"><span data-stu-id="d6b96-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="d6b96-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6b96-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="d6b96-162">Удаляет зарегистрированную процедуру простоя из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6b96-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="d6b96-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="d6b96-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="d6b96-164">Отключает или повторно включает зарегистрированный режим простоя без удаления его из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="d6b96-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="d6b96-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="d6b96-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="d6b96-166">Добавляет праздную рутину в систему MAPI с ее включением или без нее.</span><span class="sxs-lookup"><span data-stu-id="d6b96-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="d6b96-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="d6b96-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="d6b96-168">Отключит простой движок MAPI для вызываемой программы.</span><span class="sxs-lookup"><span data-stu-id="d6b96-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="d6b96-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="d6b96-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="d6b96-170">Инициализирует простой двигатель MAPI для вызываемой заявки.</span><span class="sxs-lookup"><span data-stu-id="d6b96-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="d6b96-171">**ChangeIdleRoutine,** **DeregisterIdleRoutine** и **EnableIdleRoutine** принимают в качестве параметра ввода тег функции, возвращенный **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="d6b96-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="d6b96-172">Когда все задачи переднего плана для платформы простаивают, простаивающим двигателем MAPI называются самые приоритетные режимы простоя, готовые к выполнению.</span><span class="sxs-lookup"><span data-stu-id="d6b96-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="d6b96-173">Не гарантируется порядок вызова среди праздных режимов одного и того же приоритета.</span><span class="sxs-lookup"><span data-stu-id="d6b96-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="d6b96-174">Ниже приводится пример использования флага FIRONOADJUSTMENT в _параметре iroIdle._</span><span class="sxs-lookup"><span data-stu-id="d6b96-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="d6b96-175">Регистрация простоя с 5-минутной задержкой.</span><span class="sxs-lookup"><span data-stu-id="d6b96-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="d6b96-176">Hibernate/Sleep на компьютере через 1 минуту (4 минуты, оставленные на оттайке).</span><span class="sxs-lookup"><span data-stu-id="d6b96-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="d6b96-177">Возобновим работу компьютера через 10 минут.</span><span class="sxs-lookup"><span data-stu-id="d6b96-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="d6b96-178">Поведение по умолчанию, без FIRONOADJUSTMENT, является то, что вам по-прежнему придется ждать еще 4 минуты для выполнения рутины.</span><span class="sxs-lookup"><span data-stu-id="d6b96-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="d6b96-179">То есть, ваш timer был скорректирован, чтобы разрешить, как долго компьютер спал.</span><span class="sxs-lookup"><span data-stu-id="d6b96-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="d6b96-180">Однако, если вы передаете FIRONOADJUSTMENT, процедура простоя будет работать немедленно, так как прошло более 5 минут реального времени.</span><span class="sxs-lookup"><span data-stu-id="d6b96-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

