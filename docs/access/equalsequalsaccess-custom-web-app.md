---
title: Равно (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Проверяет равенство двух выражений.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806970"
---
# <a name="equals-access-custom-web-app"></a>Равно (приложение настраиваемых web Access)

Проверяет равенство двух выражений.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

`= (Equals)`

*выражение*  =  *выражение* 
  
*выражение*  — Это любое допустимое выражение. Если выражения не представляют тот же тип данных, тип данных для одного выражения должен неявно преобразовываться в тип данных другого. Преобразование зависит от правил очередности типов данных. 
  
## <a name="return-type"></a>Возвращаемый тип

**Boolean**
  
## <a name="remarks"></a>Замечания

При сравнении двух выражений значение NULL, результатом является значение TRUE.
  
Сравнение NULL НЕНУЛЕВОЕ значение всегда дает значение FALSE.
  

