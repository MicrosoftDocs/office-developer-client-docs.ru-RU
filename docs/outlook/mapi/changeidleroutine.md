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
# <a name="changeidleroutine"></a><span data-ttu-id="37780-103">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="37780-103">ChangeIdleRoutine</span></span>

<span data-ttu-id="37780-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37780-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37780-105">Изменяет некоторые или все характеристики процедуры бездействия на основе [фнидле](fnidle.md) .</span><span class="sxs-lookup"><span data-stu-id="37780-105">Changes some or all of the characteristics of a [FNIDLE](fnidle.md) based idle routine.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37780-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="37780-106">Header file:</span></span>  <br/> |<span data-ttu-id="37780-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="37780-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="37780-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="37780-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="37780-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="37780-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="37780-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="37780-110">Called by:</span></span>  <br/> |<span data-ttu-id="37780-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="37780-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="37780-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="37780-112">Parameters</span></span>

<span data-ttu-id="37780-113">_ФТГ_</span><span class="sxs-lookup"><span data-stu-id="37780-113">_ftg_</span></span>
  
> <span data-ttu-id="37780-114">возврата Тег функции, определяющий подпрограмму Idle.</span><span class="sxs-lookup"><span data-stu-id="37780-114">[in] Function tag that identifies the idle routine.</span></span> 
    
<span data-ttu-id="37780-115">_Пфнидле_</span><span class="sxs-lookup"><span data-stu-id="37780-115">_pfnIdle_</span></span>
  
> <span data-ttu-id="37780-116">возврата Указатель на подпрограмму Idle.</span><span class="sxs-lookup"><span data-stu-id="37780-116">[in] Pointer to the idle routine.</span></span> 
    
<span data-ttu-id="37780-117">_Пвидлепарам_</span><span class="sxs-lookup"><span data-stu-id="37780-117">_pvIdleParam_</span></span>
  
> <span data-ttu-id="37780-118">возврата Указатель на новый блок памяти, выделенный вызывающей реализацией для процедуры Idle.</span><span class="sxs-lookup"><span data-stu-id="37780-118">[in] Pointer to a new block of memory that the calling implementation allocates for the idle routine.</span></span> 
    
<span data-ttu-id="37780-119">_Приидле_</span><span class="sxs-lookup"><span data-stu-id="37780-119">_priIdle_</span></span>
  
> <span data-ttu-id="37780-120">возврата Значение, представляющее новый приоритет для процедуры простоя.</span><span class="sxs-lookup"><span data-stu-id="37780-120">[in] Value representing a new priority for the idle routine.</span></span> <span data-ttu-id="37780-121">Возможные приоритеты для подпрограмм, определенных при реализации, больше или меньше нуля, но не равны нулю.</span><span class="sxs-lookup"><span data-stu-id="37780-121">Possible priorities for implementation-defined routines are greater than or less than zero, but not zero.</span></span> <span data-ttu-id="37780-122">Нулевое значение зарезервировано для события пользователя, такого как щелчок мыши или сообщение WM_PAINT.</span><span class="sxs-lookup"><span data-stu-id="37780-122">A value of zero is reserved for a user event such as a mouse click or a WM_PAINT message.</span></span> <span data-ttu-id="37780-123">Значения больше нуля представляют приоритеты для фоновых задач, которые имеют более высокий приоритет, чем события пользователя, и отправляются как часть стандартного цикла приема сообщений Windows.</span><span class="sxs-lookup"><span data-stu-id="37780-123">Values greater than zero represent priorities for background tasks that have a higher priority than user events and are dispatched as part of the standard Windows message pump loop.</span></span> <span data-ttu-id="37780-124">Значения, меньшие нуля, представляют приоритеты для бездействующих задач, которые выполняются только во время простоя для приема сообщений.</span><span class="sxs-lookup"><span data-stu-id="37780-124">Values less than zero represent priorities for idle tasks that only run during message-pump idle time.</span></span> <span data-ttu-id="37780-125">Примерами приоритетов являются: 1 для отправки на передний план, 1 для вставки символов Power и 3 для загрузки новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="37780-125">Examples of priorities are: 1 for foreground submission, 1 for power-edit character insertion, and 3 for downloading new messages.</span></span>
    
<span data-ttu-id="37780-126">_КсеЦидле_</span><span class="sxs-lookup"><span data-stu-id="37780-126">_csecIdle_</span></span>
  
