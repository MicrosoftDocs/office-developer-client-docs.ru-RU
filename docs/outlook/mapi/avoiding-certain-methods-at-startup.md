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
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808118"
---
# <a name="avoiding-certain-methods-at-startup"></a>Запуск без использования определенных методов

 
  
**Относится к**: Outlook 
  
В целях повышения производительности во время запуска предотвратить выполнение следующих вызовов:
  
- [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md)
    
- [IMAPISession::GetStatusTable](imapisession-getstatustable.md)
    
- [IMAPISession::Logoff](imapisession-logoff.md)
    
- [IMAPISession::QueryIdentity](imapisession-queryidentity.md)
    
- [IMAPIStatus::ValidateState](imapistatus-validatestate.md)
    
Вызов **IMAPIStatus::ValidateState** влияет на производительность только в том случае, когда для очереди MAPI или в подсистеме MAPI. Причина медленно, что эти методы запуска обработки том, что не удается выполнить до завершения задачи по запуску диспетчер очереди MAPI. 
  
Также следует избегать поиска хранилища сообщений во время запуска. Выполнение звонков [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) после завершения работы запуска обработки. 
  

