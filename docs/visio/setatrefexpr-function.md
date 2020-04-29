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
description: Сохраняет значение, заданное с помощью действия в пользовательском интерфейсе или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a>Функция SETATREFEXPR

Сохраняет значение, заданное с помощью действия в пользовательском интерфейсе или автоматизации.
  
## <a name="syntax"></a>Синтаксис

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Необязательна  <br/> |**Разные** <br/> |Выражение, которое заменяется значением или выражением, присваиваемым указанной ячейке в функции SETATREF. Если не указано, его начальное значение равно 0 (ноль).  <br/> |
   
## <a name="remarks"></a>Примечания

Значение выражения SETATREFEXPR также можно задать из функции SETATREF в другой ячейке, ссылающейся на ячейку, содержащую выражение SETATREFEXPR. 
  
Использование функции SETATREFEXPR в качестве параметра функции SETATREF не ограничено. 
  
## <a name="example-1"></a>Пример 1

В приведенном ниже примере используется функция SETATREFEXPR, чтобы убедиться, что фигура имеет ширину текста.
  
Width = MAX (TEXTWIDTH (TheText), SETATREFEXPR ())
  
## <a name="example-2"></a>Пример 2

В приведенном ниже примере показано, как можно использовать функцию SETATREFEXPR, чтобы фигуры привязываются к настраиваемой сетке. Формулы SETATREFEXPR размещаются в ячейках PinX и PinY, что приводит к привязке ПИН-кода фигуры к сетке, определенной в файле user. Гридкс и User. Grid. 
  
User. Гридкс = 2 in
  
User. Grid = 2 в
  
PinX = INT (SETATREFEXPR ()/Усер.гридкс + 0,5)\*User. гридкс
  
PinY = INT (SETATREFEXPR ()/Усер.Гриди + 0,5)\*User. Grid
  
## <a name="example-3"></a>Пример 3

Пример использования функции SETATREFEXPR с функцией SETATREF представлен в разделе Функция [SETATREF](setatref-function.md) . 
  

