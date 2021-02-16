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
  
Функция **MAPICrashRecovery** проверяет состояние общей памяти PST-файла или файла автономных папок (OST). Если память находится в согласованном состоянии, функция **MAPICrashRecovery** перемещает данные на диск и предотвращает дальнейший доступ на чтение или записи, пока процесс не будет завершен. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |olmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>Параметры

_ulFlags_
  
> [in] Флаги, используемые для управления выполнением аварийного восстановления MAPI. Можно установить следующие флаги:
    
   - **MAPICRASH \_ RECOVER**: если PTS или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PTS или OSTs, чтобы запретить доступ на чтение или записи.
    
   - **MAPICRASH \_ CONTINUE**: Разблокировка PTS или OSTs для отладки. После успешного вызова **MAPICrashRecovery** с флагом **MAPICRASH_RECOVER** вызовите **MAPICrashRecovery** с флагом **MAPICRASH \_ CONTINUE,** чтобы продолжить отладку. 
    
   - **MAPICRASH \_ SYSTEM_SHUTDOWN:** если PTS или OSTs находятся в согласованном состоянии, переместить данные на диск и заблокировать PTS или OSTs, чтобы запретить доступ на чтение или записи. PTS или OSTs не могут быть разблокированы с помощью **MAPICRASH \_ CONTINUE**. Должен использоваться в сочетании с **MAPICRASH \_ RECOVER.** 
    
## <a name="remarks"></a>Примечания

Верхний (0xFF000000) зарезервирован для флагов аварийного восстановления конкретного поставщика.
  
Вызовите **MAPICrashRecovery** с помощью **MAPICRASH \_ RECOVER** **и MAPICRASH_SYSTEM_SHUTDOWN** флагов в ответ на WM_ENDSESSION **сообщения.** 
  
## <a name="see-also"></a>См. также

- [Сведения об API аварийного восстановления MAPI](about-the-mapi-crash-recovery-api.md)
- [Использование API аварийного восстановления MAPI](how-to-use-the-mapi-crash-recovery-api.md)

