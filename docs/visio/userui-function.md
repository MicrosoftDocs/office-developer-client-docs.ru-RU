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
description: Оценивает одно из двух выражений в зависимости от значения состояния.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420348"
---
# <a name="userui-function"></a>Функция USERUI

Оценивает одно из двух выражений в зависимости от значения _состояния._
  
## <a name="syntax"></a>Синтаксис

USERUI(** *состояние* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Обязательный  <br/> |**Логический** <br/> |Определяет, какое выражение следует оценить.  <br/> |
| _defaultexpression_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение по умолчанию.  <br/> |
| _userexpression_ <br/> |Обязательный  <br/> |**String** <br/> |Выражение, предоставленное пользователем.  <br/> |
   
## <a name="remarks"></a>Примечания

Если  _состояние_ 0, функция USERUI оценивает  _значение defaultexpression_. Если  _состояние_ 1, он оценивает  _userexpression_.
  
## <a name="example"></a>Пример

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75) 
  
Оценивает выражение Ширина \* .075 и возвращает результат. 
  

