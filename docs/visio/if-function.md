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
description: Возвращает valueiftrue, если logicalexpression имеет значение TRUE. В противном случае возвращает valueiffalse.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813941"
---
# <a name="if-function"></a>Функция IF

Возвращает _valueiftrue_ , если _logicalexpression_ имеет значение TRUE. В противном случае возвращает _valueiffalse_.
  
## <a name="syntax"></a>Синтаксис

Если (** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Выражение для вычисления.  <br/> |
| _valueiftrue_ <br/> |Обязательный  <br/> |**Разные** <br/> |Значение, возвращаемое, если _logicalexpression_ имеет значение true.  <br/> |
| _valueiffalse_ <br/> |Обязательный  <br/> |**Разные** <br/> | Значение, возвращаемое, если _logicalexpression_ имеет значение false.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Разные
  
## <a name="example"></a>Пример

Если (высота \> 1,25 в, 5, 7)
  
Возвращает 5, если высота фигуры больше, чем 1,25 дюйма. Возвращает 7, если высота фигуры — меньше или равно 1,25 дюйма.
  

