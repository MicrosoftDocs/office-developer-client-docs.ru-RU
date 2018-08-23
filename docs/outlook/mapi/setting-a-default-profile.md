---
title: Установка профиля по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591774"
---
# <a name="setting-a-default-profile"></a>Установка профиля по умолчанию

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Профиль по умолчанию является профиль, который используется, если не указано явно в вызове [MAPILogonEx](mapilogonex.md), вместо этого установка флага MAPI_USE_DEFAULT.
  
 **Чтобы установить профиль по умолчанию**
  
1. Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** . 
    
2. Вызов [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** задает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) для нового профиля по умолчанию и удаляет параметр для предыдущих профиля по умолчанию.
    

