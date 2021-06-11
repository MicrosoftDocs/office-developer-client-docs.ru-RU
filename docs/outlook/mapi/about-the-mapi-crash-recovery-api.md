---
title: Сведения об API аварийного восстановления MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420264"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Сведения об API аварийного восстановления MAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API аварийного восстановления MAPI проверяет состояние файла персональных папок (PST) или файла автономных папок (OST), чтобы убедиться, что данные в согласованном состоянии. Если оно находится в согласованном состоянии, функция [MAPICrashRecovery](mapicrashrecovery.md) перемещает данные из открытых PSTs или OSTs на диск и блокирует PSTs или OSTs и не позволяет читать или записывать доступ к данным. Это гарантирует, что данные остаются в согласованном состоянии до окончания процесса. Гарантируя, что psTs или OSTs находятся в согласованном состоянии до прекращения процесса, вы можете запретить Microsoft Outlook 2013 и Microsoft Outlook 2010, русская версия отобразить следующее сообщение об ошибке и избежать проблем с производительностью. 
  
 **Файл данных не закрывался должным образом при последнем использовании и проверяется на наличие проблем. Производительность может быть затронута во время проверки.**
  
В этом API содержится следующее:
  
Константы:
  
- [��������� MAPI](mapi-constants.md)
    
Функции:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>См. также



[Использование API аварийного восстановления MAPI](how-to-use-the-mapi-crash-recovery-api.md)

