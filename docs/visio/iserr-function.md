---
title: Функция ISERR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Возвращает значение TRUE, если значение cellreference имеет какой-либо тип ошибки, кроме #N/A; в противном случае возвращается false. Функция ISERR используется в формулах, которые ссылаются на другую ячейку.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432109"
---
# <a name="iserr-function"></a>Функция ISERR

Возвращает значение TRUE, если значение  _cellreference_ имеет какой-либо тип ошибки, кроме #N/A; в противном случае возвращается false. Функция ISERR используется в формулах, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Обязательно  <br/> |**Строка** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Formula**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
Возвращает false, так как #N/A! ошибка не распознается функцией ISERR. Используйте ISERROR для поиска всех типов ошибок.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Formula**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#ЗНАЧ!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Возвращает true, так как #VALUE! ошибка распознается функцией ISERR.
  

