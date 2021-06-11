---
title: Функция SIGN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: Возвращает значение, которое представляет знак номера.
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420656"
---
# <a name="sign-function"></a>Функция SIGN

Возвращает значение, которое представляет знак номера. 
  
## <a name="syntax"></a>Синтаксис

SIGN(** *number* **, ** *fuzz* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Числовой** <br/> | Номер, для которого нужно определить знак.  <br/> |
| _fuzz_ <br/> |Необязательный  <br/> |**Числовой** <br/> |Указывает, насколько близко к нулю должно быть число, чтобы считаться равным нулю.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Функция SIGN возвращает 1, если число положительное, 0, если число нулевое, или -1, если _число_ отрицательное.   
  
Specifyin a  _fuzz_ value helps avoid floating-point roundoff errors when a calculation is almost zero. Если не указать значение _fuzz,_ Visio использует 1E-9 (0.00000000001). Может потребоваться предоставить другое значение при масштабирования рисунков или при точном сравнении. 
  
## <a name="example-1"></a>Пример 1

SIGN(-5)
  
Возвращает -1.
  
## <a name="example-2"></a>Пример 2

SIGN(0)
  
Возвращает 0.
  
## <a name="example-3"></a>Пример 3

SIGN (0.00000000001)
  
Возвращает 0.
  
## <a name="example-4"></a>Пример 4

SIGN (0.00000000001,0)
  
Возвращает 1.
  

