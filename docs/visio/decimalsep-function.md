---
title: Функция DECIMALSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Возвращает строку разделителя целой и дробной части для текущей операционной системы.
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813573"
---
# <a name="decimalsep-function"></a>Функция DECIMALSEP

Возвращает строку разделителя целой и дробной части для текущей операционной системы.
  
## <a name="syntax"></a>Синтаксис

(DECIMALSEP)
  
## <a name="example"></a>Пример

SETF(GETREF(User.Size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

