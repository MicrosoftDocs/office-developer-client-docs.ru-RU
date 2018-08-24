---
title: Использование API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1a9871c2-b9bb-332e-b67e-85c50f7f685c
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 41d70c2ab94712e40de9011bc752c79d8c859161
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595183"
---
# <a name="use-the-mapi-crash-recovery-api"></a>Использование API аварийного восстановления MAPI

**Относится к**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример кода на C++ показано, как вызывать функцию [MAPICrashRecovery](mapicrashrecovery.md) из функции [UnhandledExceptionFilter](http://msdn.microsoft.com/en-us/library/ms681401%28VS.85%29.aspx) . Функция [MAPICrashRecovery](mapicrashrecovery.md) проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти. 

Если объем памяти, находится в стабильном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные на диске и предотвращает дальнейший доступ на чтение или запись, пока процесс завершается. Убедитесь, что PST и OST в стабильном состоянии до завершения процесса, позволяет предотвратить отображение следующее сообщение об ошибке Microsoft Outlook 2010 или Microsoft Outlook 2013 и избежать проблем с производительностью: 
  
**Файл данных не закрыта должным образом время последнего он использовался и выполняется проверка проблем. Может повлиять на производительность во время выполнения проверки.**
  
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

## <a name="see-also"></a>См. также

- [Сведения об API аварийного восстановления MAPI](about-the-mapi-crash-recovery-api.md) 
- [MAPICrashRecovery](mapicrashrecovery.md)

