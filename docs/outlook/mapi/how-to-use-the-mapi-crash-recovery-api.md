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
# <a name="use-the-mapi-crash-recovery-api"></a>Использование API аварийного восстановления MAPI

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе приведен пример кода на языке C++, в котором показано, как вызвать функцию [мапикрашрековери](mapicrashrecovery.md) из функции [унхандледексцептионфилтер](https://msdn.microsoft.com/library/ms681401%28VS.85%29.aspx) . Функция [мапикрашрековери](mapicrashrecovery.md) проверяет состояние общей памяти файла личных папок (PST) или файла автономных папок (OST). 

Если память находится в согласованном состоянии, функция [мапикрашрековери](mapicrashrecovery.md) переместит данные на диск и предотвращает дальнейший доступ для чтения или записи до завершения процесса. Убедившись, что PST-файлы или Остс находятся в согласованном состоянии до завершения процесса, можно запретить Microsoft Outlook 2010 или Microsoft Outlook 2013 отображать следующее сообщение об ошибке и избежать проблем с производительностью. 
  
**Файл данных не был правильно закрыт при последнем использовании и проверяется на наличие проблем. В процессе проверки производительность может быть снижена.**
  
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

