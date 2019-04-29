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
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="5c68a-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5c68a-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="5c68a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c68a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c68a-105">Добавляет подпрограмму бездействия на основе функции [фнидле](fnidle.md) в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c68a-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c68a-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="5c68a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c68a-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="5c68a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5c68a-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="5c68a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c68a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c68a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c68a-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="5c68a-110">Called by:</span></span>  <br/> |<span data-ttu-id="5c68a-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="5c68a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="5c68a-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c68a-112">Parameters</span></span>

<span data-ttu-id="5c68a-113">_Пфнидле_</span><span class="sxs-lookup"><span data-stu-id="5c68a-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="5c68a-114">возврата Указатель на подпрограмму Idle.</span><span class="sxs-lookup"><span data-stu-id="5c68a-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="5c68a-115">_Пвидлепарам_</span><span class="sxs-lookup"><span data-stu-id="5c68a-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="5c68a-116">возврата Указатель на блок памяти, который антивирусная программа должна передать в качестве параметра в подпрограмму Idle при его вызове.</span><span class="sxs-lookup"><span data-stu-id="5c68a-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="5c68a-117">_Приидле_</span><span class="sxs-lookup"><span data-stu-id="5c68a-117">_priIdle_</span></span>
  
> <span data-ttu-id="5c68a-118">возврата Начальный приоритет для процедуры Idle.</span><span class="sxs-lookup"><span data-stu-id="5c68a-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="5c68a-119">Возможные приоритеты для подпрограмм, определенных при реализации, больше или меньше нуля, но не равны нулю.</span><span class="sxs-lookup"><span data-stu-id="5c68a-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="5c68a-120">Нулевой приоритет резервируется для события пользователя, такого как щелчок мыши или сообщение WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="5c68a-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="5c68a-121">Приоритеты больше нуля представляют фоновые задачи, которые имеют более высокий приоритет, чем события пользователя, и отправляются как часть стандартного цикла приема сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="5c68a-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="5c68a-122">Приоритеты, меньшие нуля, представляют неактивные задачи, выполняемые во время простоя при загрузке сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c68a-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="5c68a-123">Ниже приведены примеры приоритетов: 1 для отправки на передний план, 2 для вставки символов Power и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="5c68a-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="5c68a-124">_КсеЦидле_</span><span class="sxs-lookup"><span data-stu-id="5c68a-124">_csecIdle_</span></span>
  
> <span data-ttu-id="5c68a-125">возврата Начальное значение времени в сотых долях секунды, которое будет использоваться при указании параметров подпрограммы бездействия.</span><span class="sxs-lookup"><span data-stu-id="5c68a-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="5c68a-126">Значение начального значения времени может различаться в зависимости от того, что передается в параметре _ироидле_ .</span><span class="sxs-lookup"><span data-stu-id="5c68a-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="5c68a-127">Значение может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="5c68a-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="5c68a-128">Минимальный период действия пользователя, который должен пройти, прежде чем антивирусное ядро MAPI вызывает подпрограмму простоя в первый раз, если установлен флаг ФИРОВАИТ в _ироидле_.</span><span class="sxs-lookup"><span data-stu-id="5c68a-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="5c68a-129">По исТечении этого времени модуль простоя может вызывать процедуру простоя, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5c68a-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="5c68a-130">Минимальный интервал между вызовами процедуры Idle, если установлен флаг ФИРОИНТЕРВАЛ в _ироидле_.</span><span class="sxs-lookup"><span data-stu-id="5c68a-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="5c68a-131">_Ироидле_</span><span class="sxs-lookup"><span data-stu-id="5c68a-131">_iroIdle_</span></span>
  
