---
title: Функция HASCATEGORY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Возвращает TRUE, если указанная строка находится в списке категорий фигуры.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433355"
---
# <a name="hascategory-function"></a>Функция HASCATEGORY

Возвращает TRUE, если указанная строка находится в списке категорий фигуры.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

HASCATEGORY (** *категория* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _категория_ <br/> |Обязательный  <br/> |**String** <br/> |Категория, для поиска.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

 **Boolean**
  
## <a name="remarks"></a>Примечания

 *Категории —*  это строки, определенные пользователем, которые можно использовать для классификации фигур. Категории можно определить в ячейке User.msvShapeCategories в shapeSheet для фигуры. Вы можете определить несколько категорий для фигуры, разделив категории с полу-двоеточиями. 
  

