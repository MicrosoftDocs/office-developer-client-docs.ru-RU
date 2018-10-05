---
title: Использование API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388506"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="b0a7b-103">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="b0a7b-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="b0a7b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0a7b-105">В этом разделе содержится пример кода на C++ показано, как вызывать функцию [MAPICrashRecovery](mapicrashrecovery.md) из функции [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="b0a7b-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="b0a7b-106">Функция [MAPICrashRecovery](mapicrashrecovery.md) проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="b0a7b-107">Если объем памяти, находится в стабильном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные на диске и предотвращает дальнейший доступ на чтение или запись, пока процесс завершается.</span><span class="sxs-lookup"><span data-stu-id="b0a7b-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="b0a7b-108">Убедитесь, что PST и OST в стабильном состоянии до завершения процесса, позволяет предотвратить отображение следующее сообщение об ошибке Microsoft Outlook 2010 или Microsoft Outlook 2013 и избежать проблем с производительностью:</span><span class="sxs-lookup"><span data-stu-id="b0a7b-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="b0a7b-109">**Файл данных не закрыта должным образом время последнего он использовался и выполняется проверка проблем. Может повлиять на производительность во время выполнения проверки.**</span><span class="sxs-lookup"><span data-stu-id="b0a7b-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
```cpp
LONG WINAPI UnhandledExceptionFilter(__in EXCEPTION_POINTERS* pep) 
{ 
    // Let the OS terminate the process upon return. 
    LONG retval = EXCEPTION_EXECUTE_HANDLER; 
 
    switch (pep->ExceptionRecord->ExceptionCode) 
    { 
        case EXCEPTION_BREAKPOINT: 
        case EXCEPTION_SINGLE_STEP: 
            // Ignore debugging exceptions. 
            retval = EXCEPTION_CONTINUE_SEARCH; 
            break; 
 
        default: 
            // The process is going to be terminated, so disconnect the MAPI database. 
            MAPICrashRecovery(MAPICRASH_RECOVER); 
            // Optionally, you can display a crash reporting dialog box here. 
            // If the user chooses to debug,  
            // call MAPICrashRecovery(MAPICRASH_CONTINUE). 
            break; 
    } 
 
    return retval; 
}
```

## <a name="see-also"></a><span data-ttu-id="b0a7b-110">См. также</span><span class="sxs-lookup"><span data-stu-id="b0a7b-110">See also</span></span>

- [<span data-ttu-id="b0a7b-111">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="b0a7b-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="b0a7b-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="b0a7b-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

