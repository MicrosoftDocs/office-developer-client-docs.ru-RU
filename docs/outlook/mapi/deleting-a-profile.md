---
title: Удаление профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d01ab2e-40fd-409d-a69d-163b7d5462ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1cd87b92a9d289f06e466f4e44ce757c93074336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410205"
---
# <a name="deleting-a-profile"></a>Удаление профиля

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Удаление профиля**
  
- Call [ипрофадмин::D елетепрофиле](iprofadmin-deleteprofile.md).
    
 **Делетепрофиле** помечает профиль для удаления, если он используется в данный момент, дождитесь, пока он не станет активным. В действительности профиль не исчезает, пока не будет отключен каждый клиент с активным сеансом. 
  
 **Делетепрофиле** вызывает функцию точки входа каждой службы сообщений в профиле с параметром _улконтекст_ , для которого задано значение MSG_SERVICE_DELETE. Вызовы функций точки входа происходят до того, как службы физически удаляются из профиля. 
  

