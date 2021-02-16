---
title: SetReturnVar Macro action (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 57965c84-7a52-4d7c-9c7f-be3d4570576d
description: Действие SetReturnVar создает возвращаемую переменную и задает для нее определенное значение.
ms.openlocfilehash: 29445f5021bed99fe45cee1d34457f1f91ca417d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409596"
---
# <a name="setreturnvar-macro-action-access-custom-web-app"></a>SetReturnVar Macro action (Access custom web app)

Действие **SetReturnVar** создает возвращаемую переменную и задает для нее определенное значение. 
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
> [!NOTE]
> Действие **SetReturnVar** доступно только в макросах данных. 
  
## <a name="setting"></a>Setting

Действие **SetReturnVar** имеет следующие аргументы. 
  
|**Имя аргумента**|**Обязательный**|**Description**|
|:-----|:-----|:-----|
| _Name_ <br/> |Да  <br/> |Строка, определяющая имя переменной.  <br/> |
| _Expression_ <br/> |Да  <br/> |Выражение, которое будет использоваться для задания значений для данной временной переменной. Не ставьте перед выражением знак равенства (=). Вы можете нажать кнопку **Build**, чтобы использовать **Создатель выражений** для установки данного аргумента.  <br/> |
   
## <a name="remarks"></a>Комментарии

Действие **SetReturnVar** используется для создания **ReturnVar**, переменной, которая может использоваться макросами, которые называют макрос данных с помощью действия **RunDataMacro.** 
  
После создания **ReturnVar** с помощью действия **SetReturnVar** вызываемая макрос может использовать его в выражении. Например, если вы создали **ReturnVar** **с именем UpdateSuccess,** можно использовать переменную с помощью следующего синтаксиса:
  
`=[ReturnVars]![UpdateSuccess]`

Действие **SetReturnVar** можно использовать только в именуемом макросах данных. Он не доступен в макросах данных, прикрепленных к событию макроса данных. 
  

