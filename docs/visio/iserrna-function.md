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
description: 'Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — тип #N/A! (недоступны); в противном случае возвращает FALSE. Функция ISERRNA используется в формулах, которые относятся к другой ячейке.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432116"
---
# <a name="iserrna-function"></a>Функция ISERRNA

Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — тип #N/A! (недоступны); в противном случае возвращает FALSE. Функция ISERRNA используется в формулах, которые относятся к другой ячейке. 
  
## <a name="syntax"></a>Синтаксис

ISERRNA(** *cellreference* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |
   
Возвращает FALSE, так как возвращенные значения доступны.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA()  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |
   
Возвращает ЗНАЧЕНИЕ TRUE, так как возвращено значение типа #N/A!
  

