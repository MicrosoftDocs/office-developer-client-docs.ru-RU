---
title: Функция AND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Возвращает true (1), если все предоставленные логические выражения имеют true. Если любое из логических выражений false или 0, функция AND возвращает false (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422014"
---
# <a name="and-function"></a>Функция AND

Возвращает true (1), если все логические выражения имеют true. Если любое из логических выражений — FALSE или 0, функция AND возвращает false (0).
  
## <a name="syntax"></a>Синтаксис

AND(** *logical expression1* **, ** *logical expression2* **,..., ** *logical expressionN* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _логическое выражение_ <br/> |Обязательно  <br/> |**Строка** <br/> | Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, которое приводит к значению. Любое выражение, которое оценивается как ненулевой, считается TRUE.  <br/> |
   
## <a name="example"></a>Пример

AND(Height \> 1, PinX \> 1)
  
Возвращает true, если оба выражения имеют true. Возвращает false, если для любого из выражений запроизведется false.
  

