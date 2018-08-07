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
ms.openlocfilehash: 29e7806afce885968956d53005a66bd14639ad64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808269"
---
# <a name="deleting-a-profile"></a>Удаление профиля

  
  
**Относится к**: Outlook 
  
 **Чтобы удалить профиль**
  
- Вызов [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md).
    
 **DeleteProfile** помечает профиля для удаления, если он в настоящее время используется, ждать, пока не является активной удаляет его. Профиль не исчезает фактически только после отключения каждого клиента с активного сеанса. 
  
 **DeleteProfile** вызывает функцию точки входа для каждой службы сообщений в профиле совместно с параметром _ulContext_ , равным MSG_SERVICE_DELETE. Вызовы функций точки входа достигаться до служб физически удалены из профиля. 
  

