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
ms.openlocfilehash: 49682007946a4c5dda3800751deaebcc0e1e5740
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579454"
---
# <a name="changeidleroutine"></a><span data-ttu-id="85299-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="85299-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="85299-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85299-105">Изменяет некоторые или все характеристики простоя подпрограмма [FNIDLE](fnidle.md) на основе.</span><span class="sxs-lookup"><span data-stu-id="85299-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="85299-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="85299-106">Header file:</span></span>  <br/> |<span data-ttu-id="85299-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="85299-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="85299-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="85299-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85299-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85299-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85299-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="85299-110">Called by:</span></span>  <br/> |<span data-ttu-id="85299-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="85299-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="85299-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="85299-112">Parameters</span></span>

<span data-ttu-id="85299-113">_ftg_</span><span class="sxs-lookup"><span data-stu-id="85299-113">_ftg_</span></span>
  
> <span data-ttu-id="85299-114">[in] Функция тег, идентифицирующий простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="85299-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="85299-115">_pfnIdle_</span><span class="sxs-lookup"><span data-stu-id="85299-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="85299-116">[in] Указатель на простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="85299-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="85299-117">_pvIdleParam_</span><span class="sxs-lookup"><span data-stu-id="85299-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="85299-118">[in] Указатель на новый блок памяти, вызывающий реализации выделяет для бездействующих процедуры.</span><span class="sxs-lookup"><span data-stu-id="85299-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="85299-119">_priIdle_</span><span class="sxs-lookup"><span data-stu-id="85299-119">_priIdle_</span></span>
  
> <span data-ttu-id="85299-120">[in] Значение, представляющее новый приоритет для бездействующих процедуры.</span><span class="sxs-lookup"><span data-stu-id="85299-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="85299-121">Возможных приоритетов для реализации процедуры больше или меньше, чем нулю, но не ноль.</span><span class="sxs-lookup"><span data-stu-id="85299-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="85299-122">Нулевое значение зарезервировано для событие пользователя, например, одним щелчком мыши или сообщение WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="85299-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="85299-123">Приоритеты для фоновых задач, которые имеют более высокий приоритет, чем событий пользователя и отправляется как часть стандартного цикла обработки сообщений Windows представляют значения больше нуля.</span><span class="sxs-lookup"><span data-stu-id="85299-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="85299-124">Значения меньше, чем нулевой представляют приоритеты для бездействующих задачи, на которых выполняется только во время простоя обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="85299-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="85299-125">Примеры приоритетов: 1 для отправки переднего плана, 1 для вставки символ power Правка и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="85299-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="85299-126">_csecIdle_</span><span class="sxs-lookup"><span data-stu-id="85299-126">_csecIdle_</span></span>
  
> <span data-ttu-id="85299-127">[in] Время в сотые доли секунды, для применения к простоя подпрограммы новый.</span><span class="sxs-lookup"><span data-stu-id="85299-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="85299-128">Смысл значения начальное время, может изменяться в зависимости от того, что передается в параметре _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="85299-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="85299-129">Это может быть:</span><span class="sxs-lookup"><span data-stu-id="85299-129">It can be:</span></span> 
    
  - <span data-ttu-id="85299-130">Минимальный период бездействия со стороны пользователя, которое должно пройти перед MAPI простоя механизм вызывает простоя подпрограммы в первый раз, если флаг FIROWAIT установлен в _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="85299-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="85299-131">По истечении этого времени простоя модуль может вызывать простоя процедуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="85299-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="85299-132">Минимальный интервал между вызовами простоя процедуру, если флаг FIROINTERVAL установлен в _iroIdle_.</span><span class="sxs-lookup"><span data-stu-id="85299-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="85299-133">_iroIdle_</span><span class="sxs-lookup"><span data-stu-id="85299-133">_iroIdle_</span></span>
  
