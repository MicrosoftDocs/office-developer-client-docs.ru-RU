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
description: Возвращает значение TRUE, если значение целлреференце имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ЕОШИБКА используется в формулах, которые ссылаются на другую ячейку.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421545"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Возвращает значение TRUE, если значение _целлреференце_ имеет любой тип ошибки; в противном случае возвращает значение FALSE. Функция ЕОШИБКА используется в формулах, которые ссылаются на другую ячейку. 
  
## <a name="syntax"></a>Синтаксис

Ошибка (* * *целлреференце* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _целлреференце_ <br/> |Обязательный  <br/> |**String** <br/> |Ссылка на ячейку.  <br/> |
   
## <a name="example-1"></a>Пример 1

|**Cell**|**Formula**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|". A1"  <br/> |= НД ()  <br/> |#N/A!  <br/> |
|"С нуля".  <br/> |= Ошибка (". a1")  <br/> |TRUE  <br/> |
   
Возвращает значение TRUE, так как #N/A! Ошибка распознается функцией ЕОШИБКА. Вы можете использовать ЕОШ для поиска всех типов, но #N/A! ошибкой.
  
## <a name="example-2"></a>Пример 2

|**Cell**|**Formula**|**Возвращаемое значение**|
|:-----|:-----|:-----|
|"С начала. x1"  <br/> |= "Дом"  <br/> |#ЗНАЧ!  <br/> |
|"С нуля".  <br/> |= Ошибка (". x1)"  <br/> |TRUE  <br/> |
   
Возвращает значение TRUE, так как #VALUE! Ошибка распознается функцией ЕОШИБКА. Создание выражения на основе #VALUE! ошибка, используйте функцию ISERRVALUE.
  

