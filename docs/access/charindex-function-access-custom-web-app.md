---
title: Функция CharIndex (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: Поиск текстового выражения для другого текстового выражения и возвращает его исходное положение при обнаружении.
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423134"
---
# <a name="charindex-function-access-custom-web-app"></a>Функция CharIndex (Доступ к настраиваемой веб-приложению)

Поиск текстового выражения для другого текстового выражения и возвращает его исходное положение при обнаружении.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**Имя аргумента**|**Обязательный**|**Описание**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |Да  <br/> |Текстовое выражение, содержаное найденный текст.  <br/> |
| *WithinText*  <br/> |Да  <br/> |Текстовое выражение, необходимое для поиска.  <br/> |
| *Start*  <br/> |Нет  <br/> |Integer, который указывает расположение  *в WithinText,*  чтобы начать поиск. Если  *start*  не указан, это отрицательное число или 0, поиск начинается в начале  *WithinText*  .  <br/> |
   
## <a name="remarks"></a>Примечания

Если  *textExpression или*  *WithinText*  является NULL,  *CharIndex*  возвращает NULL. 
  
Если  *TextExpression*  не найден в  *WithinText,*  *CharIndex*  возвращает 0. 
  
Возвращаемая 1-базовая, а не 0-базовая позиция.
  

