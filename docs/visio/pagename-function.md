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
description: Возвращает имя страницы в виде строки.
ms.openlocfilehash: 530707530d60955f460d6a747024b98ebdd5ab62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814344"
---
# <a name="pagename-function"></a>Функция PAGENAME

Возвращает имя страницы в виде строки.
  
## <a name="syntax"></a>Синтаксис

ИМЯ_СТРАНИЦЫ (** *langID_opt* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Число** <br/> |Используется для указания языка, функция возвращает строки. Используйте 0 (значение по умолчанию), чтобы указать на локальном языке. Используйте 750, чтобы указать универсального языка.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Если передать код незаконную языка, используется локальный язык.
  

