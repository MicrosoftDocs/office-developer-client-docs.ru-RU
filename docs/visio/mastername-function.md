---
title: Функция MASTERNAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251581
localization_priority: Normal
ms.assetid: 519d79d4-9178-2231-c26d-aa7f31a43412
description: Возвращает имя образца листа в виде строки или строка «не образец» Если листа отсутствует главный.
ms.openlocfilehash: c1d5891fba0f967cde4a4e9ca58d07f87239f0b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814210"
---
# <a name="mastername-function"></a>Функция MASTERNAME

Возвращает имя образца листа в виде строки или строка "\<не образец\>" Если листа отсутствует главный.
  
## <a name="syntax"></a>Синтаксис

ИМЯОБРАЗЦА ([** *langID_opt* **]) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Число** <br/> |Используется для указания языка, функция возвращает строки. Используйте 0 (значение по умолчанию), чтобы указать на локальном языке. Используйте 750, чтобы указать универсального языка.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Если передать код незаконную языка, используется локальный язык. 
  

