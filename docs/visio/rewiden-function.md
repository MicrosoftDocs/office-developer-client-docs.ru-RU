---
title: Функция REWIDEN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Преобразует формулу, которая создает 16-разрядные коды символов, которые расширяются однобайтными или многобайтными кодами символов, в строку из 16-разрядных кодов символов Юникод, используя указанные наборы символов.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405214"
---
# <a name="rewiden-function"></a>Функция REWIDEN

Преобразует формулу, которая создает 16-разрядные коды символов, которые расширяются однобайтными или многобайтными кодами символов, в строку из 16-разрядных кодов символов Юникод, используя указанные наборы символов. 
  
## <a name="syntax"></a>Синтаксис

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Обязательный  <br/> |**String** <br/> |Набор символов в исходных документах.  <br/> |
| _dstCharSet_ <br/> |Обязательный  <br/> |**String** <br/> | Набор символов в документе назначения.  <br/> |
| _text_ <br/> |Обязательный  <br/> |**String** <br/> |Текст преобразования.  <br/> |
   
## <a name="remarks"></a>Примечания

Функция REWIDEN используется в автоматическом преобразовании документов 2002 Visio 2002 Visio документов 2003 года. Другое использование не рекомендуется.
  

