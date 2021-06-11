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
description: Возвращает ЗНАЧЕНИЕ TRUE, если значение cellreference — это тип ошибки; в противном случае возвращает FALSE. Функция ISERROR используется в формулах, которые относятся к другой ячейке.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421545"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Возвращает ЗНАЧЕНИЕ TRUE, если значение  _cellreference_ — это тип ошибки; в противном случае возвращает FALSE. Функция ISERROR используется в формулах, которые относятся к другой ячейке. 
  
## <a name="syntax"></a>Синтаксис

ISERROR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NA()  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR (Scratch.A1)  <br/> |TRUE  <br/> |
   
Возвращает TRUE, так как #N/A! ошибка распознается функцией ISERROR. Вы можете использовать ISERR для поиска всех типов, кроме #N/A! ошибка.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Формула**|**Возвращено значение**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Дом"  <br/> |#ЗНАЧ!  <br/> |
|Scratch.B1  <br/> |=ISERROR (Scratch.X1)  <br/> |TRUE  <br/> |
   
Возвращает TRUE, потому что #VALUE! ошибка распознается функцией ISERROR. Создание выражения на основе #VALUE! ошибка, используйте функцию ISERRVALUE.
  

