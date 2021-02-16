---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает измерение указанной части границ фигуры.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428279"
---
# <a name="boundingboxdist-function"></a>Функция BOUNDINGBOXDIST

Возвращает измерение указанной части границ фигуры. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXDIST(** *Index* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательна  <br/> |**Number** <br/> |Часть ограниченного окна фигуры для измерения и возврата. Возможные значения см. в примечаиях.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Number**
  
## <a name="remarks"></a>Примечания

 *Индекс*  может быть одним из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1   <br/> |
|Левый край к контакту фигуры  <br/> |2   <br/> |
|Закрепление фигуры справа  <br/> |3   <br/> |
|Закрепление фигуры к верхнему краю  <br/> |4   <br/> |
|Нижний край к контакту фигуры  <br/> |5   <br/> |
|Центр контактного окна с PinX  <br/> |6   <br/> |
|Центр привязывавного окна к PinY  <br/> |7   <br/> |
   

