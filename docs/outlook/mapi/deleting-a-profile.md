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
ms.openlocfilehash: d13af3a2d0293641fd87d1065bceedfa4b62a3b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573245"
---
# <a name="deleting-a-profile"></a>Удаление профиля

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы удалить профиль**
  
- Вызов [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** помечает профиля для удаления, если он в настоящее время используется, ждать, пока не является активной удаляет его. Профиль не исчезает фактически только после отключения каждого клиента с активного сеанса. 
  
 **DeleteProfile** вызывает функцию точки входа для каждой службы сообщений в профиле совместно с параметром _ulContext_ , равным MSG_SERVICE_DELETE. Вызовы функций точки входа достигаться до служб физически удалены из профиля. 
  

