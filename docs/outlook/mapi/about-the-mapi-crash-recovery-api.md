---
title: Сведения об API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576591"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Сведения об API аварийного восстановления MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API сбой восстановления MAPI, проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти для проверки правильности данных в стабильном состоянии. Если он установлен в стабильном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные из open PST и OST на диске и блокирует PST и OST и не позволяет любой доступ на чтение или запись доступа к данным. Это гарантирует, что данные остается в стабильном состоянии, пока процесс завершается. Убедитесь, что PST и OST в стабильном состоянии до завершения процесса, позволяет предотвратить отображение следующее сообщение об ошибке Microsoft Outlook 2013 и Microsoft Outlook 2010 и избежать проблем с производительностью. 
  
 **Файл данных не закрыта должным образом время последнего он использовался и выполняется проверка проблем. Может повлиять на производительность во время выполнения проверки.**
  
Этот интерфейс API предоставляет следующие возможности:
  
Константы:
  
- [Константы MAPI](mapi-constants.md)
    
Функции:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>См. также



[Использование API аварийного восстановления MAPI](how-to-use-the-mapi-crash-recovery-api.md)

