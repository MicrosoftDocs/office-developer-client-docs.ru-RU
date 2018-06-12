---
title: Функция SETATREFEXPR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Сохраняет значение, заданное через действие пользовательского интерфейса (UI) или автоматизации.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814765"
---
# <a name="setatrefexpr-function"></a>Функция SETATREFEXPR

Сохраняет значение, заданное через действие пользовательского интерфейса (UI) или автоматизации.
  
## <a name="syntax"></a>Синтаксис

SETATREFEXPR ([** *expr_opt* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Optional  <br/> |**Может отличаться** <br/> |Выражение, которое заменяется значение или выражение, назначаемое для связанной ячейки в ВЫРАЖЕНИЕ_МНОЖЕСТВА функции. Если не указано, его начальное значение равно 0 (ноль).  <br/> |
   
## <a name="remarks"></a>Замечания

Значение выражения SETATREFEXPR можно также задать из ВЫРАЖЕНИЕ_МНОЖЕСТВА функции в другую ячейку, которая ссылается на ячейку, содержащий выражение SETATREFEXPR. 
  
Вы не только с помощью функции SETATREFEXPR в качестве параметра ВЫРАЖЕНИЕ_МНОЖЕСТВА функции. 
  
## <a name="example-1"></a>Пример 1

В следующем примере функция SETATREFEXPR убедитесь, что фигуры по ширине текст.
  
Ширина =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Пример 2

В следующем примере показано, как можно использовать функцию SETATREFEXPR для фигур для привязки к настраиваемой сетке. Формулы SETATREFEXPR помещаются в ячейках PinX и PinY вызывает ошибку фигуры ПИН-кода для привязки к сетке, определенных в User.GridX и User.GridY. 
  
User.GridX = 2
  
User.GridY = 2
  
PinX = INT (SETATREFEXPR /User.GridX () +.5)\*User.GridX
  
PinY = INT (SETATREFEXPR /User.GridY () +.5)\*User.GridY
  
## <a name="example-3"></a>Пример 3

Пример с помощью функции SETATREFEXPR с ВЫРАЖЕНИЕ_МНОЖЕСТВА функции в разделе [ВЫРАЖЕНИЕ_МНОЖЕСТВА](setatref-function.md) функции. 
  

