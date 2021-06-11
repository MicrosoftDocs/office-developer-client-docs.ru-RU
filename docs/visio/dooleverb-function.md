---
title: Функция DOOLEVERB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Выполняет глагол для объекта OLE.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435664"
---
# <a name="dooleverb-function"></a>Функция DOOLEVERB

Выполняет глагол для объекта OLE.
  
## <a name="syntax"></a>Синтаксис

DOOLEVERB(" ** *глагол* ** ") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _"глагол"_ <br/> |Обязательный  <br/> |**String** <br/> |Глагол для выполнения.  <br/> |
   
## <a name="remarks"></a>Примечания

В более ранних версиях Visio эта функция отображается как _DOOLEVERB. Visio версии 4.0 и более поздние версии принимают любой стиль. 
  
## <a name="example"></a>Пример

DOOLEVERB ("изменить")
  
Запускает объектную программу OLE и отображает связанный или встроенный объект, чтобы его можно было изменить.
  

