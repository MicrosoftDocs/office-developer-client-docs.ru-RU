---
title: Функция BOUNDINGBOXDIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8a2490f2-48c4-5df3-a3b3-40e8e0c80479
description: Возвращает измерения указанную часть фигуры, ограничивающего поля.
ms.openlocfilehash: 94cad37c4a0d2c6c7e7c69d997af09a9d7f1d651
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813310"
---
# <a name="boundingboxdist-function"></a>Функция BOUNDINGBOXDIST

Возвращает измерения указанную часть фигуры, ограничивающего поля. 
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

BOUNDINGBOXDIST (** *индекса* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Обязательный  <br/> |**Число** <br/> |Части фигуры ограничивающего прямоугольника измерения и возврата. Возможные значения см.  <br/> |
   
### <a name="return-value"></a>������������ ��������

 **Число**
  
## <a name="remarks"></a>Замечания

 *Индекс* может иметь одно из следующих значений. 
  
|**Элемент**|**Значение**|
|:-----|:-----|
|Width  <br/> |0  <br/> |
|Height  <br/> |1  <br/> |
|Левая граница для фигуры  <br/> |2  <br/> |
|Фигура прикрепить к правому краю  <br/> |3  <br/> |
|Фигура прикрепить к верхнему краю  <br/> |4  <br/> |
|Нижняя граница для фигуры  <br/> |5  <br/> |
|Центр ограничивающих поле PinX  <br/> |6  <br/> |
|Центр ограничивающих поле PinY  <br/> |7  <br/> |
   

