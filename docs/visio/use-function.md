---
title: Функция USE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251510
localization_priority: Normal
ms.assetid: 410c4187-21f3-d959-750e-9dc6095fba9a
description: ПриМеняет к фигуре шаблон линии, узор заливки или конец строки, вызываемый в ячейке в ячейке LinePattern, FillPattern, BeginArrow или EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337151"
---
# <a name="use-function"></a>Функция USE

ПриМеняет к фигуре шаблон линии, узор заливки __ или конец строки, вызываемый в ячейке в ячейке LinePattern, FillPattern, BeginArrow или EndArrow. 
  
## <a name="syntax"></a>Синтаксис

USE ("* * *Name* * *") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Обязательный  <br/> |**String** <br/> |Любая строка, которая является допустимым именем образца.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Комментарии

Если в трафарете документа имеется шаблон именованного _имени_ , шаблон применяется как узор линии, узор заливки, стрелка начала или стрелка конца. 
  
Эта функция всегда возвращает значение 254.
  
## <a name="example"></a>Пример

ИСПОЛЬЗОВАНИЕ ("Раилроадных дорожек") 
  
Форматирует фигуру, применяя к фигуре, содержащей формулу, шаблон образца с именем Раилроад. 
  

