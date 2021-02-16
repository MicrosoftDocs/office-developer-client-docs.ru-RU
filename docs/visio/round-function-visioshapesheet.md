---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Округлит число до точности, представленной числомofdigits.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439970"
---
# <a name="round-function-visioshapesheet"></a>ROUND Function (VisioShapeSheet)

Округлит число до точности, представленной *числомofdigits.* 
  
## <a name="syntax"></a>Синтаксис

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Number** <br/> |Номер, который необходимо округить.  <br/> |
| _numberofdigits_ <br/> |Обязательна  <br/> |**Number** <br/> |Количество десятичных мест точности.  <br/> |
   
## <a name="remarks"></a>Примечания

Если _числоofdigits_ больше 0,  число округляется _числомofdigits_ справа от десятичной заголовки. Если  _numberofdigits_ имеет 0,  _число_ округлится до integer. Если _числоofdigits_ меньше 0,  число округляется _числомofdigits_ слева от десятичной заголовки. 
  
## <a name="example-1"></a>Пример 1

ROUND(123.654,2)
  
Возвращает 123,65.
  
## <a name="example-2"></a>Пример 2

ROUND(123.654,0)
  
Возвращает 124.
  
## <a name="example-3"></a>Пример 3

ROUND(123.654,-1)
  
Возвращает 120.
  

