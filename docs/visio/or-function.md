---
title: Функция OR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Возвращает значение TRUE (1), если какие-либо логических выражений, переданных в качестве параметров имеют значение TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814325"
---
# <a name="or-function"></a>Функция OR

Возвращает значение TRUE (1), если какие-либо логических выражений, переданных в качестве параметров имеют значение TRUE.
  
## <a name="syntax"></a>Синтаксис

ИЛИ (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression1_ <br/> |Обязательный  <br/> |**Строка** <br/> |Первое выражение, чтобы оценить достоверность.  <br/> |
| _logicalexpression2_ <br/> |Обязательный  <br/> |**Строка** <br/> |Второе выражение, чтобы оценить достоверность.  <br/> |
| _logicalexpressionN_ <br/> |Обязательный  <br/> |**Строка** <br/> |N-е выражение, чтобы оценить достоверность.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Логический
  
## <a name="remarks"></a>Замечания

Любое выражение, которое оценивается как ненулевое значение считается значение TRUE. Если все логические выражения имеют значение FALSE или равно 0, эта функция возвращает значение FALSE. 
  
## <a name="example"></a>Пример

ИЛИ (высота \> 1, PinX \> 1) 
  
Возвращает значение TRUE (1), если одно из выражений имеет значение TRUE. Возвращает значение FALSE (0) только в том случае, если оба выражения имеют значение FALSE. 
  

