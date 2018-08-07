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
description: Применяется шаблон линии, узора или имя для фигуры при размещении в ячейке LinePattern, узор заливки, BeginArrow или EndArrow конца строки.
ms.openlocfilehash: 0b6668e57a8f997a69fece51cbc5bd1b1574a576
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815109"
---
# <a name="use-function"></a>Функция USE

Применяется шаблон линии, узора или именем _имя_ фигуры при размещении в ячейке LinePattern, узор заливки, BeginArrow или EndArrow конца строки. 
  
## <a name="syntax"></a>Синтаксис

Использование ("** *имя* **") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Обязательный  <br/> |**Строка** <br/> |Любая строка, которая является допустимым именем главной.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Number
  
## <a name="remarks"></a>Замечания

При наличии в документе шаблона документа с именем _name_ главный шаблон применяется как шаблон линии, узора заливки начать стрелкой, или окончания. 
  
Эта функция всегда возвращает значение 254.
  
## <a name="example"></a>Пример

Использование ("Отслеживание железных") 
  
Форматирует фигуры, применяя главных шаблон с именем отслеживает железных фигуру, содержащий формулу. 
  