> <span data-ttu-id="37780-127">возврата Новое время в сотых долях секунды, которое применяется к процедуре бездействия.</span><span class="sxs-lookup"><span data-stu-id="37780-127">[in] A new time, in hundredths of a second, to apply to the idle routine.</span></span> <span data-ttu-id="37780-128">Значение начального значения времени может различаться в зависимости от того, что передается в параметре _ироидле_ .</span><span class="sxs-lookup"><span data-stu-id="37780-128">The meaning of the initial time value varies, depending on what is passed in the  _iroIdle_ parameter.</span></span> <span data-ttu-id="37780-129">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="37780-129">It can be:</span></span> 
    
  - <span data-ttu-id="37780-130">Минимальный период действия пользователя, который должен пройти, прежде чем антивирусное ядро MAPI вызывает подпрограмму простоя в первый раз, если установлен флаг ФИРОВАИТ в _ироидле_.</span><span class="sxs-lookup"><span data-stu-id="37780-130">The minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time, if the FIROWAIT flag is set in  _iroIdle_.</span></span> <span data-ttu-id="37780-131">По исТечении этого времени модуль простоя может вызывать процедуру простоя, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="37780-131">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
  - <span data-ttu-id="37780-132">Минимальный интервал между вызовами процедуры Idle, если установлен флаг ФИРОИНТЕРВАЛ в _ироидле_.</span><span class="sxs-lookup"><span data-stu-id="37780-132">The minimum interval between calls to the idle routine, if the FIROINTERVAL flag is set in  _iroIdle_.</span></span> 
    
<span data-ttu-id="37780-133">_Ироидле_</span><span class="sxs-lookup"><span data-stu-id="37780-133">_iroIdle_</span></span>
  
> <span data-ttu-id="37780-134">возврата Битовая маска флагов, указывающих новые параметры для вызова процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="37780-134">[in] Bitmask of flags indicating new options for calling the idle routine.</span></span> <span data-ttu-id="37780-135">Необходимо задать только один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="37780-135">Exactly one of the following flags must be set:</span></span>
    
  - <span data-ttu-id="37780-136">ФИРОИНТЕРВАЛ: время, заданное параметром _ксеЦидле_ , является минимальным интервалом между последовательными вызовами процедуры Idle.</span><span class="sxs-lookup"><span data-stu-id="37780-136">FIROINTERVAL: The time specified by the  _csecIdle_ parameter is the minimum interval between successive calls to the idle routine.</span></span> 
      
  - <span data-ttu-id="37780-137">ФИРУНЦЕОНЛИ: устарело.</span><span class="sxs-lookup"><span data-stu-id="37780-137">FIROONCEONLY: Obsolete.</span></span> <span data-ttu-id="37780-138">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="37780-138">Do not use.</span></span> 
      
  - <span data-ttu-id="37780-139">ФИРОПЕРБЛОКК: устарело.</span><span class="sxs-lookup"><span data-stu-id="37780-139">FIROPERBLOCK: Obsolete.</span></span> <span data-ttu-id="37780-140">Не следует использовать.</span><span class="sxs-lookup"><span data-stu-id="37780-140">Do not use.</span></span> 
      
  - <span data-ttu-id="37780-141">ФИРОВАИТ: время, заданное параметром _ксеЦидле_ , является минимальным периодом действия пользователя, который должен пройти, прежде чем антивирусное ядро MAPI вызывает подпрограмму простоя в первый раз.</span><span class="sxs-lookup"><span data-stu-id="37780-141">FIROWAIT: The time specified by the  _csecIdle_ parameter is the minimum period of user inaction that must elapse before the MAPI idle engine calls the idle routine for the first time.</span></span> <span data-ttu-id="37780-142">По исТечении этого времени модуль простоя может вызывать процедуру простоя, как это необходимо.</span><span class="sxs-lookup"><span data-stu-id="37780-142">After this time passes, the idle engine can call the idle routine as often as necessary.</span></span> 
    
<span data-ttu-id="37780-143">_ИрЦидле_</span><span class="sxs-lookup"><span data-stu-id="37780-143">_ircIdle_</span></span>
  
> <span data-ttu-id="37780-144">возврата Битовая маска флагов, используемых для указания изменений, которые необходимо внести в подпрограмму периода бездействия.</span><span class="sxs-lookup"><span data-stu-id="37780-144">[in] Bitmask of flags used to indicate the changes to be made to the idle routine.</span></span> <span data-ttu-id="37780-145">Следующие флаги можно задавать в любом сочетании:</span><span class="sxs-lookup"><span data-stu-id="37780-145">The following flags can be set in any combination:</span></span>
    
  - <span data-ttu-id="37780-146">ФИРККСЕК: изменяет время, связанное с подпрограммой простоя, то есть изменением, указанным значением, переданным в параметре _ксеЦидле_ .</span><span class="sxs-lookup"><span data-stu-id="37780-146">FIRCCSEC: A change to the time associated with the idle routine, that is, a change indicated by the value passed in the  _csecIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="37780-147">ФИРЦИРО: изменение параметров для подпрограммы периода бездействия, то есть изменения, которые указываются значением, переданным в параметре _ироидле_ .</span><span class="sxs-lookup"><span data-stu-id="37780-147">FIRCIRO: A change to the options for the idle routine, that is, a change indicated by the value passed in the  _iroIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="37780-148">ФИРКПФН: изменение указателя на процедуру простоя, то есть изменение, заданное значением, переданным в параметре _пфнидле_ .</span><span class="sxs-lookup"><span data-stu-id="37780-148">FIRCPFN: A change to the idle routine pointer, that is, a change indicated by the value passed in the  _pfnIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="37780-149">ФИРКПРИ: изменение приоритета неактивной процедуры, то есть изменения, которые указываются значением, переданным в параметре _приидле_ .</span><span class="sxs-lookup"><span data-stu-id="37780-149">FIRCPRI: A change to the priority of the idle routine, that is, a change indicated by the value passed in the  _priIdle_ parameter.</span></span> 
      
  - <span data-ttu-id="37780-150">ФИРКПВ: изменение блока памяти для подпрограммы Idle, то есть изменения, которые указываются значением, переданным в параметре _пвидлепарам_ .</span><span class="sxs-lookup"><span data-stu-id="37780-150">FIRCPV: A change to the memory block of the idle routine, that is, a change indicated by the value passed in the  _pvIdleParam_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="37780-151">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37780-151">Return value</span></span>

