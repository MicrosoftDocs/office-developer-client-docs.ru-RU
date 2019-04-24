---
title: Функция LISTSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251882
localization_priority: Normal
ms.assetid: 73dc5981-2c8c-e76e-e4bd-e65a7c8db242
description: Возвращает строку с разделителем списков для текущего языкового стандарта пользователя.
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322346"
---
# <a name="listsep-function"></a>Функция LISTSEP

Возвращает строку с разделителем списков для текущего языкового стандарта пользователя.
  
## <a name="syntax"></a>Синтаксис

LISTSEP ()
  
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="example"></a>Пример

SETF (GETREF (User. экстент), "MAX (ширина" &amp; ListSep () &amp; "высота)") 
  

