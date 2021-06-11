---
title: Функция LOCALFORMULAEXISTS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60105
localization_priority: Normal
ms.assetid: 2b757c8d-7732-0f9b-c836-ef755dd1c673
description: Указывает, содержит ли эталонная ячейка локализованную формулу.
ms.openlocfilehash: bd0a5dafecf1bd8dca1567392d880ecaaa3e0374
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433292"
---
# <a name="localformulaexists-function"></a>Функция LOCALFORMULAEXISTS

Указывает, содержит ли эталонная ячейка локализованную формулу. 
  
## <a name="syntax"></a>Синтаксис

LOCALFORMULAEXISTS (** *cellref* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Обязательный  <br/> |**String** <br/> | Ячейка, которую необходимо проверить на наличие формулы.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

Функция LOCALFORMULAEXISTS возвращает 1, если ячейка содержит локализованную формулу; если нет формулы или если формула наследуется, она возвращает 0 (ноль). 
  

