---
title: Макрокоманда RunDataMacro (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Вы можете использовать действие RunDataMacro для запуска автономного макроса данных.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304244"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Макрокоманда RunDataMacro (пользовательское веб-приложение для Access)

Вы можете использовать действие **RunDataMacro** для запуска автономного макроса данных. 
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

Действие **RunDataMacro** имеет следующий аргумент. 
  
|**Аргумент макрокоманды**|**Описание**|
|:-----|:-----|
| _Имя макроса_ <br/> |Имя запускаемого макроса данных.  <br/> |
   
## <a name="remarks"></a>Замечания

При выборе макроса данных, который требуется запустить в конструкторе макросов, Access определяет, требуются ли для макроса данных параметры. Если макрос данных требует параметров, отображаются текстовые поля, в которых можно вводить аргументы.
  
При запуске макроса, содержащего действие **RunDataMacro** , и достижении действия **RunDataMacro** , Access запускает макрос данных, который вызывается. После завершения вызываемого макроса данных Access возвращается к исходному макросу и выполняет следующее действие. 
  

