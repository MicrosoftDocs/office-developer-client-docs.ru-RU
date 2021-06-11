---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает измерение указанной части окне границы фигуры.
ms.openlocfilehash: a62d5b82c310e7b99e16b70982b75a68172b7fd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428279"
---
# <a name="boundingboxdist-function"></a>Функция BOUNDINGBOXDIST

Возвращает измерение указанной части окне границы фигуры. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXDIST(** *Index* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательный  <br/> |**Number** <br/> |Часть связанного окна фигуры для измерения и возврата. См. примечание для возможных значений.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Number**
  
## <a name="remarks"></a>Примечания

 *Индекс*  может быть одним из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1  <br/> |
|Левый край для фигуры пин-кода  <br/> |2  <br/> |
|Пин-код формы к правому краю  <br/> |3  <br/> |
|Пин-код формы до верхнего края  <br/> |4   <br/> |
|Нижний край для фигуры пин-кода  <br/> |5   <br/> |
|Центр связанного окна с PinX  <br/> |6   <br/> |
|Центр связанного окна с PinY  <br/> |7   <br/> |
   

