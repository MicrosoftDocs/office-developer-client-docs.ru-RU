---
title: Функция IF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Возвращает значение valueiftrue, если логическоеexpression имеет значение TRUE. В противном случае возвращается значение.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405473"
---
# <a name="if-function"></a>Функция IF

Возвращает  _значение valueiftrue,_ если  _логическоеexpression_ имеет значение TRUE. В противном случае _возвращается значение._
  
## <a name="syntax"></a>Синтаксис

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Обязательно  <br/> |**Строка** <br/> |Выражение для оценки.  <br/> |
| _valueiftrue_ <br/> |Обязательный  <br/> |**Разные** <br/> |Возвращаемая величина,  _если логическоеexpression_ имеет значение true.  <br/> |
| _valueiffalse_ <br/> |Обязательный  <br/> |**Разные** <br/> | Возвращаемая величина,  _если логическоеexpression_ имеет значение false.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Разные
  
## <a name="example"></a>Пример

IF(Height \> 1.25 in,5,7)
  
Возвращает 5, если высота фигуры превышает 1,25 дюйма. Возвращает 7, если высота фигуры меньше или равна 1,25 дюйма.
  

