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
ms.openlocfilehash: 22f17df9347b4744dfe6598e7007469ffb9e5251
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809897"
---
# <a name="mapicrashrecovery"></a><span data-ttu-id="f4a6d-103">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="f4a6d-103">MAPICrashRecovery</span></span>

<span data-ttu-id="f4a6d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f4a6d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f4a6d-105">Функция **MAPICrashRecovery** проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-105">The **MAPICrashRecovery** function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> <span data-ttu-id="f4a6d-106">Если объем памяти, находится в стабильном состоянии, функция **MAPICrashRecovery** перемещает данные на диске и предотвращает дальнейший доступ на чтение или запись, пока процесс завершается.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-106">If the memory is in a consistent state, the **MAPICrashRecovery** function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f4a6d-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f4a6d-107">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4a6d-108">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="f4a6d-108">Exported by:</span></span>  <br/> |<span data-ttu-id="f4a6d-109">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="f4a6d-109">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="f4a6d-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="f4a6d-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4a6d-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="f4a6d-111">Client</span></span>  <br/> |
|<span data-ttu-id="f4a6d-112">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="f4a6d-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4a6d-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="f4a6d-113">Outlook</span></span>  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a><span data-ttu-id="f4a6d-114">���������</span><span class="sxs-lookup"><span data-stu-id="f4a6d-114">Parameters</span></span>

<span data-ttu-id="f4a6d-115">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f4a6d-115">_ulFlags_</span></span>
  
> <span data-ttu-id="f4a6d-116">[in] Флаги, используемые для управления, как выполняется восстановления после сбоя MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-116">[in] Flags used to control how the MAPI crash recovery is performed.</span></span> <span data-ttu-id="f4a6d-117">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="f4a6d-117">The following flags can be set:</span></span>
    
   - <span data-ttu-id="f4a6d-118">**MAPICRASH\_ВОССТАНОВИТЬ**: Если PST и OST в стабильном состоянии, перемещение данных на диск и заблокировать PST-файлов или OST, чтобы запретить доступ на чтение или запись.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-118">**MAPICRASH\_RECOVER**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span>
    
   - <span data-ttu-id="f4a6d-119">**MAPICRASH\_ПРОДОЛЖИТЬ**: разблокировать PST и OST для отладки.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-119">**MAPICRASH\_CONTINUE**: Unlock the PSTs or OSTs for debugging.</span></span> <span data-ttu-id="f4a6d-120">После успешного вызова **MAPICrashRecovery** с флагом **MAPICRASH_RECOVER** , вызовите **MAPICrashRecovery** с **MAPICRASH\_ПРОДОЛЖИТЬ** флаг для отладки для продолжения.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-120">After a successful call to **MAPICrashRecovery** with the **MAPICRASH_RECOVER** flag, call **MAPICrashRecovery** with the **MAPICRASH\_CONTINUE** flag to allow debugging to continue.</span></span> 
    
   - <span data-ttu-id="f4a6d-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: Если PST и OST в стабильном состоянии, перемещение данных на диск и заблокировать PST-файлов или OST, чтобы запретить доступ на чтение или запись.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-121">**MAPICRASH\_SYSTEM_SHUTDOWN**: If the PSTs or OSTs are in a consistent state, move the data to disk and lock the PSTs or OSTs to prevent read or write access.</span></span> <span data-ttu-id="f4a6d-122">PST и OST невозможно разблокировать с помощью **MAPICRASH\_ПРОДОЛЖИТЬ**.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-122">The PSTs or OSTs cannot be unlocked using **MAPICRASH\_CONTINUE**.</span></span> <span data-ttu-id="f4a6d-123">Следует использовать в сочетании с **MAPICRASH\_ВОССТАНОВИТЬ**.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-123">Must be used in combination with **MAPICRASH\_RECOVER**.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f4a6d-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4a6d-124">Remarks</span></span>

<span data-ttu-id="f4a6d-125">Верхний байт (0xFF000000) зарезервирован для поставщика конкретных аварийного восстановления флаги.</span><span class="sxs-lookup"><span data-stu-id="f4a6d-125">The upper byte (0xFF000000) is reserved for provider specific crash recovery flags.</span></span>
  
<span data-ttu-id="f4a6d-126">Вызов **MAPICrashRecovery** с **MAPICRASH\_ВОССТАНОВИТЬ** и флаги **MAPICRASH_SYSTEM_SHUTDOWN** в ответ на сообщение **WM_ENDSESSION** .</span><span class="sxs-lookup"><span data-stu-id="f4a6d-126">Call **MAPICrashRecovery** with the **MAPICRASH\_RECOVER** and **MAPICRASH_SYSTEM_SHUTDOWN** flags in response to the **WM_ENDSESSION** message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4a6d-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f4a6d-127">See also</span></span>

- [<span data-ttu-id="f4a6d-128">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a6d-128">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md)
- [<span data-ttu-id="f4a6d-129">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="f4a6d-129">Use the MAPI Crash Recovery API</span></span>](how-to-use-the-mapi-crash-recovery-api.md)

