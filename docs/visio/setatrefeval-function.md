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
description: Используется в параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции указывает, что этот set_expression должно оцениваться перед назначением параметру ссылки в функции SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814743"
---
# <a name="setatrefeval-function"></a>Функция SETATREFEVAL

Используется в _параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции_ указывает, что этот _set_expression_ должно оцениваться перед назначением параметру _ссылки_ в функции SETATREF. 
  
## <a name="syntax"></a>Синтаксис

SETATREFEVAL (** *expr* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Обязательный  <br/> |**Разные** <br/> | Выражение, которое оценивается при ВЫРАЖЕНИЕ_МНОЖЕСТВА функции перенаправляет _set_expression_ на другую ячейку.  <br/> |
   
## <a name="remarks"></a>Замечания

При назначении *параметре ВЫРАЖЕНИЕ_МНОЖЕСТВА функции* на ячейку, который указывает ссылка, Microsoft Visio записывает *set_expression* ячейки как выражение по умолчанию. Тем не менее если любой части *параметре* переносится с помощью функции SETATREFEVAL, Visio применяет выражение и заменяет функции SETATREFEVAL результат перед разрешением выражение функции SETATREF. 
  
## <a name="example"></a>Пример

Пример в разделе [ВЫРАЖЕНИЕ_МНОЖЕСТВА](setatref-function.md) функции. 
  

