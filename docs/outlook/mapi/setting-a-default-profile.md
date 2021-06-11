---
title: Настройка профиля по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439816"
---
# <a name="setting-a-default-profile"></a>Настройка профиля по умолчанию

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Профиль по умолчанию — это профиль, который используется, если в вызове [MAPILogonEx](mapilogonex.md)явно не указан профиль, задав вместо него MAPI_USE_DEFAULT флага.
  
 **Создание профиля по умолчанию**
  
1. Вызов [функции MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin.** 
    
2. Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** задает **свойство PR_DEFAULT_PROFILE** [(PidTagDefaultProfile)](pidtagdefaultprofile-canonical-property.md)для нового профиля по умолчанию и удаляет параметр для предыдущего профиля по умолчанию.
    

