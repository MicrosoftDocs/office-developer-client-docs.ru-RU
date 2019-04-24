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
description: Используется в параметре Set_Expression функции SETATREF, чтобы указать, что перед назначением параметра reference в SETATREF необходимо оценить значение аргумента Set_Expression.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326161"
---
# <a name="setatrefeval-function"></a>Функция SETATREFEVAL

Используется в параметре _Set_Expression_ функции SETATREF, чтобы указать, что __ перед назначением параметра _Reference_ в SETATREF необходимо оценить значение аргумента Set_Expression. 
  
## <a name="syntax"></a>Синтаксис

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Обязательный  <br/> |**Разные** <br/> | Выражение, которое оценивается, когда функция SETATREF перенаправляет аргумент _Set_Expression_ в другую ячейку.  <br/> |
   
## <a name="remarks"></a>Замечания

При назначении аргумента *Set_Expression* функции SETATREF ячейке, на которую указывает ссылка, Microsoft Visio записывает аргумент *Set_Expression* в ячейку как выражение по умолчанию. Тем не менее, если какая-либо часть параметра *Set_Expression* упакована функцией SETATREFEVAL, Visio вычисляет выражение и заменяет функцию SETATREFEVAL на ее результат перед разрешением выражения SETATREF. 
  
## <a name="example"></a>Пример

Пример приведен в разделе Функция [SETATREF](setatref-function.md) . 
  

