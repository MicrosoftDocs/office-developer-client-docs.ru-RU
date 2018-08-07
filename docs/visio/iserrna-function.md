---
title: Функция ISERRNA
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Возвращает значение TRUE, если значение ссылка_на_ячейку имеет тип ошибки, # н/д! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813995"
---
# <a name="iserrna-function"></a>Функция ISERRNA

Возвращает значение TRUE, если значение _ссылка_на_ячейку_ имеет тип ошибки, # н/д! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ISERRNA (** *ссылка_на_ячейку* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _ссылка_на_ячейку_ <br/> |Обязательный  <br/> |**Строка** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |= «5 + 3»  <br/> |«8»  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |FALSE  <br/> |
   
Возвращает значение FALSE, так как значение, возвращаемое доступен.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формулы**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |= (НД)  <br/> |# Н/Д!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |TRUE  <br/> |
   
Возвращает TRUE, так как возвращаемое значение Ошибка типа # н/д!
  

