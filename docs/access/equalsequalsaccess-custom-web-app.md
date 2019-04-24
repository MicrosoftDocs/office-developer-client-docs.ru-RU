---
title: Equals (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Сравнивает равенство двух выражений.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308227"
---
# <a name="equals-access-custom-web-app"></a>Equals (пользовательское веб-приложение для Access)

Сравнивает равенство двух выражений.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

`= (Equals)`

**  =  *выражение* выражения 
  
*expression* — любое допустимое выражение. Если выражения относятся к одному и тому же типу данных, то тип данных для одного выражения должен быть неявно преобразуемым к типу данных другого. Преобразование зависит от правил приоритета для типов данных. 
  
## <a name="return-type"></a>Возвращаемый тип

**Boolean**
  
## <a name="remarks"></a>Примечания

При сравнении двух выражений NULL результат будет иметь значение TRUE.
  
При сравнении значения NULL со значением, отличным от NULL, всегда получается значение FALSE.
  

