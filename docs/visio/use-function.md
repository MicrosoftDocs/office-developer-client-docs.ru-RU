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
description: Применяет шаблон строки, шаблон заливки или название конца строки, называемое именем, к фигуре при размещении в ячейках LinePattern, FillPattern, BeginArrow или EndArrow.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422826"
---
# <a name="use-function"></a>Функция USE

Применяет шаблон строки, шаблон заливки  или название конца строки, называемое именем, к фигуре при размещении в ячейках LinePattern, FillPattern, BeginArrow или EndArrow. 
  
## <a name="syntax"></a>Синтаксис

USE(" ** *name* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Обязательно  <br/> |**Строка** <br/> |Любая строка, которая является допустимым именем хозяина.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Числовой
  
## <a name="remarks"></a>Примечания

Если в  трафарете документа присутствует имя хозяина, шаблон применяется в качестве шаблона линии, шаблона заливки, стрелки начала или стрелки конца. 
  
Эта функция всегда возвращает 254.
  
## <a name="example"></a>Пример

USE("Tracks") 
  
Форматирование фигуры путем применения образца шаблона с именем "Замещая дорожки" к фигуре, содержащей формулу. 
  

