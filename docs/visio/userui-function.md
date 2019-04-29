---
title: Функция USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Вычисляет одно из двух выражений в зависимости от значения State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420348"
---
# <a name="userui-function"></a>Функция USERUI

Вычисляет одно из двух выражений в зависимости от значения _State_.
  
## <a name="syntax"></a>Синтаксис

USERUI (* * *State* * *, * * *дефаултекспрессион* * *, * * *усерекспрессион* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Обязательный  <br/> |**Логический** <br/> |Определяет, какое выражение следует вычислить.  <br/> |
| _дефаултекспрессион_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение, используемое по умолчанию.  <br/> |
| _усерекспрессион_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение, предоставленное пользователем.  <br/> |
   
## <a name="remarks"></a>Примечания

Если значение _State_ равно 0, функция USERUI оценивает значение _дефаултекспрессион_. Если _состояние_ равно 1, вычисляется _усерекспрессион_.
  
## <a name="example"></a>Пример

USERUI (1, если (Width\>6in, 6In, Width), Width\*0,75) 
  
Оценивает ширину\*выражения. 075 и возвращает результат. 
  

