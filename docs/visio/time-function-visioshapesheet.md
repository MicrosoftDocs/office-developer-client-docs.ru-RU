---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Возвращает время, представленное в виде часа, минуты и секунды.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414475"
---
# <a name="time-function-visioshapesheet"></a>TIME Function (VisioShapeSheet)

Возвращает время, представленное в виде _часа_, _минуты_и _секунды_.
  
## <a name="syntax"></a>Синтаксис

TIME (* * *час* * *, * * *минут* * *, * * *секунд* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _час_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Компонент часа.  <br/> |
| _за_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Минута комонент.  <br/> |
| _Втор_ <br/> |Обязательна  <br/> |**Числовой** <br/> |Второй компонент.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="example-1"></a>Пример 1

ВРЕМЯ (15, 30, 30)
  
Возвращает значение, представляющее 15:30:30.
  
## <a name="example-2"></a>Пример 2

FORMAT (время (15, 30, 30), "чч: мм")
  
Возвращает значение, представляющее 15:30.
  
## <a name="example-3"></a>Пример 3

ВРЕМЯ (15, 30, 30) + 8 EH.
  
Возвращает значение, представляющее 23:30:30.
  

