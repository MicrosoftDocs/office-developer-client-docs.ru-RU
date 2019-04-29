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
description: 'Возвращает значение TRUE, если значение целлреференце имеет тип ошибки #N/A! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432116"
---
# <a name="iserrna-function"></a>Функция ISERRNA

Возвращает значение TRUE, если значение _целлреференце_ имеет тип ошибки #N/a! (недоступно); в противном случае возвращает значение FALSE. Функция ISERRNA используется в формулах, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ISERRNA (* * *целлреференце* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _целлреференце_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Formula**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|". A1"  <br/> |= "5 + 3"  <br/> |8,5  <br/> |
|"С нуля".  <br/> |= ISERRNA ("a. a1")  <br/> |FALSE  <br/> |
   
Возвращает значение FALSE, так как возвращаемое значение доступно.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Formula**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|". A1"  <br/> |= НД ()  <br/> |#N/A!  <br/> |
|"С нуля".  <br/> |= ISERRNA ("a. a1")  <br/> |TRUE  <br/> |
   
Возвращает значение TRUE, так как возвращаемое значение имеет тип ошибки #N/A!
  

