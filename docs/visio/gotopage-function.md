---
title: Функция GOTOPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Отображает страницу с именем имя_страницы в активное окно.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813871"
---
# <a name="gotopage-function"></a>Функция GOTOPAGE

Отображает страницу с именем *имя_страницы* в активное окно. 
  
## <a name="syntax"></a>Синтаксис

НАСТРАНИЦУ ("** *имя_страницы* **") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _имя_страницы_ <br/> |Обязательный  <br/> |**Строка** <br/> |Имя страницы, чтобы перейти к.  <br/> |
   
## <a name="remarks"></a>Замечания

Если окно уже отображается страница, это окно становится активной. Если *имя_страницы* не существует, приложение пытается перейти к http:// *имя_страницы* /. Если Visio выступать в качестве сервера на месте, функция НАСТРАНИЦУ не оказывает влияния. 
  
Функция ГИПЕРССЫЛКИ для перехода к любой путь DOS, UNC или URL-адрес. 
  
В более ранних версиях продуктов Visio эта функция отображается в виде _GOTOPAGE. Visio версии 4.0 и более поздних версий принимать любого из стилей. 
  

