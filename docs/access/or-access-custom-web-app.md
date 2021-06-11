---
title: OR (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединяет два условия. Возвращает TRUE, когда все эти два условия верны.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414762"
---
# <a name="or-access-custom-web-app"></a>OR (Доступ к настраиваемой веб-приложению)

Объединяет два условия. Возвращает TRUE, когда все эти два условия верны.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 *BooleanExpression* **или** *BooleanExpression* 
  
Оператор **Or** использует следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Любое допустимые выражения, возвращая TRUE или FALSE.  <br/> |
   
## <a name="remarks"></a>Примечания

Когда в операторе используется несколько логических операторов, **или** операторы оцениваются после **And** operators. Однако можно изменить порядок оценки с помощью скобок. 
  
В следующей таблице показан результат **оператора Or.** 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

