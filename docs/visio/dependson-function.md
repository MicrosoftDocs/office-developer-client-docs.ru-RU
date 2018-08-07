---
title: Функция DEPENDSON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Создает зависимость адреса ячейки.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813589"
---
# <a name="dependson-function"></a>Функция DEPENDSON

Создает зависимость адреса ячейки.
  
## <a name="syntax"></a>Синтаксис

DEPENDSON (** *cellref* ** [, ** *cellref2* **,...]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Обязательный  <br/> |**Строка** <br/> |Первый ссылка на ячейку.  <br/> |
| _cellref2_ <br/> |Optional  <br/> |**Строка** <br/> |Вторая ссылка на ячейку.  <br/> |
   
## <a name="remarks"></a>Замечания

Эта функция всегда возвращает значение FALSE. Он не оказывает влияния при использовании в строку события или в действие ячейки. 
  
## <a name="example"></a>Пример

OPENTEXTWIN() + DEPENDSON(PinX,PinY) 
  
Открывает блок текста фигуры при каждом изменении фигуры PinX или PinY ячеек. 
  

