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
# <a name="mapicrashrecovery"></a><span data-ttu-id="94350-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="94350-103">MAPICrashRecovery</span></span>

<span data-ttu-id="94350-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94350-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94350-105">Функция **мапикрашрековери** проверяет состояние общей памяти файла личных папок (PST) или файла автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="94350-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="94350-106">Если память находится в согласованном состоянии, функция **мапикрашрековери** переместит данные на диск и предотвращает дальнейший доступ для чтения или записи до завершения процесса.</span><span class="sxs-lookup"><span data-stu-id="94350-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="94350-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="94350-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94350-108">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="94350-108">Exported by:</span></span>  <br/> |<span data-ttu-id="94350-109">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="94350-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="94350-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="94350-110">Called by:</span></span>  <br/> |<span data-ttu-id="94350-111">Client</span><span class="sxs-lookup"><span data-stu-id="94350-111">Client</span></span>  <br/> |
|<span data-ttu-id="94350-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="94350-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="94350-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="94350-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="94350-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="94350-114">Parameters</span></span>

<span data-ttu-id="94350-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94350-115">_ulFlags_</span></span>
  
> <span data-ttu-id="94350-116">возврата Флаги, используемые для управления выполнением восстановления после сбоя MAPI.</span><span class="sxs-lookup"><span data-stu-id="94350-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="94350-117">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="94350-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="94350-118">**Мапикраш\_Recover**: Если PST-файлы или остс находятся в согласованном состоянии, переместите данные на диск и заблокируйте PST-файлы или остс, чтобы запретить доступ на чтение или запись.</span><span class="sxs-lookup"><span data-stu-id="94350-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="94350-119">**Мапикраш\_Continue**: Разблокируйте PST или остс для отладки.</span><span class="sxs-lookup"><span data-stu-id="94350-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="94350-120">После успешного вызова **мапикрашрековери** с помощью флага **MAPICRASH_RECOVER** вызовите **мапикрашрековери** с флагом **мапикраш\_Continue** , чтобы разрешить продолжение отладки.</span><span class="sxs-lookup"><span data-stu-id="94350-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="94350-121">**Мапикраш\_SYSTEM_SHUTDOWN**: Если PST-файлы или остс находятся в согласованном состоянии, переместите данные на диск и заблокируйте PST-файлы или остс, чтобы запретить доступ на чтение или запись.</span><span class="sxs-lookup"><span data-stu-id="94350-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="94350-122">Невозможно разблокировать PST или Остс с помощью **мапикраш\_Continue**.</span><span class="sxs-lookup"><span data-stu-id="94350-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="94350-123">Должен использоваться в сочетании с **\_мапикраш Recover**.</span><span class="sxs-lookup"><span data-stu-id="94350-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="94350-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="94350-124">Remarks</span></span>

<span data-ttu-id="94350-125">Верхний байт (0xFF000000) зарезервирован для флагов, относящихся к аварийному восстановлению поставщика.</span><span class="sxs-lookup"><span data-stu-id="94350-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="94350-126">Вызовите **мапикрашрековери** с флагами **восстановления\_мапикраш** и **MAPICRASH_SYSTEM_SHUTDOWN** в ответ на сообщение **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="94350-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94350-127">См. также</span><span class="sxs-lookup"><span data-stu-id="94350-127">See also</span></span>

- [<span data-ttu-id="94350-128">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="94350-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="94350-129">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="94350-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

