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
description: Возвращает строку "list-separator" для текущего пользовательского региональных точки.
ms.openlocfilehash: 901442a3c2af8509855b8b038057e7f813634ea1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431409"
---
# <a name="listsep-function"></a>Функция LISTSEP

Возвращает строку "list-separator" для текущего пользовательского региональных точки.
  
## <a name="syntax"></a>Синтаксис

LISTSEP ()
  
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="example"></a>Пример

SETF(GETREF(user.extent), "MAX(Width" &amp; ListSep() &amp; "Height)") 
  

