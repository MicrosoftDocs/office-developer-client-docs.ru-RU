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
# <a name="mapicrashrecovery"></a>MAPICrashRecovery

**Относится к**: Outlook 
  
Функция **MAPICrashRecovery** проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти. Если объем памяти, находится в стабильном состоянии, функция **MAPICrashRecovery** перемещает данные на диске и предотвращает дальнейший доступ на чтение или запись, пока процесс завершается. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |olmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
```cpp
void MAPICrashRecovery(ULONG ulFlags);
```

## <a name="parameters"></a>���������

_ulFlags_
  
> [in] Флаги, используемые для управления, как выполняется восстановления после сбоя MAPI. Можно задать следующие флажки:
    
   - **MAPICRASH\_ВОССТАНОВИТЬ**: Если PST и OST в стабильном состоянии, перемещение данных на диск и заблокировать PST-файлов или OST, чтобы запретить доступ на чтение или запись.
    
   - **MAPICRASH\_ПРОДОЛЖИТЬ**: разблокировать PST и OST для отладки. После успешного вызова **MAPICrashRecovery** с флагом **MAPICRASH_RECOVER** , вызовите **MAPICrashRecovery** с **MAPICRASH\_ПРОДОЛЖИТЬ** флаг для отладки для продолжения. 
    
   - **MAPICRASH\_SYSTEM_SHUTDOWN**: Если PST и OST в стабильном состоянии, перемещение данных на диск и заблокировать PST-файлов или OST, чтобы запретить доступ на чтение или запись. PST и OST невозможно разблокировать с помощью **MAPICRASH\_ПРОДОЛЖИТЬ**. Следует использовать в сочетании с **MAPICRASH\_ВОССТАНОВИТЬ**. 
    
## <a name="remarks"></a>Замечания

Верхний байт (0xFF000000) зарезервирован для поставщика конкретных аварийного восстановления флаги.
  
Вызов **MAPICrashRecovery** с **MAPICRASH\_ВОССТАНОВИТЬ** и флаги **MAPICRASH_SYSTEM_SHUTDOWN** в ответ на сообщение **WM_ENDSESSION** . 
  
## <a name="see-also"></a>См. также

- [Сведения об API аварийного восстановления MAPI](about-the-mapi-crash-recovery-api.md)
- [Использование API аварийного восстановления MAPI](how-to-use-the-mapi-crash-recovery-api.md)

