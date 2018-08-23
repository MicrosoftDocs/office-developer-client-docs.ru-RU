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
ms.openlocfilehash: 1775e5ea79fc71ac64a4536d3866b9a75ed96a6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566278"
---
# <a name="ftgregisteridleroutine"></a><span data-ttu-id="202db-103">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="202db-103">FtgRegisterIdleRoutine</span></span>

<span data-ttu-id="202db-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="202db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="202db-105">Добавляет [FNIDLE](fnidle.md) на основе функции простоя подпрограммы в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="202db-105">Adds a [FNIDLE](fnidle.md) function-based idle routine to the MAPI system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="202db-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="202db-106">Header file:</span></span>  <br/> |<span data-ttu-id="202db-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="202db-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="202db-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="202db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="202db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="202db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="202db-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="202db-110">Called by:</span></span>  <br/> |<span data-ttu-id="202db-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="202db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a><span data-ttu-id="202db-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="202db-112">Parameters</span></span>

<span data-ttu-id="202db-113">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="202db-113">_pfnIdle_</span></span>
  
> <span data-ttu-id="202db-114">[in] Указатель на простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="202db-114">[in] A pointer to the idle routine.</span></span> 
    
<span data-ttu-id="202db-115">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="202db-115">_pvIdleParam_</span></span>
  
> <span data-ttu-id="202db-116">[in] Указатель на блок памяти, который ядро простоя следует передать в качестве параметра простоя процедуру при ее вызове.</span><span class="sxs-lookup"><span data-stu-id="202db-116">[in] A pointer to a block of memory that the idle engine should pass as a parameter to the idle routine when it calls it.</span></span> 
    
<span data-ttu-id="202db-117">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="202db-117">_priIdle_</span></span>
  
> <span data-ttu-id="202db-118">[in] Начальный приоритет для бездействующих процедуры.</span><span class="sxs-lookup"><span data-stu-id="202db-118">[in] The initial priority for the idle routine.</span></span> <span data-ttu-id="202db-119">Возможных приоритетов для реализации процедуры больше или меньше, чем нулю, но не ноль.</span><span class="sxs-lookup"><span data-stu-id="202db-119">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="202db-120">Ноль приоритет зарезервирован для событие пользователя, например, одним щелчком мыши или сообщение WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="202db-120">The zero priority is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="202db-121">Приоритеты больше нуля представляют фоновых задач, которые имеют более высокий приоритет, чем событий пользователя и отправляется как часть стандартного цикла обработки сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="202db-121">Priorities greater than zero represent background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="202db-122">Приоритеты меньше нуля представляют простоя задачи, на которых выполняется только во время простоя приема-передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="202db-122">Priorities less than zero represent idle tasks that only run during message pump idle time.</span></span> <span data-ttu-id="202db-123">Приведены примеры приоритетов: 1 для отправки переднего плана, 2 для вставки символ power Правка и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="202db-123">Examples of priorities are as follows: 1 for foreground submission, 2 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="202db-124">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="202db-124">_csecIdle_</span></span>
  
> <span data-ttu-id="202db-125">[in] Значение начального времени в сотые доли секунды, для использования в указания простоя стандартных параметров.</span><span class="sxs-lookup"><span data-stu-id="202db-125">[in] The initial time value, in hundredths of a second, to be used in specifying idle routine parameters.</span></span> <span data-ttu-id="202db-126">Смысл значения начальное время, может изменяться в зависимости от того, что передается в параметре _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="202db-126">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="202db-127">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="202db-127">The meaning can be one of the following:</span></span> 
    
  - <span data-ttu-id="202db-128">Минимальный период бездействия со стороны пользователя, которое должно пройти перед MAPI простоя механизм вызывает простоя подпрограммы в первый раз, если флаг FIROWAIT установлен в _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="202db-128">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="202db-129">По истечении этого времени простоя модуль может вызывать простоя процедуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="202db-129">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="202db-130">Минимальный интервал между вызовами простоя процедуру, если флаг FIROINTERVAL установлен в _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="202db-130">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="202db-131">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="202db-131">_iroIdle_</span></span>
  
