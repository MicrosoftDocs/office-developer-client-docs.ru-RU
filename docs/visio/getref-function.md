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
description: Ссылается на ячейку и не производит повторное вычисление формулы при изменении связанной ячейки.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813847"
---
# <a name="getref-function"></a>Функция GETREF

Ссылается на ячейку и не производит повторное вычисление формулы при изменении связанной ячейки.
  
## <a name="syntax"></a>Синтаксис

GETREF (** *cellname* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Обязательный  <br/> |**Строка** <br/> |Имя для получения ссылки на ячейки.  <br/> |
   
## <a name="example"></a>Пример

SETF(GETREF(PinX),5.1) 
  
Задает формулу в ячейку PinX 5.1. 
  

