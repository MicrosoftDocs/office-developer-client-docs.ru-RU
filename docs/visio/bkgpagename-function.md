---
title: Функция BKGPAGENAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253219
localization_priority: Normal
ms.assetid: f6e410ef-54d5-9c08-926b-97a2a9786622
description: Возвращает имя фоновой страницы как строку.
ms.openlocfilehash: 290fa62242298b3c513bf2870df37204fab31bf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813282"
---
# <a name="bkgpagename-function"></a>Функция BKGPAGENAME

Возвращает имя фоновой страницы как строку.
  
## <a name="syntax"></a>Синтаксис

BKGPAGENAME (** *langID_opt* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _langID_opt_ <br/> |Optional  <br/> |**Числовой** <br/> |Используется для указания языка, функция возвращает строки. Используйте 0 (значение по умолчанию), чтобы указать на локальном языке. Используйте 750, чтобы указать универсального языка.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Строка
  
## <a name="remarks"></a>Замечания

Если страницы, для которого выполняется с помощью функции не фоновой страницы, строки "\<не фона\>" возвращаются. 
  
Если передать код незаконную языка, используется локальный язык. 
  

