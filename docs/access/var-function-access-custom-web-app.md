---
title: Var Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Возвращает статистическую дисперсию для выборки, представленной как набор значений, содержащихся в указанном поле в запросе.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437758"
---
# <a name="var-function-access-custom-web-app"></a>Var Function (Access custom web app)

Возвращает статистическую дисперсию для выборки, представленной как набор значений, содержащихся в указанном поле в запросе.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Var** (*NumericExpression)* 
  
Функция **Var** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *NumericExpression*  <br/> |Текстовое выражение, определяющие поле, которое содержит числовой объем данных, которые необходимо оценить, или выражение, которое выполняет вычисление с использованием данных в этом поле. Операнды в  *NumericExpression*  могут включать имя поля таблицы, константы или функции (которая может быть внутренней или определяемой пользователем, но не одной из других SQL агрегатных функций).  <br/> |
   
## <a name="remarks"></a>Примечания

 **Var** можно использовать только с числами столбцов. Значения NULL игнорируются. 
  

