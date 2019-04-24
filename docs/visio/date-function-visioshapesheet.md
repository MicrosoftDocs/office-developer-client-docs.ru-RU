---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Возвращает дату, отформатированную с учетом года, месяца и дня в соответствии с кратким форматом даты в региональных параметрах системы. Значения года, месяца и дня соответствуют григорианскому календарю.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360335"
---
# <a name="date-function-visioshapesheet"></a>DATE Function (VisioShapeSheet)

Возвращает дату, отформатированную с учетом *года, месяца* и *дня* в соответствии с кратким форматом даты в региональных параметрах системы. Значения *года*, *месяца* и *дня* соответствуют григорианскому календарю. 
  
## <a name="syntax"></a>Синтаксис

Дата (* * *год* * *, * * *месяц* * *, * * *день* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Обязательный  <br/> |**Integer** <br/> |Год.  <br/> |
| _month_ <br/> |Обязательный  <br/> |**Integer** <br/> |Месяц.  <br/> |
| _открыт_ <br/> |Обязательный  <br/> |**Integer** <br/> |День.  <br/> |
   
## <a name="example-1"></a>Пример 1

ДАТА (1999, 6, 7)
  
Возвращает значение, представляющее 6/7/1999.
  
## <a name="example-2"></a>Пример 2

Дата (1999, 6, 7) + 4 Ed.
  
Возвращает значение, представляющее 6/11/1999.
  
## <a name="example-3"></a>Пример 3

FORMAT (ДАТА (1999, 10, 14), "C")
  
Возвращает значение, представляющее вторник, 14 октября 1999.
  

