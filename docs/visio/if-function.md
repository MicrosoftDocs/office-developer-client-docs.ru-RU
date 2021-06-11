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
description: Возвращает valueiftrue, если логическиеэкспрессии TRUE. В противном случае возвращается valueiffalse.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405473"
---
# <a name="if-function"></a>Функция IF

Возвращает  _valueiftrue,_ если  _логическиеэкспрессии_ TRUE. В противном случае он возвращает  _valueiffalse_.
  
## <a name="syntax"></a>Синтаксис

IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение для оценки.  <br/> |
| _valueiftrue_ <br/> |Обязательный  <br/> |**Разные** <br/> |Значение, чтобы вернуться, если  _логическиеэкспрессии_ является правдой.  <br/> |
| _valueiffalse_ <br/> |Обязательный  <br/> |**Разные** <br/> | Значение, возвращаемая, если  _логикаэкспрессии_ является ложной.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Разные
  
## <a name="example"></a>Пример

IF (Высота \> 1.25 в,5,7)
  
Возвращает 5, если высота фигуры превышает 1,25 дюйма. Возвращает 7, если высота фигуры меньше или равна 1,25 дюйма.
  