> <span data-ttu-id="85299-134">[in] Битовая маска, указывающее новые параметры для вызова простоя подпрограммы флагов.</span><span class="sxs-lookup"><span data-stu-id="85299-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="85299-135">Должны быть установлены только один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="85299-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="85299-136">FIROINTERVAL: Времени, указанного с помощью параметра _csecIdle_ — это минимальный интервал между последовательными вызовами простоя процедуру.</span><span class="sxs-lookup"><span data-stu-id="85299-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="85299-137">FIROONCEONLY: устаревший.</span><span class="sxs-lookup"><span data-stu-id="85299-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="85299-138">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="85299-138">Do not use.</span></span> 
      
  - <span data-ttu-id="85299-139">FIROPERBLOCK: устаревший.</span><span class="sxs-lookup"><span data-stu-id="85299-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="85299-140">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="85299-140">Do not use.</span></span> 
      
  - <span data-ttu-id="85299-141">FIROWAIT: Времени, указанного с помощью параметра _csecIdle_ — это минимальный период бездействия со стороны пользователя, которое должно пройти перед простоя подсистемы MAPI вызывает простоя подпрограмму в первый раз.</span><span class="sxs-lookup"><span data-stu-id="85299-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="85299-142">По истечении этого времени простоя модуль может вызывать простоя процедуру при необходимости.</span><span class="sxs-lookup"><span data-stu-id="85299-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="85299-143">_ircIdle_</span><span class="sxs-lookup"><span data-stu-id="85299-143">_ircIdle_</span></span>
  
> <span data-ttu-id="85299-144">[in] Битовая маска флаги служит для указания изменений следует обратить внимание простоя процедуру.</span><span class="sxs-lookup"><span data-stu-id="85299-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="85299-145">Следующие флаги может быть установлено в любом сочетании:</span><span class="sxs-lookup"><span data-stu-id="85299-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="85299-146">FIRCCSEC: Изменение времени, связанные с простоя процедуру, то есть, указанный в параметре значение, переданное в параметре _csecIdle_ изменений.</span><span class="sxs-lookup"><span data-stu-id="85299-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="85299-147">FIRCIRO: Внесение изменений в параметры для бездействующих процедуру, то есть изменений, указанный в параметре значение переданной в параметре _iroIdle_ .</span><span class="sxs-lookup"><span data-stu-id="85299-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="85299-148">FIRCPFN: Внесение изменений в простоя выполнять рутинные указатель, то есть изменений, указанный в параметре значение передается в параметре _pfnIdle_ .</span><span class="sxs-lookup"><span data-stu-id="85299-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="85299-149">FIRCPRI: Изменение приоритета простоя процедуру, то есть изменений, указанный в параметре значение передается в параметре _priIdle_ .</span><span class="sxs-lookup"><span data-stu-id="85299-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="85299-150">FIRCPV: Внесение изменений в блоке памяти простоя процедуру, то есть, изменения, указанный в параметре значение переданной в параметре _pvIdleParam_ .</span><span class="sxs-lookup"><span data-stu-id="85299-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85299-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85299-151">Return value</span></span>

<span data-ttu-id="85299-152">Нет.</span><span class="sxs-lookup"><span data-stu-id="85299-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85299-153">Замечания</span><span class="sxs-lookup"><span data-stu-id="85299-153">Remarks</span></span>

<span data-ttu-id="85299-154">Следующие функции работы с простоя подсистемы MAPI и на основании прототипа функции [FNIDLE](fnidle.md) простоя процедуры:</span><span class="sxs-lookup"><span data-stu-id="85299-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="85299-155">**Функция простоя процедуры**</span><span class="sxs-lookup"><span data-stu-id="85299-155">**Idle routine function**</span></span>|<span data-ttu-id="85299-156">**Использование**</span><span class="sxs-lookup"><span data-stu-id="85299-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85299-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="85299-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="85299-158">Изменение характеристик зарегистрированных простоя процедуры.</span><span class="sxs-lookup"><span data-stu-id="85299-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="85299-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="85299-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="85299-160">Удаляет зарегистрированные простоя процедуру из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="85299-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="85299-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="85299-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="85299-162">Отключает или повторно включает зарегистрированных простоя подпрограмму без его удаления из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="85299-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="85299-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="85299-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="85299-164">Добавляет простоя подпрограммы система MAPI, независимо от его включение.</span><span class="sxs-lookup"><span data-stu-id="85299-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="85299-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="85299-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="85299-166">Завершает работу обработчика бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="85299-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="85299-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="85299-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="85299-168">Инициализирует обработчик простоя MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="85299-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="85299-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**и **EnableIdleRoutine** принимают в качестве входного параметра, функция тег возвращаемых **FtgRegisterIdleRoutine**.</span><span class="sxs-lookup"><span data-stu-id="85299-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="85299-170">При бездействии все задачи переднего плана для платформы, механизм простоя MAPI вызывает наивысший приоритет простоя подпрограммы готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="85299-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="85299-171">Нет никаких гарантий вызова порядок простоя процедуры одинаковый приоритет.</span><span class="sxs-lookup"><span data-stu-id="85299-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

