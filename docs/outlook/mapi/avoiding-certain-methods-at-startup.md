---
title: Уклонение от использования определенных методов при запуске
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Дата последнего изменения: 7 декабря 2015 года'
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318090"
---
# <a name="avoiding-certain-methods-at-startup"></a>Уклонение от использования определенных методов при запуске

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Для повышения производительности в момент запуска, не используйте указанные ниже вызовы:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Вызов **IMAPIStatus::ValidateState** влияет на производительность только в случае использования либо программы буферизации данных MAPI, подсистемы MAPI. Причина, по которой эти методы замедляют процесс запуска, заключается в том, что их нельзя выполнить, пока программа буферизации данных MAPI не завершит все задачи при запуске. 
  
Кроме того, следует избегать поиска хранилища сообщений в момент запуска. Выполните вызов [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) после завершения обработки запуска. 
  

