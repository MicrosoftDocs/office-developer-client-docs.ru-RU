---
title: ИЛИ (доступа настраиваемых веб-приложения)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединение двух условий. Возвращает TRUE, если справедливо одно из двух условий.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807084"
---
# <a name="or-access-custom-web-app"></a>ИЛИ (доступа настраиваемых веб-приложения)

Объединение двух условий. Возвращает TRUE, если справедливо одно из двух условий.
  
> [!IMPORTANT]
> Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 *BooleanExpression* **Или** *BooleanExpression* 
  
Оператор **Or** используется следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Любое допустимое выражение, возвращающее значение TRUE или FALSE.  <br/> |
   
## <a name="remarks"></a>Замечания

Если более одного логический оператор, который используется в операторе, **или** операторы вычисляются после операторов **и** . Тем не менее можно изменить порядок вычисления с помощью скобок. 
  
В следующей таблице показаны в результате оператор **Or** . 
  
||**ЗНАЧЕНИЕ TRUE**|**ЗНАЧЕНИЕ FALSE**|
|:-----|:-----|:-----|
|**ЗНАЧЕНИЕ TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**ЗНАЧЕНИЕ FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

