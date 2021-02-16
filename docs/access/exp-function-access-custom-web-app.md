---
title: Exp Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Возвращает экспоненциальное значение указанного выражения.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436414"
---
# <a name="exp-function-access-custom-web-app"></a>Exp Function (Access custom web app)

Возвращает экспоненциальное значение указанного выражения.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Exp** (*NumericExpression)* 
  
Функция **Exp** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *NumericExpression*  <br/> |Выражение типа Double или типа, который можно неявно преобразовать в Double.  <br/> |
   
## <a name="remarks"></a>Примечания

**Константа e** (2.718281...), является основой естественных логарифмов. 
  
Экспонент числа — это константа **e,** которая вызывается до его мощности. Например, **Exp** (1,0) = e^1.0 = 2.71828182845905 и **Exp** (10) = e^10 = 22026.4657948067. 
  
Экспоненциальная экспоненция естественного логарифма числа — это сам номер: **Exp** (LOG (n)) = n. А естественным логарифмом экспоненциального числа является сам номер: LOG (**Exp** (n)) = n. 
  

