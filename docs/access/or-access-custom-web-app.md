---
title: OR (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Объединяет два условия. Возвращает true, если оба условия истинны.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414762"
---
# <a name="or-access-custom-web-app"></a>OR (пользовательское веб-приложение Access)

Объединяет два условия. Возвращает true, если оба условия истинны.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 *BooleanExpression* **или** *BooleanExpression* 
  
Оператор **Or** использует следующий аргумент. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *BooleanExpression*  <br/> |Любое допустимые выражения, возвращая true или FALSE.  <br/> |
   
## <a name="remarks"></a>Примечания

Если в операторе используется несколько логических операторов, операторы **Or** оцениваются после операторов **And.** Однако вы можете изменить порядок оценки с помощью скобок. 
  
В следующей таблице показаны результаты работы оператора **Or.** 
  
||**TRUE**|**FALSE**|
|:-----|:-----|:-----|
|**TRUE** <br/> |TRUE  <br/> |TRUE  <br/> |
|**FALSE** <br/> |TRUE  <br/> |FALSE  <br/> |
   

