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
description: Возвращает true (1), если любое из логических выражений, переданных в качестве параметров, является TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433509"
---
# <a name="or-function"></a>Функция OR

Возвращает true (1), если любое из логических выражений, переданных в качестве параметров, является TRUE.
  
## <a name="syntax"></a>Синтаксис

OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Обязательно  <br/> |**Строка** <br/> |Первое выражение, истина которого вы хотите оценить.  <br/> |
| _logicalexpression2_ <br/> |Обязательно  <br/> |**Строка** <br/> |Второе выражение, истина которого вы хотите оценить.  <br/> |
| _logicalexpressionN_ <br/> |Обязательно  <br/> |**Строка** <br/> |N-выражение, истина которого вы хотите оценить.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

Любое выражение, которое оценивается как ненулевой, считается TRUE. Если все логические выражения имеют логическое выражение FALSE или равно 0, эта функция возвращает false. 
  
## <a name="example"></a>Пример

OR(Height \> 1,PinX \> 1) 
  
Возвращает true (1), если для любого из выражений засве-ется TRUE. Возвращает false (0), только если оба выражения являются FALSE. 
  

