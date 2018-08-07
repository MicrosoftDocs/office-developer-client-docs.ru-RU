---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Возвращает значение TRUE, если значение ссылка_на_ячейку имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ISERROR используется в формулах, которые ссылаются на другую ячейку.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813997"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Возвращает значение TRUE, если значение _ссылка_на_ячейку_ имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ISERROR используется в формулах, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ЕОШИБКА (** *ссылка_на_ячейку* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _ссылка_на_ячейку_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |= (НД)  <br/> |# Н/Д!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.a1)  <br/> |TRUE  <br/> |
   
Возвращает значение TRUE, так как # н/д! Ошибка распознается функцию ЕОШИБКА. ЕОШ можно использовать для поиска всех типов, но # н/д! Ошибка.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |= «Дом»  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Возвращает значение TRUE, так как #VALUE! Ошибка распознается функцию ЕОШИБКА. Для построения выражения на основании #VALUE! Ошибка, используйте функцию ISERRVALUE.
  

