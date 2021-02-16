---
title: Функция CharIndex (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Выполняет поиск текстового выражения для другого текстового выражения и при его обнаружении возвращает его начальное положение.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423134"
---
# <a name="charindex-function-access-custom-web-app"></a>Функция CharIndex (пользовательское веб-приложение Access)

Выполняет поиск текстового выражения для другого текстового выражения и возвращает его начальное положение при обнаружении.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Имя аргумента**|**Обязательный**|**Описание**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Да  <br/> |Текстовое выражение, содержаное текст, который необходимо найти.  <br/> |
| *WithinText*  <br/> |Да  <br/> |Текстовое выражение для поиска.  <br/> |
| *Начало*  <br/> |Нет  <br/> |Integer that specifies the location in  *WithinText*  to begin the search. Если *start* не указан, отрицательное число или 0, поиск начинается с начала *WithinText.*  <br/> |
   
## <a name="remarks"></a>Примечания

Если  *textExpression или*  *WithinText*  имеет NULL,  *CharIndex*  возвращает NULL. 
  
Если  *textExpression*  не найден в  *WithinText,*  *CharIndex*  возвращает 0. 
  
Возвращаемая начальная позиция основана на 1, а не на 0.
  

