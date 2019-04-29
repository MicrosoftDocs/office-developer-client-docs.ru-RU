---
title: NOW Function (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Возвращает текущее значение даты и времени.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414083"
---
# <a name="now-function-visioshapesheet"></a>NOW Function (VisioShapeSheet)

Возвращает текущее значение даты и времени.
  
## <a name="syntax"></a>Синтаксис

NOW ()
  
### <a name="return-value"></a>Возвращаемое значение

Отличным
  
## <a name="remarks"></a>Примечания

ТЕПЕРЬ автоматически пересчитывается каждую минуту. 
  
## <a name="example-1"></a>Пример 1

NOW ()
  
Возвращает текущую дату и время, например 9/27/2010 12:03:30 PM.
  
## <a name="example-2"></a>Пример 2

FORMAT (NOW (), "DD MMM., гггг чч: мм")
  
Возвращает текущую дату и время в формате 27 сентября. 2010 12:03.
  
## <a name="example-3"></a>Пример 3

NOW () + 2EW.
  
Возвращает текущую дату и время, а также две прошедшие недели, например 10/11/10 12:03:30 PM.
  