> <span data-ttu-id="5c68a-132">возврата Битовая маска флагов, используемых для установки начальных параметров для процедуры Idle.</span><span class="sxs-lookup"><span data-stu-id="5c68a-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="5c68a-133">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5c68a-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="5c68a-134">ФИРОНОАДЖУСТМЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c68a-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="5c68a-135">Используйте этот флаг, чтобы указать, что таймер неактивной программы не должен быть скорректирован для спящего режима или возобновления.</span><span class="sxs-lookup"><span data-stu-id="5c68a-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="5c68a-136">Поведение по умолчанию без этого флага заключается в том, что при расчете затраченного времени исключается время сна.</span><span class="sxs-lookup"><span data-stu-id="5c68a-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="5c68a-137">Если ФИРОНОАДЖУСТМЕНТ передается, то время сна включается при расчете затраченного времени.</span><span class="sxs-lookup"><span data-stu-id="5c68a-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="5c68a-138">ФИРОДИСАБЛЕД</span><span class="sxs-lookup"><span data-stu-id="5c68a-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="5c68a-139">Подпрограмму периода бездействия следует отключить при регистрации.</span><span class="sxs-lookup"><span data-stu-id="5c68a-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="5c68a-140">Действие по умолчанию включает процедуру Idle, когда **фтгрегистеридлераутине** регистрирует ее.</span><span class="sxs-lookup"><span data-stu-id="5c68a-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="5c68a-141">ФИРОИНТЕРВАЛ</span><span class="sxs-lookup"><span data-stu-id="5c68a-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="5c68a-142">Время, заданное параметром _ксеЦидле_ , является минимальным интервалом между последовательными вызовами процедуры Idle.</span><span class="sxs-lookup"><span data-stu-id="5c68a-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="5c68a-143">ФИРУНЦЕОНЛИ</span><span class="sxs-lookup"><span data-stu-id="5c68a-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="5c68a-144">Устаревши.</span><span class="sxs-lookup"><span data-stu-id="5c68a-144">Obsolete.</span></span> <span data-ttu-id="5c68a-145">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="5c68a-145">Do not use.</span></span> 
      
  <span data-ttu-id="5c68a-146">ФИРОПЕРБЛОКК</span><span class="sxs-lookup"><span data-stu-id="5c68a-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="5c68a-147">Устаревши.</span><span class="sxs-lookup"><span data-stu-id="5c68a-147">Obsolete.</span></span> <span data-ttu-id="5c68a-148">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="5c68a-148">Do not use.</span></span> 
      
  <span data-ttu-id="5c68a-149">ФИРОВАИТ</span><span class="sxs-lookup"><span data-stu-id="5c68a-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="5c68a-150">Время, заданное параметром _ксеЦидле_ , является минимальным периодом действия пользователя, который должен пройти, прежде чем модуль бездействия MAPI вызывает подпрограмму бездействия в первый раз.</span><span class="sxs-lookup"><span data-stu-id="5c68a-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="5c68a-151">По исТечении этого времени модуль простоя может вызывать процедуру простоя, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="5c68a-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c68a-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c68a-152">Return value</span></span>

<span data-ttu-id="5c68a-153">Функция **фтгрегистеридлераутине** возвращает тег функции, определяющий подпрограмму Idle, добавленную в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c68a-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="5c68a-154">Если **фтгрегистеридлераутине** не может зарегистрировать подпрограмму Idle для клиентского приложения или поставщика услуг, например из-за проблем с памятью, возвращается значение null.</span><span class="sxs-lookup"><span data-stu-id="5c68a-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5c68a-155">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c68a-155">Remarks</span></span>

<span data-ttu-id="5c68a-156">Приведенные ниже функции работают с модулем бездействия MAPI и с процедурами простоя на основе прототипа функции [фнидле](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="5c68a-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="5c68a-157">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="5c68a-157">**Idle routine function**</span></span>|<span data-ttu-id="5c68a-158">**Usage**</span><span class="sxs-lookup"><span data-stu-id="5c68a-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c68a-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5c68a-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="5c68a-160">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="5c68a-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="5c68a-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5c68a-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="5c68a-162">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c68a-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="5c68a-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="5c68a-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="5c68a-164">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="5c68a-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="5c68a-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="5c68a-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="5c68a-166">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="5c68a-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="5c68a-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="5c68a-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="5c68a-168">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="5c68a-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="5c68a-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="5c68a-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="5c68a-170">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="5c68a-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="5c68a-171">**Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**.</span><span class="sxs-lookup"><span data-stu-id="5c68a-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="5c68a-172">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="5c68a-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="5c68a-173">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="5c68a-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="5c68a-174">Ниже приведен пример использования флага ФИРОНОАДЖУСТМЕНТ в параметре _ироидле_ .</span><span class="sxs-lookup"><span data-stu-id="5c68a-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="5c68a-175">Регистрация процедуры бездействия с 5 минутной задержкой.</span><span class="sxs-lookup"><span data-stu-id="5c68a-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="5c68a-176">Переход в спящий режим/режим сна компьютера через 1 минуту (4 минуты влево на таймер).</span><span class="sxs-lookup"><span data-stu-id="5c68a-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="5c68a-177">ВозОбновите работу компьютера спустя 10 минут.</span><span class="sxs-lookup"><span data-stu-id="5c68a-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="5c68a-178">Поведение по умолчанию, не ФИРОНОАДЖУСТМЕНТ, заключается в том, что для выполнения процедуры необходимо подождать 4 еще больше минут.</span><span class="sxs-lookup"><span data-stu-id="5c68a-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="5c68a-179">То есть ваш таймер был настроен таким образом, чтобы разрешить время, в течение которого компьютер находился в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="5c68a-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="5c68a-180">Тем не менее, если вы передаете ФИРОНОАДЖУСТМЕНТ, подпрограмму простоя будут выполняться немедленно, так как истечет более 5 минут реального времени.</span><span class="sxs-lookup"><span data-stu-id="5c68a-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

