---
title: Функция CONTAINERSHEETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Возвращает ссылку листа на указанный контейнер, содержащий фигуру.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437268"
---
# <a name="containersheetref-function"></a>Функция CONTAINERSHEETREF

Возвращает ссылку листа на указанный контейнер, содержащий фигуру.
  
## <a name="version-information"></a>Сведения о версии

Добавлена версия: Visio 2010
 
  
## <a name="syntax"></a>Синтаксис

CONTAINERSHEETREF(** *index* ** *** [, category]* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Обязательный  <br/> |**Integer** <br/> |Индекс контейнера на основе 1. Дополнительные сведения см. в комментарии.  <br/> |
| _категория_ <br/> |Необязательный  <br/> |**String** <br/> |Категория контейнера. Дополнительные сведения см. в комментарии.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Ссылка ShapeSheet
  
## <a name="remarks"></a>Примечания

Индекс контейнера рассчитывается на основе Z-порядка контейнеров спереди и сзади.
  
 *Категории —*  это строки, определенные пользователем, которые можно использовать для классификации фигур. Категории можно определить в ячейке User.msvShapeCategories в shapeSheet для фигуры. Вы можете определить несколько категорий для фигуры, разделив категории с полу-двоеточиями. 
  
Если фигура не является членом контейнера или нет контейнера, который соответствует как указанному номеру индекса, так и категории, CONTAINERSHEETREF возвращает #REF!.
  
## <a name="example"></a>Пример

CONTAINERSHEETREF (1)! Высота 
  
Возвращает значение в ячейке Height контейнера, наиболее вперед на странице, к которой принадлежит фигура. 
  

