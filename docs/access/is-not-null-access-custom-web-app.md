---
title: IS [NOT] NULL (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Определяет, имеет ли указанное выражение значение NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311139"
---
# <a name="is-not-null-access-custom-web-app"></a>IS [NOT] NULL (пользовательское веб-приложение для Access)

Определяет, имеет ли указанное выражение значение NULL.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 *выражение* **IS** [  *NOT*  ] **NULL**
  
Предикат **IS [NOT] NULL** содержит указанные ниже аргументы. 
  
|||
|:-----|:-----|
| *выражение*  <br/> |Любое допустимое выражение.  <br/> |
| *NOT*  <br/> |Указывает, что логический результат отвергается. Предикат меняет возвращенные значения на противоположные, возвращая TRUE, если значение отлично от NULL, и FALSE, если значением является NULL.  <br/> |
   
## <a name="remarks"></a>Примечания

Если *выражение* имеет значение NULL, предикат IS NULL возвращает значение TRUE; в ином случае возвращается значение FALSE. 
  
Если выражение имеет значение NULL, предикат IS NOT NULL возвращает значение FALSE; в ином случае возвращается значение TRUE.
  

