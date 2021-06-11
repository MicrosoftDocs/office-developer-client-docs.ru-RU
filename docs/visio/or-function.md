---
title: Функция OR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Возвращает TRUE (1), если любое из логических выражений, переданных в качестве параметров TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433509"
---
# <a name="or-function"></a>Функция OR

Возвращает TRUE (1), если любое из логических выражений, переданных в качестве параметров TRUE.
  
## <a name="syntax"></a>Синтаксис

OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Обязательный  <br/> |**String** <br/> |Первое выражение, истину которого необходимо оценить.  <br/> |
| _logicalexpression2_ <br/> |Обязательный  <br/> |**String** <br/> |Второе выражение, истину которого необходимо оценить.  <br/> |
| _logicalexpressionN_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение Nth, истину которого необходимо оценить.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

Любое выражение, которое оценивается до ненулевых значений, считается TRUE. Если все логические выражения false или равно 0, эта функция возвращает FALSE. 
  
## <a name="example"></a>Пример

OR(Height \> 1,PinX \> 1) 
  
Возвращает TRUE (1), если выражение TRUE. Возвращает FALSE (0) только в том случае, если оба выражения являются FALSE. 
  

