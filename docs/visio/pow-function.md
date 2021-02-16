---
title: Функция POW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Возвращает число, подавленное в силу экспонента.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406313"
---
# <a name="pow-function"></a>Функция POW

Возвращает число, подавленное в силу экспонента.
  
## <a name="syntax"></a>Синтаксис

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |**Number** <br/> |Число, поднимаемого до мощности экспонента.  <br/> |
| _exponent_ <br/> |Обязательна  <br/> |**Number** <br/> |Экспонент.  <br/> |
   
## <a name="remarks"></a>Примечания

Число  _и_  _экспоненты_ могут быть неинтеграционными, а они могут быть отрицательными. Если  _число_ не 0, а  _показатель exponent_ — 0, эта функция возвращает 1. Если  _число_ — 0,  _а показатель exponent_ отрицательный, эта функция возвращает 0,0. Если и _число,_ и _экспоненты_  — 0, или если число отрицательное и _экспоненент_ не является числом, эта функция возвращает 0,0. Если и  _число,_ и  _экспоненты_ отрицательные, эта функция возвращает -1,#IND. 
  
## <a name="example"></a>Пример

POW(5,2) 
  
Возвращает 25. 
  

