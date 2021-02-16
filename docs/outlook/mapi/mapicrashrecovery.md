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
# <a name="mapicrashrecovery"></a><span data-ttu-id="c8961-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="c8961-103">MAPICrashRecovery</span></span>

<span data-ttu-id="c8961-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8961-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8961-105">Функция **MAPICrashRecovery** проверяет состояние общей памяти PST-файла или файла автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="c8961-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="c8961-106">Если память находится в согласованном состоянии, функция **MAPICrashRecovery** перемещает данные на диск и предотвращает дальнейший доступ на чтение или записи, пока процесс не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="c8961-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c8961-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c8961-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8961-108">Экспортируется с помощью:</span><span class="sxs-lookup"><span data-stu-id="c8961-108">Exported by:</span></span>  <br/> |<span data-ttu-id="c8961-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="c8961-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c8961-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c8961-110">Called by:</span></span>  <br/> |<span data-ttu-id="c8961-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="c8961-111">Client</span></span>  <br/> |
|<span data-ttu-id="c8961-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c8961-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8961-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="c8961-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="c8961-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8961-114">Parameters</span></span>

<span data-ttu-id="c8961-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c8961-115">_ulFlags_</span></span>
  
> <span data-ttu-id="c8961-116">[in] Флаги, используемые для управления выполнением аварийного восстановления MAPI.</span><span class="sxs-lookup"><span data-stu-id="c8961-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="c8961-117">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c8961-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="c8961-118">**MAPICRASH \_ RECOVER**: если PTS или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PTS или OSTs, чтобы запретить доступ на чтение или записи.</span><span class="sxs-lookup"><span data-stu-id="c8961-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="c8961-119">**MAPICRASH \_ CONTINUE**: Разблокировка PTS или OSTs для отладки.</span><span class="sxs-lookup"><span data-stu-id="c8961-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="c8961-120">После успешного вызова **MAPICrashRecovery** с флагом **MAPICRASH_RECOVER** вызовите **MAPICrashRecovery** с флагом **MAPICRASH \_ CONTINUE,** чтобы продолжить отладку.</span><span class="sxs-lookup"><span data-stu-id="c8961-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="c8961-121">**MAPICRASH \_ SYSTEM_SHUTDOWN:** если PTS или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PTS или OSTs, чтобы запретить доступ на чтение или записи.</span><span class="sxs-lookup"><span data-stu-id="c8961-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="c8961-122">PTS или OSTs не могут быть разблокированы с помощью **MAPICRASH \_ CONTINUE**.</span><span class="sxs-lookup"><span data-stu-id="c8961-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="c8961-123">Должен использоваться в сочетании с **MAPICRASH \_ RECOVER.**</span><span class="sxs-lookup"><span data-stu-id="c8961-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c8961-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8961-124">Remarks</span></span>

<span data-ttu-id="c8961-125">Верхний (0xFF000000) зарезервирован для флагов аварийного восстановления конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="c8961-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="c8961-126">Вызовите **MAPICrashRecovery** с помощью **MAPICRASH \_ RECOVER** **и MAPICRASH_SYSTEM_SHUTDOWN** флагов в ответ на WM_ENDSESSION **сообщения.**</span><span class="sxs-lookup"><span data-stu-id="c8961-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c8961-127">См. также</span><span class="sxs-lookup"><span data-stu-id="c8961-127">See also</span></span>

- [<span data-ttu-id="c8961-128">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="c8961-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="c8961-129">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="c8961-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

