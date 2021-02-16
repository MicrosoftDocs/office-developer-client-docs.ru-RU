---
title: StopMacro Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Вы можете использовать действие StopMacro, чтобы остановить текущий запущенный макрос.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429497"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>StopMacro Macro Action (пользовательское веб-приложение Access)

Вы можете использовать действие **StopMacro,** чтобы остановить текущий запущенный макрос. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="setting"></a>Параметр

У **действия StopMacro** нет аргументов. 
  
## <a name="remarks"></a>Примечания

Обычно это действие используется, когда условие делает необходимым остановить макрос. Например, можно создать макрос пользовательского интерфейса, который открывает представление, в котором отображаются ежедневные итоги заказов для даты, введенной в текущем представлении. Можно использовать условное выражение, чтобы убедиться, что в поле "Дата заказа" содержится допустимая дата. Если это не так, действие **MessageBox** может отображать сообщение об ошибке, а действие **StopMacro** может остановить макрос пользовательского интерфейса. 
  

