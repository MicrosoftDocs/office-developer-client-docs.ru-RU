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
description: Используется в параметре set_expression функции SETATREF, чтобы указать, что set_expression необходимо оценить перед назначением параметра reference в SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432984"
---
# <a name="setatrefeval-function"></a>Функция SETATREFEVAL

Используется в параметре _Set_Expression_ функции SETATREF, чтобы указать, что _Set_Expression_ необходимо оценить перед назначением параметра _Reference_ в SETATREF. 
  
## <a name="syntax"></a>Синтаксис

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Обязательный  <br/> |**Разные** <br/> | Выражение, которое вычисляется, когда функция SETATREF перенаправляет _Set_Expression_ в другую ячейку.  <br/> |
   
## <a name="remarks"></a>Примечания

При присвоении параметру *Set_Expression* функции SETATREF указанной ячейке Microsoft Visio по умолчанию записывает *Set_Expression* в ячейку как выражение. Однако если какая-либо часть параметра *Set_Expression* переносится функцией SETATREFEVAL, Visio вычисляет выражение и заменяет функцию SETATREFEVAL на ее результат перед разрешением выражения SETATREF. 
  
## <a name="example"></a>Пример

Пример приведен в разделе Функция [SETATREF](setatref-function.md) . 
  

