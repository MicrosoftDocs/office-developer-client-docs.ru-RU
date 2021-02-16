---
title: Функция SETATREFEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Используется в set_expression функции SETATREF, чтобы указать, что set_expression следует оценить перед назначением эталонного параметра в SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432984"
---
# <a name="setatrefeval-function"></a>Функция SETATREFEVAL

Используется в _параметре set_expression_ функции SETATREF,  чтобы указать, что set_expression следует оценить  перед назначением эталонного параметра в SETATREF. 
  
## <a name="syntax"></a>Синтаксис

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Обязательный  <br/> |**Разные** <br/> | Выражение, которое оценивается при перенаправлении функции SETATREF  _set_expression_ в другую ячейку.  <br/> |
   
## <a name="remarks"></a>Примечания

При назначении  *set_expression*  функции SETATREF ячейке, на который ссылается ссылка, Microsoft Visio  *записывает*  set_expression в ячейку в качестве выражения по умолчанию. Однако если любая часть параметра  *set_expression*  оболочка с помощью функции SETATREFEVAL, Visio оценивает выражение и заменяет функцию SETATREFEVAL его результатом перед разрешением выражения SETATREF. 
  
## <a name="example"></a>Пример

Пример см. в [функции SETATREF.](setatref-function.md) 
  

