---
title: Equals(Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Сравнивает равенства двух выражений.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408931"
---
# <a name="equals-access-custom-web-app"></a>Равно (пользовательское веб-приложение Access)

Сравнивает равенства двух выражений.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

`= (Equals)`

*выражение*   =   *выражение* 
  
*expression* — любое допустимое выражение. Если выражения не имеют одного типа данных, тип данных для одного выражения должен быть неявно преобразован в тип данных другого. Преобразование зависит от правил приоритета для типов данных. 
  
## <a name="return-type"></a>Возвращаемый тип

**Boolean**
  
## <a name="remarks"></a>Примечания

При сравнении двух выражений NULL результатом является TRUE.
  
Сравнение значения NULL со значением, не относястое к NULL, всегда приводит к значению FALSE.
  

