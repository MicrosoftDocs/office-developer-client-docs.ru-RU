---
title: Avg Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Вычисляет арифметическое значение набора значений, содержащихся в указанном поле.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426725"
---
# <a name="avg-function-access-custom-web-app"></a>Avg Function (Access custom web app)

Вычисляет арифметическое значение набора значений, содержащихся в указанном поле.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Avg** (*NumericExpression)* 
  
**Avg** function contains the following argument. 
  
|**Аргумент**|**Описание**|
|:-----|:-----|
|NumericExpression  <br/> |Строковая выражение, определяющие поле, которое содержит числовую информацию, которую вы хотите усреднить, или выражение, которое выполняет вычисление с использованием данных в этом поле. Операнды в  *NumericExpression*  могут включать имя поля таблицы, переменной или функции (которая может быть внутренней или определяемой пользователем, но не одной из других SQL агрегатных функций).  <br/> |
   
## <a name="remarks"></a>Примечания

Среднее значение, вычисляемого **avg,** — это арифметическое среднее (сумма значений, разделенных на число значений). Вы можете использовать **avg, например,** для расчета средней стоимости затрат на затраты. 
  
**Avg** function does not include any **Null** values in the calculation. 
  

