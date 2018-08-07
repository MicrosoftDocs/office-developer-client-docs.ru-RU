---
title: Функция USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Применяет одну из двух выражений в зависимости от значения состояния.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815123"
---
# <a name="userui-function"></a>Функция USERUI

Применяет одну из двух выражений в зависимости от значения _состояния_.
  
## <a name="syntax"></a>Синтаксис

USERUI (** *состояние* **, ** *defaultexpression* **, ** *userexpression* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Обязательный  <br/> |**Boolean** <br/> |Определяет, какие выражение для вычисления.  <br/> |
| _defaultexpression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Выражение по умолчанию.  <br/> |
| _userexpression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Выражение, предоставленные пользователем.  <br/> |
   
## <a name="remarks"></a>Замечания

Если _состояние_ имеет значение 0, функция USERUI вычисляет _defaultexpression_. Если _задано значение 1,_ вычисляет _userexpression_.
  
## <a name="example"></a>Пример

USERUI (1, если (ширина\>на 6, 6 in, ширина), ширина\*0,75) 
  
Применяет выражение ширина\*.075 и возвращает результат. 
  

