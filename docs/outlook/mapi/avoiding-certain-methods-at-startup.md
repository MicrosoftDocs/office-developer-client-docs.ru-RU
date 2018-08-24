---
title: Запуск без использования определенных методов
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580637"
---
# <a name="avoiding-certain-methods-at-startup"></a>Запуск без использования определенных методов

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
В целях повышения производительности во время запуска предотвратить выполнение следующих вызовов:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Вызов **IMAPIStatus::ValidateState** влияет на производительность только в том случае, когда для очереди MAPI или в подсистеме MAPI. Причина медленно, что эти методы запуска обработки том, что не удается выполнить до завершения задачи по запуску диспетчер очереди MAPI. 
  
Также следует избегать поиска хранилища сообщений во время запуска. Выполнение звонков [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) после завершения работы запуска обработки. 
  

