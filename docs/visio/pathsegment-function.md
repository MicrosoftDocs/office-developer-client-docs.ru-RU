---
title: Функция PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Возвращает номер сегмента на основе 1 на указанной процентной отметке по указанному пути.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432487"
---
# <a name="pathsegment-function"></a>Функция PATHSEGMENT

Возвращает номер сегмента на основе 1 на указанной процентной отметке по указанному пути.
  
## <a name="syntax"></a>Синтаксис

PATHSEGMENT(** *раздел* **, ** *travel* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Обязательный  <br/> |**String** <br/> |Раздел Геометрия, который представляет путь, заданный ссылкой на его ячейку Path (например, Geometry1.Path).  <br/> |
| _путешествия_ <br/> |Обязательный  <br/> |**Double** <br/> |Процент пройденного пути от точки начала до конечной точки. Должно быть от 0 до 1.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Целое число
  

