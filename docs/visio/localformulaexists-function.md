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
description: Показывает, содержит ли указанная ячейка локальную формулу.
ms.openlocfilehash: 1b749011de8554cb5b777fe92b20a6bcdb2fcb19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814122"
---
# <a name="localformulaexists-function"></a>Функция LOCALFORMULAEXISTS

Показывает, содержит ли указанная ячейка локальную формулу. 
  
## <a name="syntax"></a>Синтаксис

LOCALFORMULAEXISTS (** *cellref* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellref_ <br/> |Обязательный  <br/> |**Строка** <br/> | Ячейка, необходимо проверить наличие формулы.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Логический
  
## <a name="remarks"></a>Замечания

Функция LOCALFORMULAEXISTS возвращает 1, если ячейка с формулой локального; Если нет формулы не или наследуется формулу, возвращает нуль (0). 
  

