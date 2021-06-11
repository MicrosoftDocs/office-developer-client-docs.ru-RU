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
description: Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439053"
---
# <a name="setatrefexpr-function"></a>Функция SETATREFEXPR

Сохраняет значение, за которое устанавливается действие в пользовательском интерфейсе (пользовательском интерфейсе) или автоматизации.
  
## <a name="syntax"></a>Синтаксис

SETATREFEXPR ([ ** *expr_opt* ** ]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Необязательный  <br/> |**Разные** <br/> |Выражение, которое заменяется значением или выражением, назначенным со ссылкой на ячейку в функции SETATREF. Если не указано, его начальное значение — 0 (ноль).  <br/> |
   
## <a name="remarks"></a>Примечания

Значение выражения SETATREFEXPR можно также задать из функции SETATREF в другой ячейке, которая ссылается на ячейку, содержащую выражение SETATREFEXPR. 
  
Вы не ограничивается использованием функции SETATREFEXPR в качестве параметра функции SETATREF. 
  
## <a name="example-1"></a>Пример 1

В следующем примере используется функция SETATREFEXPR для обеспечения того, чтобы форма была такой же широкой, как и ее текст.
  
Width =MAX(TEXTWIDTH(TheText), SETATREFEXPR())
  
## <a name="example-2"></a>Пример 2

В следующем примере показано, как можно использовать функцию SETATREFEXPR для привязки фигур к настраиваемой сетке. Формулы SETATREFEXPR помещаются в ячейки PinX и PinY, в результате чего пин-код фигуры прикрепляется к сетке, определенной в User.GridX и User.GridY. 
  
User.GridX =2 in
  
User.GridY =2 in
  
PinX =INT(SETATREFEXPR()/User.GridX + .5) \* User.GridX
  
PinY =INT(SETATREFEXPR()/User.GridY + .5) \* User.GridY
  
## <a name="example-3"></a>Пример 3

Пример использования функции SETATREFEXPR с функцией SETATREF см. в примере [функции SETATREF.](setatref-function.md) 
  

