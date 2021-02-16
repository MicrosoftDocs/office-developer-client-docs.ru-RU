---
title: Функция MAGNITUDE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Возвращает величину вектора, чей рост — A, а поток — B, умноженный на соответствующие константы constantA и constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420460"
---
# <a name="magnitude-function"></a>Функция MAGNITUDE

Возвращает величину вектора, чей рост _— A,_ а поток — _B,_ умноженный на соответствующие константы _constantA_ и _constantB._ 
  
## <a name="syntax"></a>Синтаксис

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Обязательна  <br/> |**Number** <br/> |Константа, на которую нужно умножить повышение.  <br/> |
| _A_ <br/> |Обязательна  <br/> |**Number** <br/> |Повышение.  <br/> |
| _constantB_ <br/> |Обязательна  <br/> |**Number** <br/> |Константа, на которую нужно умножить запуск.  <br/> |
| _B_ <br/> |Обязательна  <br/> |**Number** <br/> |Запуск.  <br/> |
   
## <a name="remarks"></a>Примечания

ВЕЛИЧИНА вычисляется по следующей формуле:
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>Пример

MAGNITUDE(1, 3, 1, 4) 
  
Возвращает 5. 
  

