---
title: Использование API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: a73889982e4aa72fb664a8eafd6fc8704e581e98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346426"
---
# <a name="use-the-mapi-crash-recovery-api"></a><span data-ttu-id="770b4-103">Использование API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="770b4-103">Use the MAPI Crash Recovery API</span></span>

<span data-ttu-id="770b4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="770b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="770b4-105">В этом разделе содержится пример кода в C++, который показывает, как вызвать функцию [MAPICrashRecovery](mapicrashrecovery.md) из функции [UnhandledExceptionFilter.](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="770b4-105">This topic contains a code sample in C++ that shows how to call the [MAPICrashRecovery](mapicrashrecovery.md) function from the [UnhandledExceptionFilter](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) function.</span></span> <span data-ttu-id="770b4-106">Функция [MAPICrashRecovery](mapicrashrecovery.md) проверяет состояние общей памяти файла персональных папок (PST) или файла автономных папок (OST).</span><span class="sxs-lookup"><span data-stu-id="770b4-106">The [MAPICrashRecovery](mapicrashrecovery.md) function checks the state of the Personal Folders file (PST) or Offline Folders file (OST) shared memory.</span></span> 

<span data-ttu-id="770b4-107">Если память находится в согласованном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные на диск и предотвращает дальнейшее чтение или записи доступа до окончания процесса.</span><span class="sxs-lookup"><span data-stu-id="770b4-107">If the memory is in a consistent state, the [MAPICrashRecovery](mapicrashrecovery.md) function moves the data to disk and prevents further read or write access until the process is terminated.</span></span> <span data-ttu-id="770b4-108">Гарантируя, что psTs или OSTs находятся в согласованном состоянии до прекращения процесса, вы можете запретить Microsoft Outlook 2010, русская версия или Microsoft Outlook 2013 отобразить следующее сообщение об ошибке и избежать проблем с производительностью:</span><span class="sxs-lookup"><span data-stu-id="770b4-108">By ensuring that the PSTs or OSTs are in a consistent state before the process is terminated, you can prevent Microsoft Outlook 2010 or Microsoft Outlook 2013 from displaying the following error message and avoid performance problems:</span></span> 
  
<span data-ttu-id="770b4-109">**Файл данных не закрывался должным образом при последнем использовании и проверяется на наличие проблем. Производительность может быть затронута во время проверки.**</span><span class="sxs-lookup"><span data-stu-id="770b4-109">**A data file did not close properly the last time it was used and is being checked for problems. Performance might be affected while the check is in progress.**</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="770b4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="770b4-110">See also</span></span>

- [<span data-ttu-id="770b4-111">Сведения об API аварийного восстановления MAPI</span><span class="sxs-lookup"><span data-stu-id="770b4-111">About the MAPI Crash Recovery API</span></span>](about-the-mapi-crash-recovery-api.md) 
- [<span data-ttu-id="770b4-112">MAPICrashRecovery</span><span class="sxs-lookup"><span data-stu-id="770b4-112">MAPICrashRecovery</span></span>](mapicrashrecovery.md)

