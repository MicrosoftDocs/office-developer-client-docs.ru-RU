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
description: Выполняет команду для объекта OLE.
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813638"
---
# <a name="dooleverb-function"></a>Функция DOOLEVERB

Выполняет команду для объекта OLE.
  
## <a name="syntax"></a>Синтаксис

DOOLEVERB ("** *глаголов* **") 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _«команды»_ <br/> |Обязательный  <br/> |**Строка** <br/> |Для выполнения команды.  <br/> |
   
## <a name="remarks"></a>Замечания

В более ранних версиях Visio эта функция отображается в виде _DOOLEVERB. Visio версии 4.0 и более поздних версий принимать любого из стилей. 
  
## <a name="example"></a>Пример

DOOLEVERB("Edit")
  
Запускает программу объекта OLE и отображает связанный или внедренный объект, в котором ее можно изменить.
  