<span data-ttu-id="37780-152">Нет.</span><span class="sxs-lookup"><span data-stu-id="37780-152">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="37780-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="37780-153">Remarks</span></span>

<span data-ttu-id="37780-154">Следующие функции работают с модулем бездействия MAPI и с процедурами Idle, основанными на прототипе функции [фнидле](fnidle.md) :</span><span class="sxs-lookup"><span data-stu-id="37780-154">The following functions deal with the MAPI idle engine and with idle routines based on the [FNIDLE](fnidle.md) function prototype:</span></span> 
  
|<span data-ttu-id="37780-155">**Функция неАктивности**</span><span class="sxs-lookup"><span data-stu-id="37780-155">**Idle routine function**</span></span>|<span data-ttu-id="37780-156">**Usage**</span><span class="sxs-lookup"><span data-stu-id="37780-156">**Usage**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37780-157">**ChangeIdleRoutine**</span><span class="sxs-lookup"><span data-stu-id="37780-157">**ChangeIdleRoutine**</span></span> <br/> |<span data-ttu-id="37780-158">Изменяет характеристики зарегистрированной процедуры бездействия.</span><span class="sxs-lookup"><span data-stu-id="37780-158">Changes the characteristics of a registered idle routine.</span></span>  <br/> |
|[<span data-ttu-id="37780-159">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="37780-159">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md) <br/> |<span data-ttu-id="37780-160">Удаляет зарегистрированную процедуру бездействия из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="37780-160">Removes a registered idle routine from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="37780-161">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="37780-161">EnableIdleRoutine</span></span>](enableidleroutine.md) <br/> |<span data-ttu-id="37780-162">Отключает или повторно включает зарегистрированную подпрограмму бездействия, не удаляя ее из системы MAPI.</span><span class="sxs-lookup"><span data-stu-id="37780-162">Disables or re-enables a registered idle routine without removing it from the MAPI system.</span></span>  <br/> |
|[<span data-ttu-id="37780-163">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="37780-163">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md) <br/> |<span data-ttu-id="37780-164">Добавляет подпрограмму бездействия в систему MAPI с включением или без него.</span><span class="sxs-lookup"><span data-stu-id="37780-164">Adds an idle routine to the MAPI system, with or without enabling it.</span></span>  <br/> |
|[<span data-ttu-id="37780-165">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="37780-165">MAPIDeInitIdle</span></span>](mapideinitidle.md) <br/> |<span data-ttu-id="37780-166">Завершает работу модуля бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="37780-166">Shuts down the MAPI idle engine for the calling application.</span></span>  <br/> |
|[<span data-ttu-id="37780-167">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="37780-167">MAPIInitIdle</span></span>](mapiinitidle.md) <br/> |<span data-ttu-id="37780-168">Инициализирует модуль бездействия MAPI для вызывающего приложения.</span><span class="sxs-lookup"><span data-stu-id="37780-168">Initializes the MAPI idle engine for the calling application.</span></span>  <br/> |
   
<span data-ttu-id="37780-169">**Чанжеидлераутине**, **дерегистеридлераутине**и **енаблеидлераутине** принимают в качестве входного параметра тег функции, возвращенный методом **фтгрегистеридлераутине**.</span><span class="sxs-lookup"><span data-stu-id="37780-169">**ChangeIdleRoutine**, **DeregisterIdleRoutine**, and **EnableIdleRoutine** take as an input parameter the function tag returned by **FtgRegisterIdleRoutine**.</span></span> 
  
<span data-ttu-id="37780-170">Когда все фоновые задачи для платформы становятся неактивными, модуль бездействия MAPI вызывает подпрограмму самого высокого приоритета, готовую к выполнению.</span><span class="sxs-lookup"><span data-stu-id="37780-170">When all foreground tasks for the platform become idle, the MAPI idle engine calls the highest priority idle routine that is ready to execute.</span></span> <span data-ttu-id="37780-171">Не существует гарантии того, что вы звоните между процедурами неактивности и одинаковым приоритетом.</span><span class="sxs-lookup"><span data-stu-id="37780-171">There is no guarantee of calling order among idle routines of the same priority.</span></span> 
  

