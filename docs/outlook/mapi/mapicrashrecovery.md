---
title: MAPICrashRecovery
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPICrashRecovery
api_type:
- COM
ms.assetid: 4172e2d3-6343-385b-c691-a64c1e198051
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9efafbac55a2925e04b533e7c08388c026540dff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407216"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="7695d-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="7695d-103">MAPICrashRecovery</span></span>

<span data-ttu-id="7695d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7695d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7695d-105">Функция **MAPICrashRecovery** проверяет состояние общей памяти файла персональных папок (PST) или файла автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="7695d-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="7695d-106">Если память находится в согласованном состоянии, функция **MAPICrashRecovery** перемещает данные на диск и предотвращает дальнейшее чтение или записи доступа до окончания процесса.</span><span class="sxs-lookup"><span data-stu-id="7695d-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7695d-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7695d-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7695d-108">Экспортируемая по:</span><span class="sxs-lookup"><span data-stu-id="7695d-108">Exported by:</span></span>  <br/> |<span data-ttu-id="7695d-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7695d-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7695d-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7695d-110">Called by:</span></span>  <br/> |<span data-ttu-id="7695d-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="7695d-111">Client</span></span>  <br/> |
|<span data-ttu-id="7695d-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7695d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="7695d-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="7695d-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="7695d-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="7695d-114">Parameters</span></span>

<span data-ttu-id="7695d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7695d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="7695d-116">[in] Флаги, используемые для управления выполнением аварийного восстановления MAPI.</span><span class="sxs-lookup"><span data-stu-id="7695d-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="7695d-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7695d-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="7695d-118">**MAPICRASH \_ ВОССТАНОВЛЕНИЕ.** Если psTs или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PSTs или OSTs, чтобы предотвратить чтение или записи доступа.</span><span class="sxs-lookup"><span data-stu-id="7695d-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="7695d-119">**MAPICRASH \_ ПРОДОЛЖИТЬ:** Разблокировать PSTs или OSTs для отладки.</span><span class="sxs-lookup"><span data-stu-id="7695d-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="7695d-120">После успешного вызова **mapICrashRecovery** с флагом MAPICRASH_RECOVER, позвоните **MAPICrashRecovery** с флагом **MAPICRASH \_ CONTINUE,** чтобы разрешить отладку для продолжения. </span><span class="sxs-lookup"><span data-stu-id="7695d-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="7695d-121">**MAPICRASH \_ SYSTEM_SHUTDOWN.** Если psTs или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PSTs или OSTs, чтобы предотвратить чтение или записи доступа.</span><span class="sxs-lookup"><span data-stu-id="7695d-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="7695d-122">PsTs или OSTs не могут быть разблокированы с помощью **MAPICRASH \_ CONTINUE**.</span><span class="sxs-lookup"><span data-stu-id="7695d-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="7695d-123">Необходимо использовать в сочетании с **MAPICRASH \_ RECOVER**.</span><span class="sxs-lookup"><span data-stu-id="7695d-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7695d-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="7695d-124">Remarks</span></span>

<span data-ttu-id="7695d-125">Верхний byte (0xFF000000) зарезервирован для определенных флагов аварийного восстановления поставщика.</span><span class="sxs-lookup"><span data-stu-id="7695d-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="7695d-126">Вызов **MAPICrashRecovery** с помощью восстановления  **MAPICRASH \_** и MAPICRASH_SYSTEM_SHUTDOWN флагов в ответ на WM_ENDSESSION **сообщение.**</span><span class="sxs-lookup"><span data-stu-id="7695d-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7695d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="7695d-127">See also</span></span>

- [<span data-ttu-id="7695d-128">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="7695d-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="7695d-129">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="7695d-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

