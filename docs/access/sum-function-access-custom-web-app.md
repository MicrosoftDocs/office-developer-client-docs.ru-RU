---
title: Sum Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Возвращает сумму всех значений в выражении.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427103"
---
# <a name="sum-function-access-custom-web-app"></a>Sum Function (Access custom web app)

Возвращает сумму всех значений в выражении.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **Sum** (*NumericExpression)* 
  
Функция **Sum** содержит следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *NumericExpression*  <br/> |Выражение, определяющие поле, которое содержит числовую информацию, которую необходимо добавить, или выражение, которое выполняет вычисление с использованием данных в этом поле. Операнды в  *NumericExpression*  могут включать имя поля таблицы, константы или функции (которая может быть внутренней или определяемой пользователем, но не одной из других SQL агрегатных функций).  <br/> |
   
## <a name="remarks"></a>Примечания

Функция **Sum** игнорирует записи, содержащие значения NULL. 
  
Функцию **Сумм** можно использовать только с числами столбцов. 
  

