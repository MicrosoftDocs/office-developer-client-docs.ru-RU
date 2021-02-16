---
title: Функция FORMAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251424
localization_priority: Normal
ms.assetid: 52f5ef4d-07c6-ab36-bf74-b30b50eea221
description: Возвращает результат выражения в виде строки, отформатированной в соответствии с formatpicture.
ms.openlocfilehash: 5eb2195c2bc52e9cc8e7aa8bc4068826a5cd14c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404654"
---
# <a name="format-function"></a>Функция FORMAT

Возвращает результат выражения в _виде_ строки, отформатированной в соответствии _с formatpicture._
  
## <a name="syntax"></a>Синтаксис

FORMAT(** *expression* **," ** *formatpicture* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Обязательно  <br/> |**Строка** <br/> |Сочетание констант, операторов, функций и ссылок на ячейки ShapeSheet, которое приводит к значению.  <br/> |
| _formatpicture_ <br/> |Обязательно  <br/> |**Строка** <br/> |Изображение формата, используемая для перезахмеки строки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Тип выражения и тип, указанные в изображении формата, управляют поведением возвращаемой строки. _Formatpicture_ должен быть подходящим для типа выражения. Дополнительные сведения об указании формата изображений см. в [сведениях о формате изображений.](about-format-pictures.md)
  
Возвращает ошибку, если  результат выражения и тип, ожидаемый в _formatpicture,_ имеют другой вид или имеются ошибки синтаксиса в _formatpicture._
  
## <a name="example-1"></a>Пример 1

FORMAT(1cm/4, "0.000 u")
  
Возвращает "0,250 cm".
  
## <a name="example-2"></a>Пример 2

FORMAT(1cm/4, "0.00 U")
  
Возвращает "0,25 CM".
  
## <a name="example-3"></a>Пример 3

FORMAT(1cm/4, "0.0 u")
  
Возвращает "0,3 cm".
  

