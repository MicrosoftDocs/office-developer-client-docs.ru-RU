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
description: При размещении в ячейке LinePattern, FillPattern, BeginArrow или EndArrow используется шаблон строки, или конец строки, называемый именем.
ms.openlocfilehash: ddd15c1c127fafa1a230545d544c74956f5c0262
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422826"
---
# <a name="use-function"></a>Функция USE

При размещении в ячейке LinePattern, FillPattern, BeginArrow или EndArrow используется шаблон строки, или конец строки, называемый именем.  
  
## <a name="syntax"></a>Синтаксис

USE(" ** *имя* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _name_ <br/> |Обязательный  <br/> |**String** <br/> |Любая строка, которая является допустимым мастер-именем.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Если на  трафарете документа присутствует имя мастера, шаблон применяется в качестве шаблона строки, шаблона заполнения, начала стрелки или конечной стрелки. 
  
Эта функция всегда возвращает 254.
  
## <a name="example"></a>Пример

USE ("Железнодорожные пути") 
  
Форматы формы, применяя шаблон магистрали с именем Железнодорожные пути к фигуре, содержащей формулу. 
  

