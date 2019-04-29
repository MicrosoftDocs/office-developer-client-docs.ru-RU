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
description: Получает значение ячейки и не вычисляет формулу при изменении значения в ячейке.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416890"
---
# <a name="getval-function"></a>Функция GETVAL

Получает значение ячейки и не вычисляет формулу при изменении значения в ячейке.
  
## <a name="syntax"></a>Синтаксис

GETVAL (* * *целлнаме* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _целлнаме_ <br/> |Обязательный  <br/> |**String** <br/> |Имя ячейки, для которой необходимо получить значение.  <br/> |
   
## <a name="example"></a>Пример

GETVAL (PinX) + GETVAL (PinY) + Width 
  
Возвращает сумму значений ячеек PinX, PinY и Width. 
  

