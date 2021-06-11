---
title: Функция PAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251577
localization_priority: Normal
ms.assetid: 12e45f46-e773-9445-4c7f-c726ab648671
description: Возвращает имя страницы в качестве строки.
ms.openlocfilehash: d5527bde58a68c96bd75773f3a0a8c30f64fa20d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438654"
---
# <a name="pagename-function"></a>Функция PAGENAME

Возвращает имя страницы в качестве строки.
  
## <a name="syntax"></a>Синтаксис

PAGENAME (** *langID_opt* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Необязательный  <br/> |**Number** <br/> |Используйте для указания языка для строки, возвращаемой функцией. Для указания локального языка используйте значение 0 (значение по умолчанию). Используйте 750 для указания универсального языка.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

String
  
## <a name="remarks"></a>Примечания

Если вы передаете нелегальный языковый код, используется местный язык.
  

