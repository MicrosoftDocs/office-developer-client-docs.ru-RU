---
title: Функция не
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Возвращает значение TRUE (1), если logicalexpression имеет значение FALSE. В противном случае возвращается значение FALSE (0).
ms.openlocfilehash: e2359aaab18469cd4f272f71aca8d899a12b2120
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814304"
---
# <a name="not-function"></a>Функция не

Возвращает значение TRUE (1), если _logicalexpression_ имеет значение FALSE. В противном случае возвращается значение FALSE (0). 
  
## <a name="syntax"></a>Синтаксис

НЕ (** *logicalexpression* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Обязательный  <br/> |**Строка** <br/> |Логическое выражение для оценки.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Логический
  
## <a name="example"></a>Пример

НЕ (высота \> 0,75 in) 
  
Возвращает значение 1, если высота — меньше или равно 0,75 дюйма. Возвращает 0, если высота больше, чем 0,75 дюйма. 
  