> <span data-ttu-id="202db-132">[in] Битовая маска, которая используется для задания начальных параметров для бездействующих подпрограммы флагов.</span><span class="sxs-lookup"><span data-stu-id="202db-132">[in] The bitmask of flags used to set initial options for the idle routine.</span></span> <span data-ttu-id="202db-133">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="202db-133">The following flags can be set:</span></span>
    
  <span data-ttu-id="202db-134">FIRONOADJUSTMENT</span><span class="sxs-lookup"><span data-stu-id="202db-134">FIRONOADJUSTMENT</span></span>
    
  > <span data-ttu-id="202db-135">Используйте этот флаг, чтобы указать, что таймер простоя процедуры не быть настроены для спящего режима или возобновления.</span><span class="sxs-lookup"><span data-stu-id="202db-135">Use this flag to specify that the idle routine timer should not be adjusted for sleep or resume.</span></span> <span data-ttu-id="202db-136">Поведение по умолчанию без этот флаг является то, что время бездействия исключен при расчете затраченное время.</span><span class="sxs-lookup"><span data-stu-id="202db-136">The default behavior without this flag is that sleep time is excluded when calculating the elapsed time.</span></span> <span data-ttu-id="202db-137">Если передается FIRONOADJUSTMENT затем время бездействия включен при расчете времени, затраченного.</span><span class="sxs-lookup"><span data-stu-id="202db-137">If FIRONOADJUSTMENT is passed then the sleep time is included when calculating elapsed time.</span></span>
      
  <span data-ttu-id="202db-138">FIRODISABLED</span><span class="sxs-lookup"><span data-stu-id="202db-138">FIRODISABLED</span></span>
    
  > <span data-ttu-id="202db-139">Простоя процедура должна быть отключена при регистрации.</span><span class="sxs-lookup"><span data-stu-id="202db-139">The idle routine should be disabled when registered.</span></span> <span data-ttu-id="202db-140">Действие по умолчанию — для включения простоя подпрограммы, когда он регистрирует **FtgRegisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="202db-140">The default action is to enable the idle routine when **FtgRegisterIdleRoutine** registers it.</span></span> 
      
  <span data-ttu-id="202db-141">FIROINTERVAL</span><span class="sxs-lookup"><span data-stu-id="202db-141">FIROINTERVAL</span></span> 
    
  > <span data-ttu-id="202db-142">Время, указанное в параметре _csecIdle_ — это минимальный интервал между последовательными вызовами простоя процедуру.</span><span class="sxs-lookup"><span data-stu-id="202db-142">The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  <span data-ttu-id="202db-143">FIROONCEONLY</span><span class="sxs-lookup"><span data-stu-id="202db-143">FIROONCEONLY</span></span> 
    
  > <span data-ttu-id="202db-p107">Устаревший. Не используйте. </span><span class="sxs-lookup"><span data-stu-id="202db-p107">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="202db-146">FIROPERBLOCK</span><span class="sxs-lookup"><span data-stu-id="202db-146">FIROPERBLOCK</span></span> 
    
  > <span data-ttu-id="202db-p108">Устаревший. Не используйте. </span><span class="sxs-lookup"><span data-stu-id="202db-p108">Obsolete. Do not use.</span></span> 
      
  <span data-ttu-id="202db-149">FIROWAIT</span><span class="sxs-lookup"><span data-stu-id="202db-149">FIROWAIT</span></span> 
    
  > <span data-ttu-id="202db-150">Время, указанное в параметре _csecIdle_ — это минимальный период бездействия со стороны пользователя, которое должно пройти перед простоя подсистемы MAPI вызывает простоя подпрограмму в первый раз.</span><span class="sxs-lookup"><span data-stu-id="202db-150">The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="202db-151">По истечении этого времени простоя модуль может вызывать простоя процедуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="202db-151">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="202db-152">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="202db-152">Return value</span></span>

