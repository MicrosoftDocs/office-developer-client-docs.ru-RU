---
title: О восстановлении после сбоя MAPI API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 34589860ed25f8236a343e16679c2e7a6bdd1e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807991"
---
# <a name="about-the-mapi-crash-recovery-api"></a>О восстановлении после сбоя MAPI API

  
  
**Применимо к**: Outlook 
  
API сбой восстановления MAPI, проверяет состояние файл личных папок (PST) или файл автономной папки (OST) общей памяти для проверки правильности данных в стабильном состоянии. Если он установлен в стабильном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные из open PST и OST на диске и блокирует PST и OST и не позволяет любой доступ на чтение или запись доступа к данным. Это гарантирует, что данные остается в стабильном состоянии, пока процесс завершается. Убедитесь, что PST и OST в стабильном состоянии до завершения процесса, позволяет предотвратить отображение следующее сообщение об ошибке Microsoft Outlook 2013 и Microsoft Outlook 2010 и избежать проблем с производительностью. 
  
 **Файл данных не закрыта должным образом время последнего он использовался и выполняется проверка проблем. Может повлиять на производительность во время выполнения проверки.**
  
Этот интерфейс API предоставляет следующие возможности:
  
Константы:
  
- [��������� MAPI](mapi-constants.md)
    
Функции:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>См. также



[Использование восстановления после сбоя MAPI API](how-to-use-the-mapi-crash-recovery-api.md)

