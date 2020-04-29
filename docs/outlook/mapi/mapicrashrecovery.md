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
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Относится к**: Outlook 2013 | Outlook 2016 
  
Функция **мапикрашрековери** проверяет состояние общей памяти файла личных папок (PST) или файла автономных папок (OST). Если память находится в согласованном состоянии, функция **мапикрашрековери** переместит данные на диск и предотвращает дальнейший доступ для чтения или записи до завершения процесса. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |olmapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Параметры

_ulFlags_
  
> возврата Флаги, используемые для управления выполнением восстановления после сбоя MAPI. Можно задать следующие флаги:
    
   - **Мапикраш\_Recover**: Если PST-файлы или остс находятся в согласованном состоянии, переместите данные на диск и заблокируйте PST-файлы или остс, чтобы запретить доступ на чтение или запись.
    
   - **Мапикраш\_Continue**: Разблокируйте PST или остс для отладки. После успешного вызова **мапикрашрековери** с помощью флага **MAPICRASH_RECOVER** вызовите **мапикрашрековери** с флагом **мапикраш\_Continue** , чтобы разрешить продолжение отладки. 
    
   - **Мапикраш\_SYSTEM_SHUTDOWN**: Если PST-файлы или остс находятся в согласованном состоянии, переместите данные на диск и заблокируйте PST-файлы или остс, чтобы запретить доступ на чтение или запись. Невозможно разблокировать PST или Остс с помощью **мапикраш\_Continue**. Должен использоваться в сочетании с **\_мапикраш Recover**. 
    
## <a name="remarks"></a>Примечания

Верхний байт (0xFF000000) зарезервирован для флагов, относящихся к аварийному восстановлению поставщика.
  
Вызовите **мапикрашрековери** с флагами **восстановления\_мапикраш** и **MAPICRASH_SYSTEM_SHUTDOWN** в ответ на сообщение **WM_ENDSESSION** . 
  
## <a name="see-also"></a>См. также

- [Сведения об API аварийного восстановления MAPI](about-the-mapi-crash-recovery-api.md)
- [Использование API аварийного восстановления MAPI](how-to-use-the-mapi-crash-recovery-api.md)

