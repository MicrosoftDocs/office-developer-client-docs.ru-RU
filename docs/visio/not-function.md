---
title: Функция NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Возвращает true (1), если логическоеexpression имеет false. В противном случае возвращается false (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413334"
---
# <a name="not-function"></a>Функция NOT

Возвращает true (1), если  _логическоеexpression_ имеет false. В противном случае возвращается false (0). 
  
## <a name="syntax"></a>Синтаксис

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Обязательно  <br/> |**Строка** <br/> |Логическое выражение для оценки.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="example"></a>Пример

NOT(Height \> 0.75 in) 
  
Возвращает 1, если высота меньше или равна 0,75 дюйма. Возвращает 0, если высота больше 0,75 дюйма. 
  

