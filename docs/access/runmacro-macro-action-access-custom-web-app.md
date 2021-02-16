---
title: RunMacro Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Макрос пользовательского интерфейса можно использовать для запуска макроса RunMacro.
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438444"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>RunMacro Macro Action (пользовательское веб-приложение Access)

Макрос пользовательского интерфейса можно использовать для запуска макроса **RunMacro.** 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

Действие **RunMacro** имеет следующие аргументы. 
  
|**Аргумент макрокоманды**|**Описание**|
|:-----|:-----|
|**Имя макроса** <br/> |Имя запускаемого макроса пользовательского интерфейса.  <br/> |
   
## <a name="remarks"></a>Примечания

Когда вы запускаете макрос пользовательского интерфейса, содержащий действие **RunMacro,** и оно достигает действия **RunMacro,** Access запускает называемый макрос пользовательского интерфейса. После завершения называемого макроса пользовательского интерфейса Access возвращается к исходному макросу пользовательского интерфейса и выполняет следующее действие. 
  

