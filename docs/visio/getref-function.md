---
title: Функция GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Ссылается на ячейку и не пересчитывает формулу при смене ссылаемой ячейки.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424331"
---
# <a name="getref-function"></a>Функция GETREF

Ссылается на ячейку и не пересчитывает формулу при смене ссылаемой ячейки.
  
## <a name="syntax"></a>Синтаксис

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Обязательный  <br/> |**String** <br/> |Имя ячейки для получения ссылки.  <br/> |
   
## <a name="example"></a>Пример

SETF(GETREF(PinX),5.1) 
  
Задает формулу ячейки PinX до 5.1. 
  

