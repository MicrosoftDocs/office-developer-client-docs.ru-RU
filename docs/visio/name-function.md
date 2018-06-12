---
title: ИМЯ функции
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251580
localization_priority: Normal
ms.assetid: 1ca67a09-9df2-37f5-b269-e761d76bb011
description: Возвращает имя листа в виде строки.
ms.openlocfilehash: 0d3a70573177d8e16a16972d0a08245381b209dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814291"
---
# <a name="name-function"></a>ИМЯ функции

Возвращает имя листа в виде строки.
  
## <a name="syntax"></a>Синтаксис

Имя (** *langID_opt* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Число** <br/> |Используется для указания языка, функция возвращает строки. Используйте 0 (значение по умолчанию), чтобы указать на локальном языке. Используйте 750, чтобы указать универсального языка.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Если передать код незаконную языка, используется локальный язык. 
  

