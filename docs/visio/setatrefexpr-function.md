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
description: Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a>Функция SETATREFEXPR

Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе или автоматизации.
  
## <a name="syntax"></a>Синтаксис

SETATREFEXPR ([ ** *expr_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Необязательна  <br/> |**Разные** <br/> |Выражение, которое заменяется значением или выражением, присвоенным ячейке, на которую ссылается функция SETATREF. Если значение не указано, начальное значение — 0 (ноль).  <br/> |
   
## <a name="remarks"></a>Примечания

Значение выражения SETATREFEXPR также можно установить из функции SETATREF в другой ячейке, которая ссылается на ячейку, содержащую выражение SETATREFEXPR. 
  
В качестве параметра функции SETATREFEXPR можно использовать не только функцию SETATREFEXPR. 
  
## <a name="example-1"></a>Пример 1

В следующем примере функция SETATREFEXPR используется для обеспечения ширины фигуры до ее текста.
  
Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Пример 2

В следующем примере показано, как можно использовать функцию SETATREFEXPR для привязки фигур к настраиваемой сетке. Формулы SETATREFEXPR помещаются в ячейки PinX и PinY, в результате чего контакт фигуры прикреплен к сетке, определенной в User.GridX и User.GridY. 
  
User.GridX =2 in
  
User.GridY =2 in
  
PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX
  
PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY
  
## <a name="example-3"></a>Пример 3

Пример использования функции SETATREFEXPR с функцией SETATREF см. в [функции SETATREF.](setatref-function.md) 
  