<span data-ttu-id="202db-153">Функция **FtgRegisterIdleRoutine** возвращает функция тег, идентифицирующий простоя подпрограммы, который был добавлен в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="202db-153">The **FtgRegisterIdleRoutine** function returns a function tag identifying the idle routine that was added to the MAPI system.</span></span> <span data-ttu-id="202db-154">Если **FtgRegisterIdleRoutine** невозможно зарегистрировать простоя подпрограммы для клиентского приложения или поставщик услуг, например из-за проблем с памяти, он возвращает значение NULL.</span><span class="sxs-lookup"><span data-stu-id="202db-154">If **FtgRegisterIdleRoutine** cannot register the idle routine for the client application or service provider, for example because of memory problems, it returns NULL.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="202db-155">Замечания</span><span class="sxs-lookup"><span data-stu-id="202db-155">Remarks</span></span>

<span data-ttu-id="202db-156">Следующие функции работы с простоя подсистемы MAPI и простоя процедуры на основании прототипа функции [FNIDLE](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="202db-156">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype.</span></span> 
  
|<span data-ttu-id="202db-157">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="202db-157">**Idle routine function**</span></span>|<span data-ttu-id="202db-158">**Использование**</span><span class="sxs-lookup"><span data-stu-id="202db-158">**Usage**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="202db-159">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="202db-159">ChangeIdleRoutine</span></span>](changeidleroutine.md) <br/> |<span data-ttu-id="202db-160">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="202db-160">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="202db-161">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="202db-161">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="202db-162">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="202db-162">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="202db-163">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="202db-163">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="202db-164">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="202db-164">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|<span data-ttu-id="202db-165">**FtgRegisterIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="202db-165">**FtgRegisterIdleRoutine**</span></span> <br/> |<span data-ttu-id="202db-166">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="202db-166">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="202db-167">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="202db-167">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="202db-168">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="202db-168">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="202db-169">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="202db-169">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="202db-170">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="202db-170">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="202db-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="202db-171">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="202db-172">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="202db-172">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="202db-173">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="202db-173">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  
<span data-ttu-id="202db-174">Ниже приведен пример использования флага FIRONOADJUSTMENT с помощью параметра _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="202db-174">The following is an example of using the FIRONOADJUSTMENT flag in the  _iroIdle_ parameter.</span></span> 
  
1. <span data-ttu-id="202db-175">Регистрация простоя подпрограммы с задержкой 5 минут.</span><span class="sxs-lookup"><span data-stu-id="202db-175">Register an idle routine with a 5 minute delay.</span></span>
    
2. <span data-ttu-id="202db-176">Спящий режим/спящий компьютер после 1 минута (4 минуты остаются на таймер).</span><span class="sxs-lookup"><span data-stu-id="202db-176">Hibernate/Sleep the computer after 1 minute (4 minutes left on the timer).</span></span>
    
3. <span data-ttu-id="202db-177">Возобновление компьютере 10 минут.</span><span class="sxs-lookup"><span data-stu-id="202db-177">Resume the computer 10 minutes later.</span></span>
    
<span data-ttu-id="202db-178">Поведение по умолчанию, без FIRONOADJUSTMENT, является то, что вы по-прежнему ожидания 4 несколько минут для процедуру для запуска.</span><span class="sxs-lookup"><span data-stu-id="202db-178">The default behavior, without FIRONOADJUSTMENT, is that you still have to wait 4 more minutes for your routine to run.</span></span> <span data-ttu-id="202db-179">То есть таймера было изменено о предоставлении как долго компьютер был находится в спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="202db-179">That is, your timer was adjusted to allow for how long the computer was asleep.</span></span> <span data-ttu-id="202db-180">Тем не менее если передать FIRONOADJUSTMENT простоя подпрограммы будет выполняться сразу же из-за истечения более 5 минут режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="202db-180">However, if you pass FIRONOADJUSTMENT your idle routine will run immediately because more than 5 minutes of real time have elapsed.</span></span>
  

