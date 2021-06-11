---
title: Функция subString (Доступ к настраиваемой веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Возвращает часть текстового выражения.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433474"
---
# <a name="substring-function-access-custom-web-app"></a>Функция subString (Доступ к настраиваемой веб-приложению)

Возвращает часть текстового выражения.
  
> [!IMPORTANT]
> Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint. В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств. 
  
## <a name="syntax"></a>Синтаксис

 **SubString** *(TextExpression*, *Start*, *Length*) 
  
Функция **SubString** содержит следующие аргументы. 
  
|**Имя аргумента**|**Описание**|
|:-----|:-----|
| *TextExpression*  <br/> |Текстовое выражение.  <br/> |
| *Start*  <br/> |Integer expression that specifies where the returned characters start. Если начало меньше 1, возвращаемая экспрессия начнется с первого символа, указанного в выражении. В этом случае количество возвращаемого символа является самым большим значением суммы начала + длины — 1 или 0. Если начало больше количества символов в выражении значения, возвращается выражение нулевой длины.  <br/> |
| *Length*  <br/> |Положительное integer выражение, которое указывает, сколько символов выражения будет возвращено. Если длина является отрицательной, создается ошибка и завершается утверждение. Если сумма начала и длины больше, чем количество символов в выражении, возвращается все выражение значения, начиная с начала.  <br/> |
   

