---
title: Действия Макрос RunDataMacro (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Вы можете использовать действие RunDataMacro для запуска автономных макрос данных.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439347"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Действия Макрос RunDataMacro (Доступ к настраиваемой веб-приложению)

Вы можете использовать **действие RunDataMacro** для запуска автономных макрос данных. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

Действие **RunDataMacro** имеет следующий аргумент. 
  
|**Аргумент макрокоманды**|**Описание**|
|:-----|:-----|
| _Имя макроса_ <br/> |Имя макроса данных для запуска.  <br/> |
   
## <a name="remarks"></a>Примечания

При выборе макроса данных, который требуется выполнить в конструкторе макроса, Access определяет, требуются ли параметры макроса данных. Если макрос данных требует параметров, отображаются текстовые поля, в которых можно ввести аргументы.
  
Когда выполняется макрос, содержащий действие **RunDataMacro** и достигаемого **действия RunDataMacro,** Access запускает называемый макрос данных. После завершения называемого макроса данных Access возвращается к исходному макросу и выполняет следующее действие. 
  

