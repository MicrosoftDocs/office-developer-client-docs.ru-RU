---
title: Функция GETVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Получает значение ячейки и не пересчитывает формулу при изменении значения ячейки.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813849"
---
# <a name="getval-function"></a>Функция GETVAL

Получает значение ячейки и не пересчитывает формулу при изменении значения ячейки.
  
## <a name="syntax"></a>Синтаксис

GETVAL (** *cellname* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Обязательный  <br/> |**Строка** <br/> |Имя ячейки, чтобы возвратить значение.  <br/> |
   
## <a name="example"></a>Пример

GETVAL(PinX) + GETVAL(PinY) + ширины 
  
Возвращает сумму значение PinX, PinY и ширина ячеек. 
  

