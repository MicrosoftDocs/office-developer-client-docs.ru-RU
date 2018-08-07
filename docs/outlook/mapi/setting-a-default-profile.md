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
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812257"
---
# <a name="setting-a-default-profile"></a>Установка профиля по умолчанию

  
  
**Относится к**: Outlook 
  
Профиль по умолчанию является профиль, который используется, если не указано явно в вызове [MAPILogonEx](mapilogonex.md), вместо этого установка флага MAPI_USE_DEFAULT.
  
 **Чтобы установить профиль по умолчанию**
  
1. Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** . 
    
2. Вызов [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** задает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) для нового профиля по умолчанию и удаляет параметр для предыдущих профиля по умолчанию.
    

